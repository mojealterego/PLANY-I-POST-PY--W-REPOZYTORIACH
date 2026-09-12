# graphiti — plan

- **Audyt:** 295
- **Status:** audyt zakończony; system grafowej pamięci/knowledge graph dla agentów.
- **Ustalenia:** kluczowe obszary to model danych, czasowość relacji, ingest, wyszukiwanie i integracja z agentami.
- **Ryzyka:** izolacja danych, prompt/data injection, retencja, spójność grafu i koszty zapytań.
- **Priorytet:** WYSOKI.
- **Kolejność:** schema → ingest → retrieval → tenant isolation → security → performance → tests.
- **Kryterium:** deterministyczne testy zapisu/odczytu i szczelna separacja danych kontekstowych.
