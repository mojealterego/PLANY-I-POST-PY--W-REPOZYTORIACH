# Taluxi Open Source — plan

- **Audyt:** 298
- **Status:** audyt zakończony; edukacyjny system taxi: dwie aplikacje Flutter + dwa mikroserwisy Node/TypeScript.
- **Ustalenia:** modularne pakiety, auth, lokalizacja kierowców, VoIP, Firebase/Agora/OneSignal; README jawnie stwierdza brak gotowości produkcyjnej i ograniczone testy UI.
- **Ryzyka:** GPS i prywatność lokalizacji, VoIP, auth, klucze usług, wybór kierowcy oparty o Haversine zamiast sieci dróg/traffic.
- **Priorytet:** WYSOKI.
- **Kolejność:** auth → privacy/GPS → routing → VoIP/TLS → secrets → mobile tests → backend tests → deployment.
- **Kryterium:** poprawny routing, kontrola danych lokalizacyjnych, bezpieczne sekrety i pełna macierz testów Android/iOS.
- **Uwaga:** repo deklaruje charakter edukacyjny; nie traktować jako produkcyjne.
