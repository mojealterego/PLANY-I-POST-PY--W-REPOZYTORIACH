# Text-To-Video-API

## Status
AUDYT ZAKOŃCZONY — cienki klient API do generacji wideo.

## Stan faktyczny
Python/requests wywołuje zewnętrzne API Vadoo przez klucz w nagłówku. Parametry obejmują temat, głos, motyw, język i czas trwania; wynik dostarczany jest przez webhook.

## Ryzyka
Sekret API, webhooki, niezaufane URL-e zwrotne, koszty i zależność od zewnętrznego API. Dokumentacja używa historycznych nazw modeli/usług i wymaga weryfikacji.

## Priorytet
WYSOKI.

## Kolejność prac
1. Dodać konfigurację sekretów poza kodem.
2. Walidować webhooki i podpisy/autoryzację.
3. Timeouty, retry z backoffem i idempotencja.
4. Testy z mockiem API.
5. Polonizacja dokumentacji.

## Kryterium zakończenia
Bezpieczny klient API z ochroną sekretu, walidacją webhooków i testami regresyjnymi.