# ai-email-writer

## Status
AUDYT ZAKOŃCZONY — FastAPI + Streamlit + Groq.

## Stan faktyczny
Python 3.10+, FastAPI i Streamlit; backend oferuje health/options/generate-email, frontend wybiera ton i intencję. Konfiguracja używa `GROQ_API_KEY`; README przewiduje pytest i Ruff.

## Ryzyka
Brak potwierdzonej autoryzacji backendu i limitów. Dane treści wiadomości mogą zawierać PII. Domyślny model i API mogą się dezaktualizować.

## Priorytet
ŚREDNI/WYSOKI.

## Kolejność prac
1. Audyt endpointów i walidacji.
2. Rate limiting, timeouty i bezpieczne logowanie.
3. Ochrona sekretów i PII.
4. Testy API/UI.
5. Aktualizacja modelu/zależności i polonizacja.

## Kryterium zakończenia
Bezpieczne API, testy regresyjne, brak sekretów w repo oraz kontrola kosztów wywołań modelu.