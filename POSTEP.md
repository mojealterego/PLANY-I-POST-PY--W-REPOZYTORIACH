# Rejestr postępu — ARCH-ENG-CORE-999

## Stan bieżący

- Data aktualizacji: 2026-09-12
- Faza: **3 — wybór produktu P0 i refaktoryzacja fundamentu wykonawcza**
- Inwentaryzacja portfela: **414 repozytoriów**
- Rekonsyliacja inwentarza: **414/414 — zakończona**
- Audyt szczegółowy: **414/414 — zakończony**
- Konsolidacja wyników: **zakończona**
- Ranking priorytetów: **zakończony**
- Produkt P0: **B2B AI Employee**
- Główny fundament implementacyjny: **Agent-Android**
- Refaktoryzacja P0: **R1 zakończone, R2 rozpoczęte**
- Rebranding: oczekuje
- Polonizacja: oczekuje
- Nowe produkty pochodne: oczekują

## Decyzja P0

Wybrano **B2B AI Employee** jako produkt nadrzędny pierwszej kolejności. `Agent-Android` jest własnym, modularnym fundamentem wykonawczym i pozostaje bazą pierwszej implementacji. Repo nie jest jeszcze oznaczone jako produkcyjne.

`mojealterego/Nowe-projekty` pozostaje poza zakresem tej refaktoryzacji; pracuje tam osobny agent.

## Wykonane prace Etapu 3 / R1

W `mojealterego/Agent-Android`:

- dodano podpisaną, wygasającą weryfikację bearer session assertion,
- endpoint `/v1/agent/ask` wymaga zweryfikowanej sesji przed uruchomieniem agenta,
- tenant i actor context są wyprowadzane z sesji serwerowej,
- mismatch aktora/organizacji jest odrzucany (`403`),
- brak/niepoprawna/wygasła sesja jest odrzucana (`401`),
- brak sekretu weryfikacyjnego kończy się fail-closed (`503`),
- dodano testy izolacji tenantów i aktora,
- CI dostosowano do Node `22.13.0`,
- architekturę zaktualizowano o rzeczywistą granicę sesji.

## R2 — wykonane części kontraktowe

- dodano jawny rejestr polityk narzędzi,
- nieznane narzędzie jest domyślnie odrzucane,
- brak wymaganej permission jest odrzucany,
- approval jest odrębnym warunkiem dla narzędzi konsekwencyjnych,
- dodano testy deny-by-default.

Pełne podłączenie polityki do transportu MCP i zweryfikowanego `authInfo` pozostaje elementem dalszej realizacji R2; nie uznaję R2 za zamknięte na podstawie samego rejestru.

## Następna kolejka implementacyjna

1. Dokończyć R2: transport MCP → zweryfikowany auth context → per-tool authorization.
2. R3: approval state machine.
3. R4: MCP/execution isolation.
4. R5: Memory/RAG z kontrolą dostępu.
5. R6: audyt i obserwowalność.
6. R7: testy security/integration/E2E.
7. R8: integracje B2B.
8. R9: billing, quotas i kontrola kosztów.
9. R10: Android E2E oraz reprodukowalny release.

## Bramka produkcyjna

Żaden wynik etapu audytu ani rozpoczęcie refaktoryzacji nie oznacza produkcyjności. Status produkcyjny może zostać nadany dopiero po buildzie, testach, hardeningu bezpieczeństwa, weryfikacji izolacji tenantów, recovery/migracjach, obserwowalności, provenance zależności/modeli i kontroli kosztów.

## Dokumenty

- `README.md` — stan globalny
- `AUDYT_GLOBALNY.md` — zasady audytu
- `POSTEP.md` — dziennik procesu
- `KONSOLIDACJA_414.md` — konsolidacja
- `RANKING_PRIORYTETOW_414.md` — ranking
- `plan pracy/*.md` — indywidualne plany
