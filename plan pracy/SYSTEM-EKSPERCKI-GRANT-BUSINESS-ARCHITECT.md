# Plan pracy — SYSTEM-EKSPERCKI-GRANT-BUSINESS-ARCHITECT

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: system wieloagentowy / architektura AI / granty i biznes
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- README definiuje topologię agentów, ledger dowodów, walidację spójności, audyt zgodności i bramkę akceptacji człowieka.
- Repozytorium zawiera obecnie README, `packages/` oraz `pyproject.toml`; opis wskazuje znacznie szerszą strukturę, której należy faktycznie poszukać i potwierdzić.
- Doktryna projektu kładzie nacisk na brak fabrykowania faktów, deterministyczne finanse i śledzenie pochodzenia twierdzeń.

## Ryzyka
1. Duża różnica między architekturą deklarowaną a aktualnym stanem implementacji.
2. Wysokie ryzyko błędów w danych finansowych i kwalifikacji grantowej bez silnych kontraktów.
3. Potrzeba izolacji źródeł, założeń i brakujących danych.
4. Konsekwencje błędów wymagają obowiązkowej kontroli człowieka przed wysłaniem dokumentów.

## Kolejność prac
1. Zinwentaryzować faktyczne pakiety i punkty wejścia.
2. Ustalić kontrakty domenowe: projekt, dowód, źródło, założenie, program finansowania, budżet i werdykt audytowy.
3. Wprowadzić Clean Architecture i separację agentów od narzędzi/infrastruktury.
4. Zbudować deterministyczny silnik finansowy i testy niezmienników.
5. Dodać provenance, walidację schematów i bramki human-in-the-loop.
6. Dodać testy integracyjne agentów i odporność na sprzeczne dane.
7. Uporządkować CI, dokumentację i pełną polonizację.

## Kryterium zakończenia
Każde istotne twierdzenie ma źródło lub jawny status założenia/braku danych, obliczenia są testowalne, a konsekwentne pakiety dokumentów wymagają zatwierdzenia człowieka przed finalizacją.
