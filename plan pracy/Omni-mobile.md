# Audyt 340 — Omni-mobile

## Stan
AUDYT ZAKOŃCZONY — Android/Jetpack Compose prototyp.

## Ustalenia
Build oparty o Kotlin/Android Compose, compile/target SDK 35, min SDK 26, OkHttp WebSocket i coroutines. Adres WebSocket ma domyślnie `ws://10.0.2.2:8000/ws`, czyli kanał developerski/emulatorowy.

## Ryzyka
Nieszyfrowany WebSocket; konfiguracja endpointu przez Gradle; brak produkcyjnego TLS/auth potwierdzonego w README.

## Priorytet
WYSOKI.

## Kolejność prac
TLS/WSS → auth → konfiguracja endpointu → lifecycle WebSocket → testy.

## Kryterium zakończenia
Brak plain-text transportu w produkcji i zweryfikowana autoryzacja.