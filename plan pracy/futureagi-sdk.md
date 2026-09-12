# Audyt 78 — futureagi-sdk

## Stan
AUDYT ZAKOŃCZONY — SDK do ewaluacji, obserwowalności i optymalizacji systemów AI.

## Ustalenia
README deklaruje Python i TypeScript/JavaScript, dataset management, prompt versioning, RAG/knowledge base, ewaluacje, guardrails, symulacje i OpenTelemetry. Dokumentacja pokazuje użycie kluczy `FI_API_KEY`/`FI_SECRET_KEY` oraz integracje z wieloma dostawcami modeli. Nie odnaleziono standardowego `pyproject.toml` ani `setup.py` pod wskazanymi ścieżkami, więc system pakowania wymaga dalszego zlokalizowania.

## Ryzyka
- przechowywanie i przesyłanie danych ewaluacyjnych oraz dokumentów RAG;
- klucze API i dane telemetryczne;
- deklaracje wydajności/latencji wymagają reprodukcji;
- kompatybilność Python/Node oraz wersjonowanie obu SDK.

## Priorytet
WYSOKI.

## Kolejność prac
Mapowanie pakietów → kontrakty API → auth/sekrety → testy deterministyczne ewaluacji → upload/RAG → telemetry → macierz dostawców → publikacja i polonizacja.

## Kryterium zakończenia
Oba SDK mają reprodukowalny build, testy kontraktowe, kontrolę sekretów i jawnie zweryfikowane granice danych.