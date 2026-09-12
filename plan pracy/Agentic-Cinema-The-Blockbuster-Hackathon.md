# Plan pracy — Agentic-Cinema-The-Blockbuster-Hackathon

## Stan audytu
- **Audyt:** zakończony
- **Klasyfikacja:** prototyp hackathonowy / system agentowy do operacji produkcji filmowej
- **Priorytet:** KRYTYCZNY
- **Produkcja:** NIE

## Ustalenia
Repozytorium implementuje StudioSync: warstwę decyzyjną dla odzyskiwania produkcji filmowej po incydencie. README deklaruje przepływ incydent → analiza równoległa → brief oparty na dowodach → bramka akceptacji człowieka. Dostępne są tryb deterministycznego demo oraz ścieżka skonfigurowana z Google ADK/Gemini i ClickHouse MCP.

`requirements.txt` obejmuje Google ADK, Google GenAI, Vertex AI, FastAPI, Uvicorn, Pydantic, HTTPX, dotenv i pytest. `pyproject.toml` definiuje Python >=3.11 i pakiet `studiosync` 0.1.0. Orkiestrator wyraźnie rozdziela demo od live i nie zwraca danych syntetycznych jako rzekomo pobranych z ClickHouse.

## Ryzyka / luki
1. Live graph jest budowany, ale `run_studiosync()` kończy się wyjątkiem informującym o konieczności podłączenia konkretnego runnera/session service ADK; nie jest to jeszcze pełna ścieżka produkcyjna.
2. Zależności mają dolne granice, ale brak pełnego lockfile ogranicza reprodukowalność.
3. Integracja MCP wymaga audytu autoryzacji, TLS, timeoutów, limitów odpowiedzi i obsługi błędów.
4. Należy zweryfikować, czy każdy element briefu ma jednoznaczne pochodzenie: wejście, fixture, MCP lub inferencja modelu.
5. Konieczne jest potwierdzenie CI i kompletności testów bez zakładania ich skuteczności wyłącznie na podstawie README.

## Kolejność prac
1. Przejrzeć `agents/`, `core/`, `services/`, `app/`, `web/`, `tests/` i konfigurację CI.
2. Zdefiniować kontrakt `evidence → finding → recommendation → approval`.
3. Dodać testy kontraktowe zapobiegające pomieszaniu danych syntetycznych z live evidence.
4. Dokończyć adapter wykonawczy ADK/session i jawny lifecycle sesji.
5. Utwardzić MCP: autoryzacja, TLS, timeouty, limity, retry/backoff i read-only enforcement.
6. Zweryfikować obsługę błędów oraz zachowanie przy częściowej awarii specjalistów.
7. Ustabilizować zależności i środowisko reprodukowalne.
8. Uruchomić testy, lint i smoke test; dopiero po tym oceniać gotowość wdrożeniową.
9. Wykonać rebranding i pełną polonizację własnej warstwy dokumentacyjnej.

## Kryterium zakończenia
Pełna ścieżka demo i live musi być wykonywalna, rozróżnienie źródeł dowodów musi być testowane, a wszystkie granice akceptacji człowieka i integracji MCP muszą być jawne. Sam audyt nie oznacza gotowości produkcyjnej.
