# InvokeAI

## Status
AUDYT ZAKOŃCZONY — duży, profesjonalny silnik kreatywny AI do mediów wizualnych.

## Stan faktyczny
Rozbudowana aplikacja lokalna z serwerem webowym i UI React, Unified Canvas, workflow/node systemem, galerią i obsługą wielu modeli dyfuzyjnych. README wskazuje CI, dokumentację, testy społecznościowe i wiele formatów modeli.

## Ryzyka
Duża powierzchnia zależności/modeli, pobieranie wag, GPU, potencjalnie duże zasoby lokalne oraz import nieufnych workflow/plików. Należy zweryfikować sandboxing i provenance modeli.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapowanie monorepo i systemu build/test.
2. Audyt ładowania modeli, workflow i rozszerzeń.
3. Aktualizacja zależności i bezpieczeństwa supply chain.
4. Polska lokalizacja UI/dokumentacji.
5. Testy GPU/CPU i regresji.

## Kryterium zakończenia
Reprodukowalny build/test, kontrolowane źródła modeli i workflow, brak niejawnego wykonania nieufnego kodu oraz kompletna lokalizacja.