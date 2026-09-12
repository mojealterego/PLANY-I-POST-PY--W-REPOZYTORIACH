# P0 — Agent-Android → B2B AI Employee

## Stan

**WYBRANY FUNDAMENT P0 — REFAKTORYZACJA R1/R2 W TOKU.**

`Agent-Android` został wybrany jako główny własny fundament wykonawczy pierwszego produktu P0: **B2B AI Employee**.

## Ustalenia bazowe

Repo ma `apps/mobile`, `services/agent-api`, `services/mcp-server`, `plugins/agent-android`, `packages/shared` i CI. README deklaruje server-side authorization, explicit approval dla działań konsekwencyjnych, brak kluczy w repo i obserwowalność. Root `package.json` v0.2.0 posiada workspace'y oraz wspólny `check`: typecheck → lint → test → build.

## Wykonane — R1 Auth/Session

1. Dodano `services/agent-api/src/session.ts` z weryfikacją podpisanego, wygasającego bearer session assertion.
2. Endpoint `/v1/agent/ask` wymaga uwierzytelnionego bearer session przed uruchomieniem agenta.
3. `organizationId`, `actorId` i `sessionId` są wyprowadzane z zweryfikowanej sesji; dane klienta nie są źródłem autorytatywnego tenant context.
4. Dodano odmowę cross-tenant/cross-actor: mismatch kończy się `403`.
5. Brak sesji lub sesja nieprawidłowa/wygasła kończy się `401`.
6. Brak konfiguracji `AUTH_SESSION_SECRET` kończy się fail-closed `503`.
7. Dodano testy: brak sesji, brak konfiguracji, malformed token, actor mismatch, organization mismatch, poprawna sesja i wygasła sesja.
8. CI podniesiono do Node `22.13.0`, zgodnie z wymaganiem projektu.
9. `docs/ARCHITECTURE.md` zaktualizowano o rzeczywistą granicę weryfikacji sesji i ograniczenia obecnego mechanizmu.

## Ograniczenie R1

To jest wewnętrzna granica weryfikacji podpisanej sesji, a nie kompletny dostawca OAuth/OIDC. Przed produkcją należy podłączyć zaufanego issuer'a enterprise, rotację kluczy i właściwy mechanizm sesyjny. Długowieczny sekret podpisujący nie może trafić do klienta.

## R2 — deny-by-default Tool Authorization

**Następny punkt wykonywany teraz.**

Cel:
- nieznane narzędzie → odmowa,
- narzędzie niezarejestrowane → odmowa,
- brak wymaganej zgody → odmowa,
- działanie konsekwencyjne → wymaga osobnej bramki approval,
- polityka ma być testowalna niezależnie od transportu MCP,
- dopiero jawnie zarejestrowane narzędzia mogą zostać rozważone do wykonania.

## Kolejne etapy

R3 — approval state machine → R4 — MCP/execution isolation → R5 — Memory/RAG → R6 — Audit/Observability → R7 — security/integration/E2E → R8 — B2B integrations → R9 — billing/quotas → R10 — Android E2E/release.

## Kryterium produkcyjne

Nieautoryzowana akcja jest niemożliwa w testach kontraktowych i integracyjnych, tenant isolation jest zweryfikowane, narzędzia są deny-by-default, approval jest audytowalny, execution jest izolowane, a build klienta i usług jest reprodukowalny.
