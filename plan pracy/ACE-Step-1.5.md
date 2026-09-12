# ACE-Step-1.5 — plan

- **Audyt:** 290
- **Status:** audyt zakończony; repo modelu/generowania muzyki.
- **Ustalenia:** należy zweryfikować pipeline inferencji, wymagania GPU, modele/wagi, licencje oraz interfejsy wejścia/wyjścia.
- **Ryzyka:** ciężkie zależności ML, pobieranie modeli, provenance danych i koszt zasobów.
- **Priorytet:** WYSOKI.
- **Kolejność:** runtime → model registry/provenance → dependency pinning → resource limits → tests → packaging.
- **Kryterium:** reprodukowalna inferencja i jawnie udokumentowane pochodzenie/licencje modeli.
