# Plan pracy — tempmail

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: Node.js CLI do tymczasowej poczty
- Priorytet: WYSOKI
- Gałąź: `main`

## Ustalenia
- Repozytorium zawiera `index.js`, `package.json`, `package-lock.json` i README.
- Pakiet nazywa się `trashx`, jest modułem ES i wystawia polecenie CLI.
- Zależności obejmują `cheerio` i `onesecmail`.
- Skrypt `test` jest celowo zakończony błędem i nie stanowi testów projektu.

## Ryzyka
1. Brak rzeczywistego zestawu testów.
2. Usługa zewnętrznej tymczasowej poczty jest zależnością krytyczną i może zmieniać API.
3. Parsowanie HTML przez Cheerio wymaga kontroli nieufnego wejścia.
4. Nazwa pakietu `trashx` nie odpowiada nazwie repozytorium i wymaga uporządkowania rebrandingu.

## Kolejność prac
1. Przeanalizować `index.js` i ustalić dokładny kontrakt CLI.
2. Wydzielić klienta usługi pocztowej, domenę wiadomości i interfejs CLI.
3. Dodać timeouty, retry z limitem, walidację odpowiedzi i czytelne błędy.
4. Zastąpić atrapę testu rzeczywistymi testami jednostkowymi i integracyjnymi.
5. Zablokować niebezpieczne logowanie danych wiadomości i danych kont.
6. Uporządkować nazwę pakietu, README i dokumentację po polsku.
7. Dodać CI oraz weryfikację publikacji pakietu.

## Kryterium zakończenia
CLI ma stabilny kontrakt, testy rzeczywiście wykonują asercje, błędy usług zewnętrznych są kontrolowane, a build/publikacja są powtarzalne.
