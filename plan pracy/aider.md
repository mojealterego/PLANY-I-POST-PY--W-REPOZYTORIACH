# Audyt 341 — aider

## Stan
AUDYT ZAKOŃCZONY — dojrzały agent pair-programming.

## Ustalenia
Aider działa w terminalu z lokalnymi i chmurowymi LLM, mapuje codebase, integruje Git i obsługuje wiele języków. Zmiany AI są zapisywane przez Git, co daje istotną ścieżkę odwracania.

## Ryzyka
Wykonywanie zmian w repozytoriach; klucze providerów; prompt injection z kodu; koszty modeli; automatyczne commity.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
Permission boundary → secrets → diff/approval → testy → obserwowalność.

## Kryterium zakończenia
Zmiany kodu są jawnie diffowane, testowane i odwracalne.