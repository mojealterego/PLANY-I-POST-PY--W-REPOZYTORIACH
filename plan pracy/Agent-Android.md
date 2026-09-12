# P0 — Agent-Android → B2B AI Employee

## Stan

**WYBRANY FUNDAMENT P0 — REFAKTORYZACJA R1 ROZPOCZĘTA.**

`Agent-Android` został wybrany jako główny własny fundament wykonawczy pierwszego produktu P0: **B2B AI Employee**.

## Ustalenia bazowe

Repo ma `apps/mobile`, `services/agent-api`, `services/mcp-server`, `plugins/agent-android`, `packages/shared` i CI. README deklaruje server-side authorization, explicit approval dla działań konsekwencyjnych, brak kluczy w repo i obserwowalność. Root `package.json` v0.2.0 posiada workspace'y oraz wspólny `check`: typecheck → lint → test → build.

## Wykonane w Etapie 3 / R1

1. Rozszerzono `packages/shared/src/contracts.ts` o `organizationId`, `actorId` i `AgentExecutionContext`.
2. Dodano kontrakty `ToolAuthorizationRequest` i `ToolAuthorizationDecision`.
3. Utworzono `docs/P0-B2B-AI-EMPLOYEE.md`.
4. Zmieniono kontrakt endpointu `/v1/agent/ask`: `organizationId` i `actorId` są wymagane przez walidację wejścia.
5. Dodano test kontraktowy potwierdzający odrzucenie żądania bez kontekstu organizacji i aktora.

## Ważne ograniczenie

Samo przyjęcie `organizationId` i `actorId` z żądania **nie jest jeszcze uwierzytelnieniem**. Komentarz w implementacji wyraźnie ustanawia te wartości jako kontekst wymagający późniejszego związania z autentyczną sesją serwerową. Do czasu implementacji Auth/Session nie wolno traktować tych identyfikatorów jako dowodu tożsamości lub członkostwa w organizacji.

## Następny krok R1

- znaleźć/wybrać mechanizm sesji i tożsamości,
- powiązać aktora z sesją serwerową,
- wyznaczać organizację na podstawie autoryzowanego kontekstu,
- odrzucać spoofing `actorId` / `organizationId`,
- dodać testy cross-tenant denial,
- fail-closed przy braku sesji.

## Kolejne etapy

R2 — deny-by-default tool authorization → R3 — approval state machine → R4 — MCP/execution isolation → R5 — Memory/RAG → R6 — Audit/Observability → R7 — security/integration/E2E → R8 — B2B integrations → R9 — billing/quotas → R10 — Android E2E/release.

## Kryterium produkcyjne

Nieautoryzowana akcja jest niemożliwa w testach kontraktowych i integracyjnych, tenant isolation jest zweryfikowane, narzędzia są deny-by-default, approval jest audytowalny, execution jest izolowane, a build klienta i usług jest reprodukowalny.
