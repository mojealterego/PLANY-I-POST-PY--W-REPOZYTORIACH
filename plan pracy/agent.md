# Plan pracy — agent

## Status
AUDYT ZAKOŃCZONY — 1MCP unified MCP runtime.

## Stan faktyczny
README opisuje `1mcp serve`, agregację wielu MCP, CLI dla agentów, progresywne `instructions → inspect → run`, presety/filtry oraz tryb proxy/direct HTTP. Repo jest narzędziem infrastrukturalnym o znaczącej powierzchni uprawnień.

## Ryzyka
agregacja zaufania wielu serwerów; auth; konfiguracja per projekt/sesję; wykonywanie narzędzi; zbyt szeroki tool surface; sekrety i lifecycle procesu.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zmapować transporty i mechanizmy auth.
2. Zweryfikować izolację konfiguracji projektu/sesji.
3. Dodać allowlisty serwerów i narzędzi oraz audyt wywołań.
4. Testy negatywne dla nieautoryzowanych `run`.
5. Polska dokumentacja operacyjna.

## Kryterium zakończenia
Deterministyczne uprawnienia, audytowalne wykonanie narzędzi i testy izolacji.