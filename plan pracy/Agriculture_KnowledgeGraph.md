# Plan pracy — Agriculture_KnowledgeGraph

## Stan audytu
**AUDYT ZAKOŃCZONY — 2026-09-12**

## Klasyfikacja
Archiwalny projekt badawczy Agricultural Knowledge Graph. README stwierdza, że projekt nie jest już utrzymywany. Kod i dane mają wartość referencyjną, ale stos jest historyczny i wymaga migracji przed jakimkolwiek użyciem produkcyjnym.

## Ustalenia
- Python + Django + Neo4j/py2neo.
- Zależności obejmują Django `>=1.11.7`, py2neo `4.1.0`, pyfasttext `0.4.5`, pymongo oraz narzędzia NLP.
- Struktura obejmuje crawler Scrapy, przetwarzanie danych, aplikację Django, KNN, crawler drzewa oraz import relacji Wikidata.
- Dane obejmują encje rolnicze, etykiety, relacje Wikidata oraz zależności pogodowo-roślinne.
- README zawiera procedury ręcznego importu CSV do Neo4j i tworzenia ograniczeń indeksowych.
- Dokumentacja odwołuje się do historycznych wersji Neo4j/Django i zawiera procedury ręcznej konfiguracji.
- Projekt jest jawnie oznaczony jako nieutrzymywany.

## Ryzyka
1. Bardzo stary stos Django/py2neo i potencjalna niezgodność z obecnym Pythonem/Neo4j.
2. Dane pochodzące z crawlowania wymagają oceny licencyjnej, jakościowej i aktualności.
3. Procedury importu używają historycznej składni ograniczeń Neo4j.
4. W dokumentacji występuje bezpośrednia konfiguracja danych dostępowych Neo4j w kodzie.
5. Brak podstaw do traktowania projektu jako produkcyjnego bez pełnej migracji i reprodukcji eksperymentów.

## Plan dalszych prac
1. Zachować repozytorium jako archiwum referencyjne.
2. Oddzielić kod eksperymentalny, crawler, dane i aplikację demonstracyjną.
3. Jeśli projekt ma zostać reaktywowany, przeprowadzić migrację do wspieranej wersji Pythona, Django i Neo4j oraz zastąpić py2neo aktualnym sterownikiem.
4. Zastąpić ręczne importy skryptami idempotentnymi i walidacją schematu grafu.
5. Usunąć dane dostępowe z kodu i przejść na zmienne środowiskowe/sekrety.
6. Dodać testy jednostkowe parserów, ETL, mapowania encji i zapytań grafowych.
7. Zdefiniować reprodukowalny dataset testowy zamiast wymagania pełnych danych historycznych.
8. Udokumentować pochodzenie danych i ograniczenia licencyjne.
9. Przetłumaczyć dokumentację operacyjną na polski przy zachowaniu nazw technologii i cytowania publikacji.

## Kryterium zakończenia
Projekt pozostaje **ARCHIWALNY/REFERENCYJNY**, chyba że zostanie podjęta decyzja o reaktywacji. W przypadku reaktywacji wymagane są: migracja stosu, bezpieczna konfiguracja, testy ETL/grafu, reprodukowalny import oraz potwierdzenie jakości i praw do danych.
