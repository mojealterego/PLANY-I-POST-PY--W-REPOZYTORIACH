# Plan pracy — elevenlabs-swift-sdk

## Status
AUDYT ZAKOŃCZONY — SDK Swift do usług ElevenLabs.

## Stan faktyczny
Repozytorium ma około 1 MB i `main`. Należy zweryfikować API, modele danych, async/cancellation, transport i sposób przechowywania credentials.

## Ryzyka
- klucze API w aplikacjach klienckich;
- audio i prywatność;
- zmiany API dostawcy;
- kompatybilność Apple platforms.

## Priorytet
WYSOKI.

## Kolejność prac
1. API/transport.
2. Secure credential boundary.
3. Audio lifecycle i cancellation.
4. Fixtures/testy.
5. Polonizacja dokumentacji.

## Kryterium zakończenia
Bezpieczny kontrakt SDK i testy kompatybilności z aktualnym API.
