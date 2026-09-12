# Audyt 162 — agents-voice

## Status
AUDYT ZAKOŃCZONY — framework LiveKit Agents dla serwerowych agentów głosowych/multimodalnych.

## Ustalenia
README opisuje STT/LLM/TTS, WebRTC, telekomunikację SIP, RPC/Data API, MCP, harmonogramowanie zadań, handoff wielu agentów i wbudowane testy. Wymaga kluczy LiveKit i providerów modeli.

## Ryzyka
Połączenia telefoniczne i agentowe działania zewnętrzne, prywatność audio/transkrypcji, sekrety, uprawnienia narzędzi MCP, koszty providerów i deterministyczność testów.

## Priorytet
WYSOKI.

## Kolejność prac
Kontrakty sesji → auth/sekrety → tool permissions → telephony guardrails → testy agentów → observability → lokalizacja.

## Kryterium zakończenia
Każde działanie konsekwentne ma autoryzację, log audytowy, test i bezpieczny mechanizm przerwania.
