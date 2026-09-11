# Plan pracy — WAO-AI-2

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: wieloagentowy system specyfikacji wizualnej / prompt compiler / MCP
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- Projekt definiuje przepływ `ANALYZE → MAP → LOCK → TRANSFORM → COMPILE → VALIDATE → OUTPUT`.
- Autorzy wskazują `protocol/`, `agents/`, `orchestrator/`, `adapters/`, `mcp/`, `security/`, `tests/`, `examples/` i `docs/` jako główne warstwy.
- Structured visual state i constraint graph są traktowane jako źródło prawdy, a prompt jako artefakt kompilacji.
- README deklaruje least-authority access, blokady tożsamości, change budgets, invarianty i adversarial QA.

## Ryzyka
1. Złożony graf ograniczeń wymaga testów niezmienników i deterministycznego rozwiązywania konfliktów.
2. Adaptery modeli mogą wprowadzać różnice semantyczne.
3. MCP stanowi granicę uprawnień i musi być audytowany niezależnie.
4. „Reference-faithful” wymaga jasnych kryteriów mierzalnych, aby nie opierać jakości na subiektywnej ocenie.

## Kolejność prac
1. Zweryfikować strukturę protokołu, schematy i kontrakty agentów.
2. Zbudować formalny model stanu i zmian lokalnych/globalnych.
3. Przetestować orchestrator jako maszynę stanów.
4. Dodać kontraktowe testy adapterów i testy regresyjne promptów.
5. Audytować MCP i politykę najmniejszych uprawnień.
6. Zbudować zestaw testów adversarial QA i kryteriów akceptacji.
7. Polonizować dokumentację i komunikaty, zachowując kanoniczne identyfikatory protokołu.

## Kryterium zakończenia
Zmiany są lokalne i deterministyczne, kontrakty są walidowane automatycznie, adaptery są izolowane, a końcowy artefakt przechodzi bramkę QA.
