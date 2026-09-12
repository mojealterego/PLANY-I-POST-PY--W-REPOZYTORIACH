# Audyt 165 — ShipinKit

## Status
AUDYT ZAKOŃCZONY — nieoficjalny Swift SDK do typed video-generation dla Runway i Luma.

## Ustalenia
README deklaruje Swift 6, Apple platforms, typed requests/responses, redagowane credentials, injectable transport, timeouts, polling, cancellation i offline fixtures. Repo rozdziela kontrakty providerów zamiast udawać ich pełną zgodność.

## Ryzyka
Zmiany kontraktów zewnętrznych API, sekrety w aplikacjach klienckich, tymczasowe URL-e wynikowe, koszty generacji i zgodność znaków towarowych/licencji.

## Priorytet
WYSOKI.

## Kolejność prac
Kontrakty API → testy fixtures → credential boundary → retry/timeout → storage outputów → CI dla platform Apple.

## Kryterium zakończenia
SDK posiada aktualne typowane kontrakty, testy bez live API i bezpieczne granice poświadczeń.
