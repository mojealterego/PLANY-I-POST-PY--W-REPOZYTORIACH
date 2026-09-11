# Plan pracy — wifi-densepose

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Projekt Python/FastAPI do estymacji pozy człowieka z CSI WiFi bez kamer.
- Posiada równoległą implementację Rust v2, WebSocket, REST API, tracking i moduły analityczne.
- README deklaruje bardzo wysokie wyniki benchmarków Rust oraz 100% pokrycie/testy; wymagają one niezależnej reprodukcji.
- Rozszerzenie WiFi-Mat deklaruje detekcję parametrów życiowych, lokalizację i triage dla ratownictwa.

## Ryzyka
1. Deklarowane benchmarki i coverage muszą zostać zweryfikowane.
2. Funkcje związane z parametrami życiowymi i triage wymagają szczególnie rygorystycznej walidacji.
3. Należy zweryfikować bezpieczeństwo API, autoryzację i rate limiting.
4. Należy porównać wyniki Python/Rust pod kątem zgodności matematycznej.

## Plan implementacji
1. Zmapować pakiety Python i workspace Rust.
2. Zweryfikować model danych CSI i matematyczne transformacje.
3. Odtworzyć benchmarki w kontrolowanym środowisku.
4. Zbudować testy cross-language Python/Rust.
5. Zweryfikować REST/WebSocket security.
6. Oddzielić core signal processing od warstw aplikacyjnych.
7. Przeprowadzić audyt modułu WiFi-Mat i jawnie oznaczyć ograniczenia wyników.
8. Uzupełnić obserwowalność i testy obciążeniowe.
9. Spolonizować dokumentację.

## Kryterium zakończenia
Reprodukowalne benchmarki, zgodność implementacji Python/Rust, testy API, udokumentowane ograniczenia i kompletna dokumentacja.