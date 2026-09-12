# Audyt: graphify

## Status
AUDYT ZAKOŃCZONY — narzędzie knowledge-graph dla repozytoriów.

## Stan faktyczny
README opisuje CLI `graphify`, lokalne parsowanie AST przez tree-sitter, graf zależności, zapytania/path/explain, mapowanie dokumentów i mediów oraz integrację z wieloma asystentami. Repo ma wersję `v8` jako domyślną gałąź i wiele tłumaczeń, w tym polskie.

## Ryzyka
Rozjazd między `EXTRACTED` i `INFERRED`, instalacja skills do repozytoriów, hooki Git, semantyczne przetwarzanie dokumentów/mediów oraz deklarowane benchmarki wymagające niezależnej reprodukcji.

## Priorytet
WYSOKI — duża wartość dla bazy wiedzy i audytów.

## Kolejność prac
1. reprodukcja benchmarków;
2. walidacja provenance krawędzi;
3. audyt instalatora i hooków;
4. testy izolacji danych;
5. wykorzystanie jako warstwa indeksowania w Knowledge-projects.

## Kryterium zakończenia
Graf jest deterministyczny dla kodu, inferencje są jawnie oznaczone, a instalacja nie modyfikuje projektu poza deklarowanym zakresem.
