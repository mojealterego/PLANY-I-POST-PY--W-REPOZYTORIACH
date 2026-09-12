# Plan pracy — ai-email-generator-2

## Status
AUDYT ZAKOŃCZONY — mała aplikacja React/Vite + Express/Supabase/LLM.

## Stan faktyczny
README opisuje responsywny frontend React/Ant Design/Zustand oraz backend Express z Supabase Auth i API modelu. Konfiguracja przewiduje klucze Supabase, AI oraz limit dzienny.

## Ryzyka
`SUPABASE_SERVICE_ROLE_KEY`; klucze AI; auth/session; prompt injection; limity i koszty; brak potwierdzonej macierzy testów; niejasna jakość aktualnych endpointów.

## Priorytet
ŚREDNI/WYSOKI.

## Kolejność prac
1. Zmapować frontend/backend i endpointy.
2. Zweryfikować service-role tylko po stronie serwera.
3. Dodać walidację wejścia, rate limit i limity kosztowe.
4. Testy auth/API i mock LLM.
5. Polska lokalizacja UI i dokumentacji.

## Kryterium zakończenia
Sekrety wyłącznie server-side, bezpieczne auth, testy API i kontrolowany koszt generacji.