# Plan pracy — citibank-van

## Status
AUDYT ZAKOŃCZONY — historyczny, nieoficjalny klient Citibank VAN.

## Stan faktyczny
README opisuje Node.js CLI/API do logowania i obsługi virtual account numbers oraz procesu 2FA. Dokumentacja zawiera przykładowe przekazywanie username/password i operacje na danych kart.

## Ryzyka
obsługa danych finansowych i credentials; zgodność z aktualnym API banku; możliwe nieaktualne mechanizmy; 2FA; brak podstaw do uznania za produkcyjnie bezpieczny.

## Priorytet
KRYTYCZNY — ze względu na dane finansowe.

## Kolejność prac
1. Nie używać realnych danych finansowych w testach.
2. Zmapować aktualność protokołu/API.
3. Usunąć przykłady zachęcające do przechowywania haseł w kodzie/logach.
4. Dodać mock banku i testy bez sieci.
5. Oznaczyć projekt jako historyczny, jeśli API jest nieaktualne.

## Kryterium zakończenia
Brak realnych sekretów w testach, bezpieczny mock i jednoznaczny status kompatybilności.