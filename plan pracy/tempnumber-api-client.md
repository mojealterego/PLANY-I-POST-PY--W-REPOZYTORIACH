# Plan pracy — tempnumber-api-client

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: biblioteka PHP / klient API
- Priorytet: WYSOKI
- Gałąź: `master`

## Ustalenia
- Biblioteka udostępnia klienta PHP dla usługi Temp-Number.
- README opisuje saldo, tworzenie aktywacji, oczekiwanie na status SMS, ponawianie, historię aktywacji oraz listy usług/krajów.
- Token API jest przekazywany do konstruktora klienta.
- Kod dokumentacyjny pokazuje polling i ekstrakcję kodu OTP z odebranej wiadomości.
- Jest to biblioteka integracyjna, a nie samodzielna aplikacja.

## Ryzyka
1. Zależność od zewnętrznego API i jego kontraktu.
2. Obsługa tokenu wymaga bezpiecznej konfiguracji po stronie użytkownika biblioteki.
3. Polling wymaga timeoutu, backoffu i kontroli liczby żądań.
4. Dane numerów i wiadomości SMS mogą być danymi wrażliwymi; nie wolno logować ich bez potrzeby.
5. Dokumentacja zawiera przykłady związane z kodami weryfikacyjnymi; modernizacja powinna pozostać na poziomie bezpiecznej integracji API.

## Kolejność prac
1. Przeanalizować strukturę klas, enumów, wyjątków i transportu HTTP.
2. Wydzielić kontrakt API od implementacji transportu.
3. Dodać timeouty, kontrolowany retry/backoff i walidację odpowiedzi.
4. Dodać testy z mockowanym API i przypadkami błędów.
5. Zweryfikować kompatybilność PHP/Composer i wersjonowanie semantyczne.
6. Ograniczyć logowanie danych aktywacji i treści SMS.
7. Ujednolicić README, changelog i pełną polonizację dokumentacji.

## Kryterium zakończenia
Biblioteka ma stabilny kontrakt, testy bez zależności od zewnętrznego serwisu, kontrolowane błędy/timeouty i bezpieczne obchodzenie się z danymi aktywacji.
