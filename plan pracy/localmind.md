# Plan pracy — localmind

## Status
AUDYT ZAKOŃCZONY — duża aplikacja lokalnego AI.

## Stan faktyczny
Repozytorium ma około 50 MB i główną gałąź `main`. Wymaga sprawdzenia runtime, modeli, storage, interfejsu i integracji sieciowych.

## Ryzyka
- lokalne modele i pobieranie wag;
- prywatność danych użytkownika;
- sandboxing narzędzi;
- GPU/CPU compatibility.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapowanie runtime/model managera.
2. Storage i dane lokalne.
3. Izolacja narzędzi i procesów.
4. Testy urządzeń.
5. Polonizacja UI/docs.

## Kryterium zakończenia
Bezpieczny lokalny runtime, reprodukowalne instalacje i testy sprzętowe.
