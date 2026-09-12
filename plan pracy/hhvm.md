# Audyt: hhvm

## Status
AUDYT ZAKOŃCZONY — duży projekt referencyjny/runtime.

## Stan faktyczny
README potwierdza HHVM jako VM/JIT dla Hack, z Proxygen/FastCGI i osobnymi licencjami dla komponentów Hack. Repozytorium jest bardzo duże; nie należy traktować go jako zwykłego projektu aplikacyjnego.

## Ryzyka
Złożony C++/Hack runtime, JIT, bezpieczeństwo wykonania kodu, ogromny koszt kompilacji/testów oraz wielolicencyjny kod.

## Priorytet
ŚREDNI — referencyjny, wysoki ciężar techniczny.

## Kolejność prac
1. zachować upstream provenance;
2. mapować moduły potrzebne do własnych projektów;
3. sprawdzić SECURITY i CI przed ewentualnym użyciem;
4. nie wykonywać szerokiego rebrandingu upstream bez celu.

## Kryterium zakończenia
Jasna klasyfikacja jako zależność/referencja i udokumentowane moduły faktycznie wykorzystywane.
