# Plan pracy — krypton-byte.github.io

## Status
AUDYT ZAKOŃCZONY — szablon automatycznego portfolio GitHub.

## Stan faktyczny
README opisuje GitProfile: React + Vite, automatyczne pobieranie profilu GitHub, motywy, SEO, analitykę, projekty, doświadczenie i blog. Deployment opiera się na GitHub Actions/Pages.

## Ryzyka
GitHub API/rate limits; tokeny i uprawnienia; third-party analytics; SEO/config `base`; zależności frontendu; prywatność danych profilu.

## Priorytet
ŚREDNI.

## Kolejność prac
1. Zmapować źródła danych GitHub i konfigurację.
2. Ograniczyć token scopes i usunąć sekrety z klienta.
3. Przejrzeć analytics/consent i dostępność.
4. Aktualizacja Vite/dependencies.
5. Polska wersja treści i konfiguracji.

## Kryterium zakończenia
Bezpieczny deployment Pages, minimalne uprawnienia i poprawna lokalizacja.