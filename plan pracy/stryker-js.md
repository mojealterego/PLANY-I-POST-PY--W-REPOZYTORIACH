# stryker-js — plan

- **Audyt:** 297
- **Status:** audyt zakończony; duży ekosystem JavaScript/TypeScript do mutation testing.
- **Ustalenia:** istotne są runnerzy, pluginy, parsery, konfiguracja i kompatybilność Node/TS.
- **Ryzyka:** wykonywanie testów z kodem użytkownika, pluginy, izolacja procesów i duży graf zależności.
- **Priorytet:** WYSOKI / REFERENCYJNY.
- **Kolejność:** workspace → packages → runners → process isolation → tests → release.
- **Kryterium:** stabilne mutation testing bez niejawnego rozszerzania uprawnień procesu testowego.
