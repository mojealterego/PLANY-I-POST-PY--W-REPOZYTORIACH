# Plan pracy — elevenlabs-android

## Status
AUDYT ZAKOŃCZONY — oficjalny SDK ElevenAgents dla Android/Kotlin.

## Stan faktyczny
README opisuje audio-first sesje LiveKit/WebRTC, text-only WebSocket, agentów public/private, typed events, data channel, feedback i sterowanie mikrofonem. SDK wymaga jawnego RECORD_AUDIO dla voice; część uprawnień LiveKit można usuwać z manifestu.

## Ryzyka
sekrety/tokeny agentów; uprawnienia mikrofonu; WebRTC/media; lifecycle sesji; prywatność transkrypcji/audio; zgodność Android SDK; błędna ekspozycja publicznych agentów.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zweryfikować model credentiali public/private.
2. Audyt manifestu i minimalnych permissions.
3. Testy lifecycle, reconnect, audio focus i błędów sieci.
4. Ochrona logów i danych audio.
5. Polska dokumentacja integracyjna.

## Kryterium zakończenia
Minimalne uprawnienia, bezpieczny credential flow i testy urządzeniowe dla voice/text.