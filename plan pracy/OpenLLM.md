# Audyt 321 — OpenLLM

## Stan
AUDYT ZAKOŃCZONY — framework/serwer do uruchamiania LLM, referencyjny.

## Ustalenia
Repozytorium zawiera runtime i integracje do serwowania modeli językowych, z API i warstwą wdrożeniową. Ze względu na model wykonawczy kluczowe są konfiguracja modeli, endpointy, zasoby GPU/CPU i provenance zależności.

## Ryzyka
Nieautoryzowany dostęp do endpointów; pobieranie modeli; zasoby obliczeniowe; supply chain; sekrety providerów.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Zmapować serwer, API, model registry i deployment.
2. Zweryfikować auth/rate limiting i izolację procesu.
3. Zweryfikować testy i wersje zależności.
4. Zachować jako materiał referencyjny.

## Kryterium zakończenia
Zweryfikowane granice API, modeli i deploymentu.