# Plan pracy — lonlybot

## Status
AUDYT ZAKOŃCZONY — aplikacja webowa AI companion.

## Stan faktyczny
Next.js 16, Tailwind, Framer Motion, Zustand z localStorage oraz integracje Gemini/OpenAI/Anthropic/OpenRouter. Aplikacja posiada chat, avatary, konfigurację osobowości i historię rozmów.

## Ryzyka
Klucze API, prywatne rozmowy i pamięć lokalna, wielo-providerowa warstwa AI, dane wrażliwe oraz niejasna granica między lokalnym UI a backendowym proxy API.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować API route i przepływ sekretów.
2. Oddzielić dane użytkownika od konfiguracji aplikacji.
3. Zweryfikować storage, usuwanie historii i eksport.
4. Dodać walidację wejścia, rate limits i testy.
5. Uporządkować provider abstraction.
6. Polonizacja UI i rebranding.

## Kryterium zakończenia
Żaden sekret dostawcy nie trafia do klienta, dane rozmów mają kontrolowaną retencję, a każdy provider jest testowalny przez wspólny kontrakt.