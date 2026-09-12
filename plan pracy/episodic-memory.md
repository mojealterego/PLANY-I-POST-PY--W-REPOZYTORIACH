# episodic-memory — plan pracy

## Status
AUDYT ZAKOŃCZONY — projekt pamięci agentów.

## Stan faktyczny
Repozytorium ok. 2 MB, z własną implementacją pamięci epizodycznej. Wymaga sprawdzenia modelu danych, API, storage i integracji z agentami.

## Ryzyka
- przechowywanie treści rozmów i danych wrażliwych;
- brak izolacji kontekstu może prowadzić do wycieku pamięci;
- retencja i usuwanie danych muszą być jawne.

## Priorytet
WYSOKI

## Kolejność prac
1. Zmapować schema/storage i API.
2. Zdefiniować tenant/session boundaries.
3. Dodać testy retencji, usuwania i izolacji.
4. Zabezpieczyć embeddings/indeksy, jeśli występują.
5. Polonizacja/rebranding.

## Kryterium zakończenia
Deterministyczna izolacja pamięci, kontrolowana retencja i testy odczytu/zapisu/usuwania.
