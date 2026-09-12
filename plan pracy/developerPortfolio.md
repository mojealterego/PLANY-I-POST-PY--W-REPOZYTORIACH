# Plan pracy — developerPortfolio

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: szablon portfolio React
- Priorytet: ŚREDNI
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Repozytorium jest szablonem portfolio opartym o Create React App/React. README deklaruje Node/npm oraz integrację z GitHub API przez `git_data_fetcher.js`. Manifest używa starego React 16, `react-scripts` 3.2.0, `node-sass` 4.14.1, GraphQL 14 oraz wielu historycznych bibliotek UI. `homepage` jest ustawione na `.`. README nadal zawiera instrukcje odnoszące się do pierwotnego repozytorium autora i szerokich tokenów GitHub.

## Ryzyka
1. Bardzo stary stos build/runtime i potencjalna niezgodność ze współczesnym Node.
2. `node-sass` i CRA 3.2 wymagają modernizacji.
3. Integracja GitHub wymaga ścisłego zakresu tokena i bezpiecznego zarządzania sekretami.
4. Dokumentacja zawiera historyczne linki i instrukcje wymagające aktualizacji.
5. Brak potwierdzonego współczesnego CI i testów E2E.

## Kolejność prac
1. Inwentaryzacja komponentów i źródeł danych.
2. Migracja builda do współczesnego React/Vite lub równoważnego rozwiązania.
3. Usunięcie `node-sass`, aktualizacja routera, GraphQL i bibliotek UI.
4. Izolacja GitHub API od frontendu i minimalizacja uprawnień tokena.
5. Testy komponentów, smoke test build/deploy i walidacja danych GitHub.
6. Aktualizacja dokumentacji i pełna polonizacja.

## Kryterium zakończenia
Powtarzalny build produkcyjny, testy przechodzące w CI, bez sekretów w kodzie, aktualna dokumentacja i zweryfikowany deployment.
