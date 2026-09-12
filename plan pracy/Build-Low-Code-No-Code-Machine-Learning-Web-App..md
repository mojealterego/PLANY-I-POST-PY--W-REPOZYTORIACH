# AURELIS ML Studio — plan

- **Audyt:** 296
- **Status:** audyt zakończony; Streamlit workspace do EDA, przygotowania danych i AutoML.
- **Ustalenia:** README opisuje CSV validation, profiling, cleaning, PyCaret CV, hold-out evaluation, tuning, finalization i eksport modelu/metadanych; limit uploadu 200 MB; historyczne piny były bardzo stare i wymagają aktualnego, kompatybilnego stosu.
- **Ryzyka:** upload danych, wykonywanie AutoML, serializacja modeli, zasoby pamięci/CPU oraz aktualność zależności.
- **Priorytet:** WYSOKI.
- **Kolejność:** dependency matrix → upload validation → resource limits → model artifact security → tests → deployment.
- **Kryterium:** reprodukowalny eksperyment, bezpieczne artefakty i aktualny kompatybilny runtime.
- **Uwaga:** audyt nie oznacza gotowości produkcyjnej.
