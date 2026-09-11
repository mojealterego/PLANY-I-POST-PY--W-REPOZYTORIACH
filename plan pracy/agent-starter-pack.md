# Plan pracy — agent-starter-pack

## Stan audytu
**AUDYT ZAKOŃCZONY — 2026-09-12**

## Klasyfikacja
CLI i zestaw szablonów do tworzenia projektów agentowych na Google Cloud. Repozytorium jest w trybie utrzymania; README jednoznacznie wskazuje migrację nowych projektów do `agents-cli`. Należy zachować je jako bazę migracyjną/referencyjną i nie prowadzić nieuzasadnionej rozbudowy funkcjonalnej.

## Ustalenia
- Python `>=3.10`.
- Pakiet `agent-starter-pack`, wersja `0.41.3`.
- CLI wystawia polecenie `agent-starter-pack`.
- Główne zależności obejmują Click, Cookiecutter, Google Cloud AI Platform, Rich, PyYAML, Backoff i Requests.
- Repozytorium ma pytest, pytest-cov, pytest-mock, xdist oraz narzędzia Ruff, ty i codespell.
- Testy integracyjne są domyślnie wyłączone z konfiguracji pytest.
- Szablony obejmują m.in. ReAct, RAG, multi-agent, Live API oraz warianty ADK/A2A.
- README wskazuje Cloud Run, Agent Engine, Terraform, CI/CD, obserwowalność i ewaluację Vertex AI.
- Aktualny kierunek projektu to migracja do `agents-cli`; stare repozytorium otrzymuje wyłącznie krytyczne poprawki.

## Ryzyka
1. Ryzyko budowania nowych projektów na technologii będącej w maintenance mode.
2. Ryzyko rozjazdu dokumentacji ze stanem `agents-cli`.
3. Wyłączenie testów integracyjnych z domyślnego przebiegu może ukrywać problemy wdrożeniowe.
4. Szablony obejmują wiele stosów i usług chmurowych, więc potrzebna jest macierz kompatybilności.
5. Koszty i skutki wdrożeń Google Cloud muszą pozostać jawne dla użytkownika.

## Plan dalszych prac
1. Nie dodawać nowych funkcji do ASP bez uzasadnienia zgodnością/migracją.
2. Zmapować wszystkie szablony i ich odpowiedniki w `agents-cli`.
3. Przygotować kontrolę kompletności migracji dla istniejących projektów.
4. Rozdzielić testy jednostkowe od integracyjnych i zapewnić osobny, obowiązkowy etap CI dla testów integracyjnych przed wdrożeniem.
5. Zweryfikować Terraform, CI/CD, obserwowalność i konfigurację bezpieczeństwa każdego szablonu.
6. Ujednolicić polską dokumentację migracyjną, bez usuwania oryginalnej terminologii technicznej.
7. Zachować repozytorium jako wersjonowany punkt odniesienia do czasu zakończenia migracji.

## Kryterium zakończenia
Audyt/refaktoryzacja tego repozytorium jest zakończona dopiero po potwierdzeniu, że wszystkie aktywnie używane szablony mają ścieżkę migracji do `agents-cli`, a projekty zależne od ASP mają udokumentowany stan i przechodzą odpowiednie testy.
