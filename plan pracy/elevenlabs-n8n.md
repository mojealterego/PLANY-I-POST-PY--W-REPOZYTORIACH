# Audyt 272 — elevenlabs-n8n

## Status
AUDYT ZAKOŃCZONY — integracja ElevenLabs z n8n.

## Ustalenia
Mały projekt integracyjny; wymagane jest sprawdzenie node definitions, credential handling, wersji n8n i kontraktów ElevenLabs.

## Ryzyka
Sekrety n8n, dane audio, webhook/tool execution, kompatybilność API i supply chain.

## Priorytet
WYSOKI.

## Kolejność prac
Credentials → node contracts → validation → tests → package/release.

## Kryterium zakończenia
Credential fields są bezpieczne, operacje walidowane, a node ma testy kontraktowe.
