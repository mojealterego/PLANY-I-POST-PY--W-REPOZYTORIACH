# n8n-nodes-futureagi — plan pracy

## Status
AUDYT ZAKOŃCZONY — integracja n8n.

## Stan faktyczny
Community node dla Future AGI obsługujący pobieranie promptów, logowanie wykonań, ewaluacje i ochronę treści. README deklaruje retry, batch processing, wiele środowisk oraz konfigurację API key/secret/base URL.

## Ryzyka
- przesyłanie promptów, outputów i PII do zewnętrznego API;
- retry/batch mogą zwielokrotniać koszty i skutki uboczne;
- konfiguracje przykładowe muszą być jednoznacznie demo-only.

## Priorytet
WYSOKI

## Kolejność prac
1. Zweryfikować package.json, credentials, node definitions i testy.
2. Sprawdzić timeouty, retry i idempotencję.
3. Dodać redakcję/zasady danych wrażliwych.
4. Testy n8n i kompatybilności wersji.
5. Polonizacja/rebranding.

## Kryterium zakończenia
Bezpieczne credentials, testy operacji synchronicznych/asynchronicznych i kontrolowane retry.
