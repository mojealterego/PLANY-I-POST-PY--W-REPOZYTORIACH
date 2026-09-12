# Audyt 91 — cli

## Stan
AUDYT ZAKOŃCZONY — ElevenLabs CLI / Agents as Code.

## Ustalenia
README opisuje pełny dostęp do API oraz zarządzanie agentami z plików konfiguracyjnych, push/pull, branches, tools, tests, data residency i UI components. Projekt jest generowany z OpenAPI przez Fern, z ręcznie utrzymywaną warstwą workflow. Testy obejmują framework, wire mocks, workflow i opt-in live E2E. README wyraźnie wymaga osobnego konta testowego dla E2E.

## Ryzyka
- operacje `push/delete/update` mogą modyfikować zdalne zasoby;
- API keys i `.env`;
- `ELEVENLABS_INSECURE=1` musi pozostać trybem wyłącznie developerskim;
- `--base-url` i proxy zwiększają znaczenie walidacji endpointów;
- generowane SDK mogą zmieniać się wraz z OpenAPI.

## Priorytet
WYSOKI.

## Kolejność prac
Auth/secrets → endpoint allowlist → dry-run semantics → destructive action confirmations → generated/manual boundary → mock tests → dedicated E2E account → release verification.

## Kryterium zakończenia
Operacje destrukcyjne są jawne, testowalne i nie uruchamiają przypadkowego production E2E; regeneracja z OpenAPI jest reprodukowalna.