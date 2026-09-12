# Audyt 300 — AI-Resume-Optimizer

## Stan
AUDYT ZAKOŃCZONY — aplikacja AI do analizy/optymalizacji CV.

## Ustalenia
Repozytorium ma istotny rozmiar i stanowi osobny produkt aplikacyjny. Zakres wymaga dalszego mapowania entrypointów, zależności, przepływu dokumentów i modelu AI.

## Ryzyka
Prywatne dane CV, przesyłanie dokumentów, sekrety API, prompt injection przez treść CV oraz retencja danych.

## Priorytet
WYSOKI

## Plan prac
Mapowanie UI/API → izolacja dokumentów → redakcja/logowanie → auth → walidacja wyników AI → testy → deployment → polonizacja.

## Kryterium
Brak wycieku danych użytkownika, deterministyczne kontrakty API i kompletne testy ścieżek dokumentowych.
