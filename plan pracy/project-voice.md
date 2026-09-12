# Project VOICE

## Status
AUDYT ZAKOŃCZONY — eksperymentalne narzędzie dostępnościowe.

## Stan faktyczny
Aplikacja webowa wykorzystująca Gemini do predykcji słów/zdań dla osób z trudnościami w mówieniu lub pisaniu. README wskazuje Node.js, Python, Google App Engine, lit-localize, Storybook i Secret Manager. Autorzy deklarują wprost, że projekt demonstracyjny nie jest produkcyjny.

## Ryzyka
Przetwarzanie potencjalnie wrażliwych treści i PII; zależność od API generatywnego; koszty/billing GCP. Należy zachować dostępność, prywatność i ograniczenia modelu.

## Priorytet
WYSOKI.

## Kolejność prac
1. Audyt aplikacji i backendu.
2. Weryfikacja sekretów, CSRF, logów i PII.
3. Testy dostępności i lokalizacji.
4. Aktualizacja zależności i deploymentu.
5. Polonizacja interfejsu bez pogorszenia WCAG.

## Kryterium zakończenia
Testowalna aplikacja z kontrolą danych, sekretów i kosztów; dokumentacja jasno oddziela demo od produkcji.