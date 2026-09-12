# Plan pracy — ChatGPT-CodeReview

## Stan audytu
- **Audyt:** zakończony
- **Klasyfikacja:** aplikacja Probot/GitHub Action do automatycznego code review
- **Priorytet:** WYSOKI
- **Produkcja:** NIE

## Ustalenia
Repozytorium zawiera bota do automatycznego przeglądu zmian w Pull Requestach. README opisuje wdrożenie jako AWS Lambda oraz GitHub Actions, a także możliwość self-hostingu przez Node/Probot. `package.json` definiuje Node >=18, Probot, adaptery AWS Lambda/GitHub Actions, OpenAI SDK, Next, minimatch, Rollup, ncc, Jest i TypeScript. Skrypt `build` buduje aplikację i GitHub Action, a `build:lambda` wariant Lambda.

## Ryzyka / luki
1. README jest historyczne i zawiera konfiguracje modeli/usług, które należy zweryfikować przed ponownym użyciem.
2. `package.json` ma `homepage` ustawione na `https://github.com//`, co jest błędną metadanymi projektu.
3. Dokumentacja zawiera instrukcje używające szerokich uprawnień GitHub Actions; należy ograniczyć permissions do minimum potrzebnego do publikacji review.
4. Należy zweryfikować bezpieczeństwo webhooków, instalacji Probot, tokenów i obsługi sekretów.
5. OpenAI API endpoint/model configuration wymaga aktualnego kontraktu i testów kompatybilności.
6. Brak potwierdzenia aktualnego CI/build/test w tej sesji; nie wolno uznawać projektu za produkcyjny na podstawie samego README.

## Kolejność prac
1. Zmapować `src/`, konfigurację Probot, GitHub Action, Lambda i testy.
2. Zweryfikować eventy PR, zakres pobieranych diffów i filtrowanie plików.
3. Utwardzić permissions GitHub App/Actions i granice sekretów.
4. Dodać testy kontraktowe dla webhooków, dużych diffów, błędów API i retry.
5. Zweryfikować limity kosztów, długości patcha, timeouty i rate limiting.
6. Uaktualnić SDK/model API oraz usunąć nieaktualne instrukcje.
7. Naprawić metadane pakietu i ustabilizować build Node 18+.
8. Uruchomić testy, build Action i wariant Lambda w CI.
9. Wykonać rebranding i pełną polonizację własnych materiałów.

## Kryterium zakończenia
Bot musi mieć zweryfikowany przepływ PR → analiza → komentarz, minimalne uprawnienia, bezpieczne sekrety, ograniczenia kosztów oraz powtarzalne testy/build. Audyt nie oznacza gotowości produkcyjnej.
