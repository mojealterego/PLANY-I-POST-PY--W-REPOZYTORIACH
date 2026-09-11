# Plan pracy — PaulaA

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: aplikacja Kivy/Python + Google Gemini
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- Repozytorium zawiera `.replit`, `README.md`, `main.py` i `requirements.txt`.
- `main.py` implementuje prosty interfejs Kivy oraz wywołanie `google.generativeai` z modelem Gemini.
- Klucz API jest wpisany jako jawny placeholder w kodzie i nie może być podstawą produkcyjnej konfiguracji.
- Komunikacja z modelem jest synchroniczna w obsłudze zdarzenia UI, co grozi blokowaniem interfejsu.
- Brak widocznych testów, walidacji wejścia, warstwy konfiguracji, obsługi timeoutów i CI.

## Ryzyka
1. Sekret/konfiguracja API znajduje się w kodzie źródłowym.
2. Brak izolacji domeny, infrastruktury AI i UI.
3. Brak kontroli błędów poza ogólnym komunikatem.
4. Brak testów i potwierdzonego procesu budowania mobilnego.

## Kolejność prac
1. Przenieść konfigurację do bezpiecznego mechanizmu ustawień/zmiennych środowiskowych.
2. Oddzielić UI, przypadek użycia rozmowy, klienta Gemini i konfigurację.
3. Wprowadzić asynchroniczną obsługę żądań, timeouty i bezpieczne anulowanie.
4. Dodać walidację wejścia, limity i diagnostykę bez ujawniania sekretów.
5. Dodać testy jednostkowe/integracyjne i pipeline CI.
6. Zweryfikować docelową platformę i pakowanie Kivy.
7. Wykonać pełną polonizację dokumentacji i stabilizację marki Paula.

## Kryterium zakończenia
Aplikacja działa bez sekretów w kodzie, UI nie blokuje się podczas zapytań, warstwy są rozdzielone, testy przechodzą, a build docelowej platformy jest powtarzalny.
