# emailnator-tempmail

## Status
AUDYT ZAKOŃCZONY — prosty klient CLI tymczasowej poczty.

## Stan faktyczny
Node.js CLI generuje adres tymczasowy i pobiera listę/treść wiadomości. README wskazuje axios, tough-cookie i axios-cookiejar-support oraz bezpośrednie żądania do Emailnator. Dokumentacja przyznaje użycie nagłówków imitujących przeglądarkę.

## Ryzyka
Rate limiting, zmienność niepublicznego zachowania usługi, prywatność wiadomości i możliwość nadużycia. Należy unikać obchodzenia zabezpieczeń/usługowych ograniczeń.

## Priorytet
ŚREDNI/WYSOKI.

## Kolejność prac
1. Zweryfikować kod HTTP i obsługę błędów.
2. Usunąć zależności od spoofingu tam, gdzie nie są konieczne.
3. Dodać limity, timeouty i bezpieczne logowanie.
4. Testy jednostkowe z mockami.
5. Polonizacja dokumentacji.

## Kryterium zakończenia
CLI działa zgodnie z publicznym interfejsem usługi, nie omija ograniczeń, nie wycieka treści i ma testy regresyjne.