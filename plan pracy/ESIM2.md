# ESIM2 — plan pracy

## Stan audytu
**AUDYT ZAKOŃCZONY — repozytorium referencyjne ML/NLI.**

## Ustalenia
- Implementacja modelu Enhanced Sequential Inference Model dla natural language inference w PyTorch.
- Projekt jest powiązany z pracą magisterską autora i ma charakter badawczo-referencyjny.
- README opisuje pobieranie SNLI/MultiNLI/BNLI, preprocessing, trening i testowanie oraz podaje historyczne wyniki.
- `setup.py` deklaruje pakiet ESIM 1.0.1 oraz zależności: torch, numpy, nltk, matplotlib, tqdm, wget.
- Workflow oparty jest na starszym modelu dystrybucji i nie przedstawia współczesnej macierzy kompatybilności ani widocznego CI.

## Ryzyka
1. Stary stos packagingu i potencjalna niezgodność z aktualnymi wersjami PyTorch/Pythona.
2. Wyniki benchmarków są historyczne i wymagają reprodukcji przed użyciem jako aktualne.
3. Pobieranie danych z zewnętrznych źródeł wymaga kontroli integralności, licencji i wersji datasetów.
4. Brak potwierdzonego współczesnego CI/reprodukowalnego środowiska.

## Plan
1. Ustalić docelową wersję Python/PyTorch i zbudować zamrożone środowisko.
2. Zmodernizować packaging do `pyproject.toml` bez zmiany wyników modelu.
3. Dodać testy jednostkowe tensorów, maskowania, attention i forward pass.
4. Dodać test reprodukcji wyników na małym fixture dataset.
5. Oddzielić kod eksperymentalny od pipeline'u reprodukowalnego.
6. Zweryfikować licencje/proweniencję datasetów i checkpointów.
7. Dodać CI dla lint/test/smoke training.
8. Przygotować pełną polską dokumentację i dopiero potem rozważyć rebranding.

## Kryterium zakończenia
Instalowalne środowisko, deterministyczny smoke test, testy modelu, reprodukowalny pipeline danych i udokumentowana kompatybilność. Audyt nie oznacza produkcyjnej gotowości.
