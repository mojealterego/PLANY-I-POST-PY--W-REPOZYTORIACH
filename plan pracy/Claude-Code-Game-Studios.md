# Plan pracy — Claude-Code-Game-Studios

## Status
AUDYT ZAKOŃCZONY — system organizacji pracy AI dla produkcji gier.

## Stan faktyczny
README opisuje 49 agentów, 73 skills, 12 hooks, 11 rules i 41 templates, z hierarchią dyrektorów, leadów i specjalistów oraz obsługą Godot/Unity/Unreal. System jest przede wszystkim konfiguracją workflow dla Claude Code.

## Ryzyka
nadmierne uprawnienia agentów/hooks; wykonywanie zmian w repo; niespójność ról; konflikty instrukcji; brak testów zachowania agentów; zależność od konkretnej wersji klienta.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować agentów, hooks, rules i skills.
2. Ustalić hierarchię uprawnień i approval gates.
3. Testy konfliktów instrukcji i niepożądanych zmian.
4. Dodać wersjonowanie kontraktów agentów.
5. Polska dokumentacja i szablony.

## Kryterium zakończenia
Każda rola ma ograniczony zakres, kryteria jakości i ścieżkę eskalacji; workflow jest testowalny.