# Plan pracy — ollama

## Status
AUDYT ZAKOŃCZONY — duży runtime lokalnych modeli AI; projekt referencyjny.

## Stan faktyczny
Repozytorium ma około 93 MB i `main`. To komponent infrastrukturalny do uruchamiania modeli lokalnie; zmiany muszą respektować upstream i kompatybilność platform.

## Ryzyka
- natywne runtime i GPU;
- model supply chain;
- API sieciowe i ekspozycja lokalnego serwera;
- bezpieczeństwo modeli i danych.

## Priorytet
KRYTYCZNY — REFERENCJA.

## Kolejność prac
1. Mapowanie runtime/API.
2. Kontrola bindów sieciowych i auth.
3. Testy platform/GPU.
4. Provenance modeli.

## Kryterium zakończenia
Zweryfikowana wersja runtime, bezpieczna ekspozycja API i reprodukowalne testy.
