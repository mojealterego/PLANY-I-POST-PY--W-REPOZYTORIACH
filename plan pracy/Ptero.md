# AUDYT 358 — Ptero

## Status
Audyt wykonany. Ptero to darmowy wielomodelowy czat AI z frontendem JavaScript/HTML/CSS i integracją WordPress/PHP.

## Ustalenia
README deklaruje lokalne przechowywanie rozmów w przeglądarce, brak konta, wiele modeli i możliwość osadzenia jako plugin WordPress.

## Ryzyka
Bezpieczeństwo kluczy/API, prywatność lokalnego storage, zależność od zewnętrznych providerów, bezpieczeństwo shortcode/pluginu WordPress i aktualizacji.

## Plan prac
Zmapować kod, endpointy i plugin, sprawdzić storage/CSP/CORS, obsługę sekretów, sanitizację treści i testy. Następnie polonizacja i hardening.

## Kryterium zakończenia
Zweryfikowany transport, storage, plugin WordPress i polityka sekretów.
