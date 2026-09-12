# Resolver Stable Diffusion Client — plan

- **Audyt:** 280
- **Status:** audyt zakończony; aplikacja Android/Capacitor do zdalnego sterowania Forge/ComfyUI.
- **Ustalenia:** Android 10+, Vanilla JS + Capacitor, Java Foreground Service/Wake Lock, REST/WebSocket, inpainting, metadata, kolejka i lokalne/HTTPS połączenia.
- **Ryzyka:** CORS `*`, zdalny sygnał KILL, adresy hostów, Wake Lock/foreground service, zdalne backendy i lokalne dane.
- **Priorytet:** WYSOKI.
- **Kolejność:** 1) model zaufania i walidacja endpointów; 2) HTTPS/TLS; 3) ograniczenie CORS; 4) autoryzacja operacji zdalnych; 5) bezpieczne przechowywanie konfiguracji; 6) testy Android/Capacitor.
- **Kryterium zakończenia:** brak nieograniczonego zaufania do zdalnego hosta, testy połączeń i operacji uprzywilejowanych, reprodukowalny build.
- **Uwaga:** audyt nie oznacza gotowości produkcyjnej.
