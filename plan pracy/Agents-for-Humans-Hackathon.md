# Plan pracy — Agents-for-Humans-Hackathon

## Status audytu
AUDYT ZAKOŃCZONY — repozytorium #39 w bieżącym przebiegu.

## Stan faktyczny
Projekt **CogniSync Professional** jest publicznym artefaktem hackathon/grant dla agentów profesjonalnych. README deklaruje deterministyczny prototyp z rozdzieleniem `prepared ≠ authorized ≠ executed`, bramką decyzji człowieka, audytem hash-chain oraz testami ścieżek pozytywnych i błędnych. Integracja Strands/Bedrock jest adapterem, a nie dowodem wdrożenia chmurowego.

Stack: Python >=3.11, `strands-agents`, opcjonalnie AWS/Bedrock i evals, pytest, Ruff. Repo zawiera `cognisync/`, `tests/`, `docs/`, `scripts/` oraz konfigurację CI/środowiska.

## Mocne strony
- jawna granica działań konsekwencyjnych;
- fail-closed dla nieznanych możliwości;
- deterministyczny tryb demo bez efektów zewnętrznych;
- rozbudowane testy jednostkowe bezpieczeństwa i zachowania;
- ledger audytowy i claim ledger rozdzielający implementację od roadmapy.

## Ryzyka / luki
- produkcyjna integracja AWS/Bedrock wymaga osobnej walidacji IAM, sekretów, timeoutów, retry i obserwowalności;
- brak dowodu produkcyjnego persistence/RBAC/webhooków w publicznym prototypie;
- dokumentacja grantowa jest po angielsku i wymaga pełnej polonizacji w ramach docelowego procesu;
- należy zweryfikować kompletność CI i powtarzalność środowiska instalacyjnego.

## Kolejność prac
1. Potwierdzić strukturę modułów domenowych, policy, verification, decision gate i adapterów.
2. Uruchomić testy + Ruff + quality check w reprodukowalnym środowisku.
3. Przeprowadzić testy kontraktowe granicy `prepared/authorized/executed`.
4. Dodać/zweryfikować persistence, RBAC, sekrety, webhook authentication i kill switch dopiero dla wariantu produkcyjnego.
5. Polonizacja README/docs z zachowaniem terminologii technicznej.
6. Rebranding po ustaleniu docelowej nazwy produktu.
7. Dopiero po testach integracyjnych rozważyć status produkcyjny.

## Kryterium zakończenia
Powtarzalny build, zielone testy i lint, udokumentowane trust boundaries oraz jednoznaczna separacja demonstratora od rzeczywistych efektów zewnętrznych.
