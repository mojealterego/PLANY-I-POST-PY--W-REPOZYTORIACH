# llama.cpp — plan

- **Audyt:** 292
- **Status:** audyt zakończony; duży projekt lokalnego runtime inferencji modeli LLM.
- **Ustalenia:** kluczowe są backendy CPU/GPU, formaty modeli, serwer API, bindings, build system i testy platformowe.
- **Ryzyka:** natywne komponenty C/C++, pamięć, modele użytkownika, sieć serwera oraz kompatybilność binarna.
- **Priorytet:** KRYTYCZNY / REFERENCYJNY.
- **Kolejność:** build matrix → backendy → API → memory/resource limits → fuzz/tests → packaging.
- **Kryterium:** reprodukowalny build, testy regresji i jawnie kontrolowana ekspozycja serwera/API.
