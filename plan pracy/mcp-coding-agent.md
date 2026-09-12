# Plan pracy — mcp-coding-agent

## Stan audytu
- **Audyt:** zakończony
- **Klasyfikacja:** autonomiczny builder agentów i oprogramowania przez MCP
- **Priorytet:** KRYTYCZNY
- **Produkcja:** NIE

## Ustalenia
Repozytorium implementuje manager-style orchestration z wyspecjalizowanymi agentami: architekt, planner, coding, review, QA, debugging, security i DevOps. Udostępnia MCP przez Streamable HTTP oraz narzędzia budowania, projektowania, pracy na workspace i inspekcji Git. README deklaruje ochronę project root, kontrolę ścieżek/symlinków, ograniczenie wykonywania komend oraz usuwanie typowych sekretów z procesów potomnych.

`pyproject.toml` definiuje Python >=3.11, wersję 1.0.1, MCP >=2,<3, OpenAI Agents >=0.6,<1, Pydantic, dotenv i Uvicorn. Dostępne są CLI `mcp-coding-agent` i `mcp-coding-agent-cli`, testy w `tests/` oraz konfiguracja Ruff.

## Ryzyka / luki
1. To system, który może generować i wykonywać kod, więc izolacja workspace nie może być jedyną granicą bezpieczeństwa dla niezaufanego kodu.
2. `/mcp` posiada opcjonalny Bearer token; dla zdalnego wdrożenia należy wymusić bezpieczną konfigurację zamiast traktować auth jako opcjonalne zabezpieczenie.
3. `/health` pozostaje publiczny — należy potwierdzić, że nie ujawnia danych operacyjnych.
4. `execute_workspace_command` wymaga testów allow/deny, timeoutów, limitów zasobów, symlinków i prób wyjścia poza workspace.
5. Planowany GitHub write/deployment wymaga osobnych, minimalnych poświadczeń i bramek zatwierdzających.
6. README przyznaje brak aktywnego checkoutu/runtime w tej sesji, dlatego CI/testy nie są tutaj uznawane za wykonane.

## Kolejność prac
1. Przejrzeć `src/mcp_coding_agent/`, `tests/`, `scripts/`, Dockerfile, Railway i CI.
2. Przetestować wszystkie operacje plikowe względem project root i symlinków.
3. Zbudować macierz polityki komend: dozwolone, blokowane, wymagające dodatkowej zgody.
4. Dodać twardą izolację wykonania dla niezaufanego wygenerowanego kodu: kontener/VM/sandbox.
5. Zweryfikować MCP auth, TLS/proxy, limity requestów i odporność na nieufne wejście.
6. Przetestować pętlę plan → implementacja → test → repair → security → finalize bez możliwości przedwczesnego „success”.
7. Zweryfikować trwałość stanu budowy i odporność na restart/przerwanie.
8. Dopiero potem projektować kontrolowane adaptery GitHub/deployment z approval gates.
9. Wykonać testy jednostkowe, kontraktowe, HTTP smoke i CI; następnie rebranding/polonizację.

## Kryterium zakończenia
Żaden wygenerowany kod ani narzędzie nie może samodzielnie rozszerzyć zakresu uprawnień systemu. Operacje workspace/MCP muszą być ograniczone, testowane i audytowalne, a ścieżka produkcyjna musi posiadać izolację i jawne approval gates.
