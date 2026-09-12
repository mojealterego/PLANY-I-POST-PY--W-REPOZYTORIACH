# traceAI — plan pracy

## Status
AUDYT ZAKOŃCZONY — biblioteka obserwowalności, wymaga weryfikacji kontraktów.

## Stan faktyczny
Projekt OpenTelemetry-native dla obserwowalności aplikacji AI, z deklarowanym wsparciem Python/TypeScript/Java/C# i wieloma integracjami LLM/agentów. README pokazuje osobne pakiety/instrumentory i architekturę opartą o trace/span attributes.

## Ryzyka
- telemetry może zawierać prompty, completion i dane wejściowe użytkowników;
- kompatybilność wielu języków/frameworków wymaga macierzy CI;
- przykłady zawierają klucze jako placeholdery i muszą pozostać wyłącznie konfiguracją środowiskową;
- wersje semantycznych konwencji OTel trzeba kontrolować.

## Priorytet
WYSOKI

## Kolejność prac
1. Zmapować pakiety, manifesty i macierze CI.
2. Zweryfikować redakcję PII/secrets przed eksportem spanów.
3. Testy kompatybilności dla głównych providerów.
4. Benchmark overhead i stabilność streamingu/error handling.
5. Polonizacja dokumentacji i rebranding warstwy użytkowej.

## Kryterium zakończenia
Powtarzalne buildy wszystkich obsługiwanych języków, testy instrumentacji oraz udokumentowana polityka prywatności telemetry.
