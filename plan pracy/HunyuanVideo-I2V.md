# Plan pracy — HunyuanVideo-I2V

## Status
AUDYT ZAKOŃCZONY — duży projekt generowania wideo image-to-video.

## Stan faktyczny
Repozytorium ma około 150 MB i `main`. Przed użyciem należy zweryfikować pipeline inferencji, wymagania GPU, pobieranie wag i licencje.

## Ryzyka
- provenance/licencje wag;
- wysokie wymagania GPU;
- bezpieczeństwo wejść multimedialnych;
- generowanie wizerunków bez zgody.

## Priorytet
WYSOKI — REFERENCJA.

## Kolejność prac
1. Pipeline i zależności.
2. Model weights/provenance.
3. Reprodukowalność GPU.
4. Polityka zgody i bezpieczne dane wejściowe.

## Kryterium zakończenia
Reprodukowalna inferencja, potwierdzone licencje i bezpieczny proces danych.
