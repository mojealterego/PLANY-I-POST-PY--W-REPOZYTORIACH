# Audyt 79 — MATS-Grants

## Stan
AUDYT ZAKOŃCZONY — dossier badawcze + uruchamialny syntetyczny vertical slice.

## Ustalenia
README pokazuje rozdzielenie tezy badawczej od implementacji: efekt behawioralny → sygnał predykcyjny → interwencja przyczynowa → odporność → znaczenie bezpieczeństwa. Repo zawiera CI, `configs`, `docs`, `scripts`, `src/mats_research`, testy i `pyproject.toml`. Projekt używa Python >=3.10, numpy/pandas/scikit-learn/PyYAML oraz pytest. Demonstrator nie łączy się z systemami zewnętrznymi.

## Ryzyka
- należy zachować granicę między prototypem syntetycznym a twierdzeniami o realnym schemingu;
- dokumentacja aplikacyjna ma własne ograniczenia integralności, które trzeba utrzymywać;
- wyniki naukowe wymagają reprodukcji i kontroli statystycznych.

## Priorytet
WYSOKI — wartość badawcza i infrastrukturalna.

## Kolejność prac
Reprodukcja CI/demo → testy statystyczne → konfiguracja eksperymentów → negative controls → dokumentacja provenance/evidence → polonizacja techniczna.

## Kryterium zakończenia
Każda metryka ma test/seed/proweniencję, demo jest reprodukowalne, a claims są wyraźnie oddzielone od obserwacji eksperymentalnych.