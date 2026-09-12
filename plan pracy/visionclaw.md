# AUDYT 365 — visionclaw

## Status
Audyt wykonany. Aplikacja visionOS/Apple Vision Pro z postacią 3D, STT/TTS i mostem WebSocket do OpenClaw.

## Ustalenia
Swift/RealityKit/SwiftUI, Vision Pro, Bonjour discovery, WebSocket, SFSpeechRecognizer, AVSpeechSynthesizer i Python bridge. Stan interakcji jest modelowany jako state machine.

## Ryzyka
Mikrofon, lokalna sieć/Bonjour, WebSocket, zaufanie do Mac bridge, prywatność rozmów i aktualność protokołu.

## Plan prac
Zweryfikować TLS/uwierzytelnianie bridge, pairing urządzeń, uprawnienia mikrofonu, reconnect/timeout i ochronę danych głosowych. Następnie testy visionOS i lokalizacja.

## Kryterium zakończenia
Bezpieczny kanał Vision Pro↔Mac, testy concurrency/network i kontrola danych głosowych.
