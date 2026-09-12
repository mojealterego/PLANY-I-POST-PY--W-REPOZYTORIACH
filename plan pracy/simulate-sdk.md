# simulate-sdk — plan pracy

## Status
AUDYT ZAKOŃCZONY — SDK Python z rozbudowaną dokumentacją.

## Stan faktyczny
Repozytorium zawiera `fi/`, `examples/`, `docs/`, `.github`, `pyproject.toml`, `poetry.lock`, `requirements.txt`, README, SECURITY i CONTRIBUTING. Obecność lockfile i CI wskazuje na projekt pakietowy z naciskiem na reprodukowalność.

## Ryzyka
- dwa źródła deklaracji zależności (`pyproject` i requirements) mogą się rozjechać;
- trzeba zweryfikować wersję Pythona i kompatybilność runtime;
- duży zakres SDK wymaga testów kontraktowych API.

## Priorytet
WYSOKI

## Kolejność prac
1. Przejrzeć pyproject, testy i workflow CI.
2. Ujednolicić źródło zależności i politykę lockfile.
3. Zweryfikować publiczne API oraz przykłady.
4. Dodać testy integracyjne i macierz wersji Python.
5. Następnie polonizacja dokumentacji/rebranding.

## Kryterium zakończenia
Reproducible install, pełne testy API i CI, zgodność manifestów oraz brak rozbieżności między dokumentacją i kodem.
