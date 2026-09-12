# Plan pracy — ZeroAI

## Status
AUDYT ZAKOŃCZONY — eksperymentalny agent AI dla Androida.

## Stan faktyczny
Kotlin 2.0, Jetpack Compose, Rust i UniFFI. Długowieczny runtime, Gemma przez LiteRT-LM, providerzy chmurowi/lokalni, Telegram, Discord, Messages, Terminal, pamięć, harmonogram, pluginy i sandbox Rhai. Android zarządza UX, sekretami i lifecycle; Rust runtime i wykonaniem.

## Ryzyka
Długowieczne wykonywanie agenta, shell/SSH, kanały zewnętrzne, pluginy, sekrety, pobieranie modeli, FFI Kotlin↔Rust i uprawnienia Android.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Capability i permission matrix.
2. Sandbox Rhai i granice procesu.
3. Sekrety, SSH i kanały.
4. Foreground service, concurrency i lifecycle.
5. Provenance/integralność modeli.
6. Testy Gradle, detekt, spotless i urządzeniowe.
7. Polonizacja i rebranding.

## Kryterium zakończenia
Każda operacja zewnętrzna ma jawne uprawnienie, limit i ścieżkę audytową; FFI, storage, modele i lifecycle są zweryfikowane na urządzeniach.