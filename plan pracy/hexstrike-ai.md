# hexstrike-ai — plan pracy

## Status
AUDYT ZAKOŃCZONY — platforma cyberbezpieczeństwa; wyłącznie autoryzowane laboratoria.

## Stan faktyczny
README opisuje MCP server, wieloagentową automatyzację testów, ponad 150 narzędzi, browser automation i API. Wymaga dalszej walidacji kodu, manifestu i procesów wykonawczych.

## Ryzyka
- bardzo szeroka powierzchnia narzędzi ofensywnych;
- subprocess, sieć i przetwarzanie celu przez agenta;
- możliwość niekontrolowanego łańcucha działań.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Mapa narzędzi i entrypointów.
2. Default-deny, allowlisty celów i sandbox.
3. Separacja planowania od wykonania i approval gates.
4. Audyt logów, sekretów, timeoutów i izolacji procesów.
5. Testy tylko na fixture/lab.

## Kryterium zakończenia
Brak automatycznego dostępu do nieautoryzowanych celów i pełny audyt każdej operacji wykonawczej.
