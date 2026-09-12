# WDA Photo Agent — plan pracy

## Status
AUDYT ZAKOŃCZONY — implementacja niezweryfikowana produkcyjnie.

## Stan faktyczny
Repozytorium zawiera mobilny rdzeń Wirtualnego Dyrektora Artystycznego: Next.js/React/TypeScript, analizę obrazu przez OpenAI Responses API, Structured Output, adapter Adobe Firefly, server-side OAuth oraz konfigurację CI/Vercel. README opisuje pipeline SOURCE → ANALYZE → ART DIRECT → EXECUTE → VERIFY oraz jawnie oddziela diagnozę, receptę i wykonanie.

## Ryzyka
- zależność od kontraktów OpenAI/Adobe i wersji API;
- sekrety OAuth muszą pozostać wyłącznie po stronie serwera;
- operacje edycyjne wymagają walidacji adapterów i błędów asynchronicznych;
- brak dowodu z audytu na pełną walidację Photoshop API v2.

## Priorytet
WYSOKI

## Kolejność prac
1. Zmapować komponenty, route handlers, manifest i workflow CI.
2. Zweryfikować kontrakty OpenAI/Firefly i obsługę timeoutów/retry.
3. Dodać testy kontraktowe i integracyjne dla pipeline'u.
4. Uporządkować konfigurację sekretów i obserwowalność.
5. Dopiero potem polonizacja/rebranding i deployment produkcyjny.

## Kryterium zakończenia
Build, testy, lint, bezpieczeństwo sekretów i integracje API potwierdzone automatycznie; brak statusu produkcyjnego przed walidacją end-to-end.
