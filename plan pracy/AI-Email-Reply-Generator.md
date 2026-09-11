# Plan pracy — AI-Email-Reply-Generator

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: full-stack AI web app
- Priorytet: WYSOKI
- Gałąź: `main`

## Ustalenia
- Frontend: React + Vite.
- Backend: FastAPI z modułami `main.py`, `routes.py`, `models.py`, `services.py`, `prompts.py`.
- Integracja generowania: Google Gemini; fallback lokalny pozwala uruchomić aplikację bez klucza.
- README deklaruje endpointy generowania zwykłego i strumieniowego oraz wdrożenie frontend Vercel/backend Render.
- Plan rozwoju obejmuje uwierzytelnianie, historię, wiele modeli, integracje pocztowe i adaptację stylu.

## Ryzyka
1. Brak potwierdzonych testów jednostkowych, API i E2E w dokumentacji.
2. Konfiguracja adresu backendu wymaga spójnego modelu środowisk.
3. Dane treści wiadomości są wrażliwe i wymagają polityki retencji oraz logowania bez treści.
4. Integracje Gmail/Outlook powinny być projektowane z minimalnymi uprawnieniami.

## Kolejność prac
1. Zmapować aktualny kod frontendu/backendu i kontrakty HTTP.
2. Wydzielić warstwy domeny, aplikacji, infrastruktury i prezentacji.
3. Ustandaryzować konfigurację i walidację zmiennych środowiskowych.
4. Dodać testy API, generowania, fallbacku i obsługi błędów.
5. Dodać limity, ochronę przed nadużyciem i redakcję logów.
6. Zaprojektować bezpieczne integracje pocztowe dopiero po stabilizacji rdzenia.
7. Polonizować UI/dokumentację i zweryfikować build/deploy.

## Kryterium zakończenia
Frontend i backend mają stabilne kontrakty, testy przechodzą, sekrety nie trafiają do repozytorium ani logów, a wdrożenia są powtarzalne.
