# Plan pracy — G0DM0D3

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: wielomodelowy interfejs AI / red teaming / aplikacja webowa
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- Projekt posiada rozbudowane README, dokumentację API, bezpieczeństwa, warunków i trybu modeli lokalnych.
- Główna powierzchnia to pojedynczy `index.html`; dodatkowo istnieją `src/` dla React/Next.js, `api/` oraz funkcja telemetryczna Cloudflare.
- Projekt obsługuje OpenRouter, Venice i lokalne serwery zgodne z API OpenAI; ma lokalną historię w `localStorage`.
- Telemetria jest domyślnie aktywna, a README szczegółowo opisuje jej zakres oraz tryby No-Log/Local-only.
- README wskazuje możliwość wysyłania surowego promptu do pomocniczego modelu w celu klasyfikacji oraz opcjonalne zbieranie pełnej treści w API po świadomym ustawieniu flagi.
- Występuje kilka równoległych powierzchni aplikacji, co zwiększa ryzyko rozbieżności między wersją standalone a React/API.

## Ryzyka
1. Klucze dostawców są przechowywane w pamięci przeglądarki; należy zweryfikować model zagrożeń i XSS.
2. Telemetria i klasyfikator promptów wymagają ścisłej kontroli prywatności i dokumentacji zgód.
3. Opcjonalny zapis pełnych rozmów do datasetu wymaga twardych barier przed ujawnieniem danych.
4. Pojedynczy duży `index.html` i duże komponenty TSX utrudniają testowanie oraz utrzymanie.
5. Lista modeli dostawców jest dynamiczna i może się dezaktualizować.

## Kolejność prac
1. Zdefiniować kanoniczną powierzchnię produkcyjną i rozdzielić ją od eksperymentalnych modułów.
2. Zmapować przepływy danych, granice zaufania, sekrety, telemetrię i eksport danych.
3. Wydzielić domenę, transporty dostawców, scoring i polityki prywatności.
4. Wprowadzić testy kontraktowe dla dostawców i deterministyczne testy scoringu.
5. Dodać ochronę danych, walidację schematów, limity i fail-safe dla datasetu.
6. Uporządkować build/deploy oraz CI dla wszystkich aktywnych powierzchni.
7. Przeprowadzić polonizację dokumentacji i interfejsu bez utraty technicznej precyzji.

## Kryterium zakończenia
Jedna jasno zdefiniowana ścieżka produkcyjna ma przechodzące testy, jawny model prywatności, kontrolowane sekrety, odseparowane eksperymenty i powtarzalny build.
