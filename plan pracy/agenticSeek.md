# Audyt 90 — agenticSeek

## Stan
AUDYT ZAKOŃCZONY — lokalny/autonomiczny agent z przeglądarką, kodowaniem i wieloma providerami LLM.

## Ustalenia
README deklaruje lokalne modele, web browsing, automatyczne uruchamianie kodu, Docker/SearXNG/Redis, integracje lokalne i chmurowe oraz konfigurację przez `.env` i `config.ini`. Projekt rekomenduje Python 3.10.x. Agent otrzymuje dostęp do wskazanego `WORK_DIR`.

## Ryzyka
- wykonywanie kodu i dostęp do filesystemu;
- automatyczna obsługa przeglądarki i formularzy;
- `stealth_mode` i zewnętrzne scraping endpoints wymagają ograniczeń zgodności;
- sekrety wielu providerów;
- Docker/Redis/SearXNG i localhost boundaries.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Sandbox wykonania → workspace allowlist → browser action policy → secret handling → provider isolation → network egress policy → session/audit → tests/e2e → release.

## Kryterium zakończenia
Agent nie wykonuje uprzywilejowanych działań poza zatwierdzonym workspace i listą narzędzi, a wszystkie operacje są audytowalne.