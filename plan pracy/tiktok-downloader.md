# Plan pracy — tiktok-downloader

## Status
AUDYT ZAKOŃCZONY — narzędzie pobierania treści z serwisu zewnętrznego.

## Stan faktyczny
Repozytorium ma około 2,8 MB. Wymaga sprawdzenia klienta HTTP, parsera, storage i aktualności endpointów.

## Ryzyka
- zmiany API/stron;
- ograniczenia usług i rate limits;
- prawa autorskie i warunki serwisu;
- niebezpieczne URL-e i pliki wyjściowe.

## Priorytet
ŚREDNI/WYSOKI.

## Kolejność prac
1. Mapa pobierania/parsing.
2. Walidacja URL i ograniczenia zasobów.
3. Testy fixture offline.
4. Dokumentacja zgodnego użycia.

## Kryterium zakończenia
Stabilne testy parsera i bezpieczne pobieranie bez obchodzenia zabezpieczeń usług.
