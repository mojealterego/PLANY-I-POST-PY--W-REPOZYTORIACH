# Plan pracy — agent-framework

## Status
AUDYT ZAKOŃCZONY — framework agentowy, średnio-duży.

## Stan faktyczny
Repozytorium ma około 140 MB, `main`. Wymaga mapowania agentów, modeli, narzędzi, pamięci, transportów i testów.

## Ryzyka
- tool execution;
- auth i sekrety;
- prompt/tool injection;
- koszty i niekontrolowane pętle;
- kompatybilność API modeli.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Mapa architektury.
2. Policy/approval boundaries.
3. Testy bezpieczeństwa i regresji.
4. Observability i limity.

## Kryterium zakończenia
Kontrolowany runtime agentów z deterministycznymi granicami narzędzi.
