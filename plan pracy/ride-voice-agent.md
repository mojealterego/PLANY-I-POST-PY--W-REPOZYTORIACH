# Ride Voice Agent — plan pracy

## Status
AUDYT ZAKOŃCZONY — demonstrator z rozbudowanymi guardrails, nie produkcyjny backend przewozowy.

## Stan faktyczny
Lokalny agent głosowy LiveKit dla inbound ride booking. Pipeline wykorzystuje Deepgram STT/TTS, Gemini/Vertex, Silero VAD i PostgreSQL. README opisuje potwierdzanie geokodowania, źródłowe narzędzia dla taryf/ETA, unieważnianie quote po zmianie adresu, OTP, idempotentne zapisy oraz brak PAN/CVV w bazie. Dostępne są testy pytest, Ruff i opcjonalne testy integracyjne Docker/Postgres.

## Ryzyka
- płatności i rezerwacje są operacjami wysokiego wpływu;
- demo używa stałego OTP i symulatora płatności;
- telekomunikacja wymaga zgodności z jurysdykcją, nagrywaniem i transferem;
- dane rozmów wymagają redakcji i retencji.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Zweryfikować strukturę agenta, API tools, bazę i testy.
2. Wymienić stuby na autoryzowane integracje dopiero za istniejącymi guardrails.
3. Dodać redakcję transkryptów, rate limiting, sekrety i audyt.
4. Przetestować idempotencję, webhooki i failure modes.
5. Dopiero potem przygotować polonizację/rebranding.

## Kryterium zakończenia
Testy jednostkowe/integracyjne, bezpieczne płatności/webhooki, zgodność prywatności i deterministyczne zabezpieczenia przed przypadkową rezerwacją.
