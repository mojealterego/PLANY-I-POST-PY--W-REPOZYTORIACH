# Email-Generation — plan

- **Audyt:** 282
- **Status:** audyt zakończony; narzędzie Python do tymczasowych skrzynek i ekstrakcji OTP.
- **Ustalenia:** requests/BeautifulSoup; generowanie wielu skrzynek, polling, regex OTP 4–6 cyfr, izolacja sesji/cookies.
- **Ryzyka:** automatyzacja usług disposable mail, dane wiadomości, cookies, OTP oraz zależność od zmian stron dostawców.
- **Priorytet:** WYSOKI.
- **Kolejność:** walidacja wejścia → prywatność/retencja → ograniczenie automatyzacji → testy parsera → obsługa błędów/rate limitów → dokumentacja zgodności.
- **Kryterium:** testowalny klient bez obchodzenia zabezpieczeń usług i bez przechowywania sekretów/danych ponad niezbędny zakres.
- **Uwaga:** audyt nie oznacza gotowości produkcyjnej.
