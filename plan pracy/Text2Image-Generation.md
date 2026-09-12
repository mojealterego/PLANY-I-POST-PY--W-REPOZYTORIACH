# Text2Image-Generation — plan pracy

## Stan audytu
**AUDYT ZAKOŃCZONY — aplikacja/projekt eksperymentalny generowania obrazów.**

## Ustalenia
- Brak dostępnego `README.md` na domyślnej gałęzi w chwili audytu.
- `requirements.txt` wskazuje szeroki stos: PyTorch, torchvision, TensorFlow, Transformers, NLTK, Flask, Gunicorn, OpenCV, Pydantic, pytest oraz narzędzia formatowania.
- Obecny manifest jest nieprecyzyjny: zależności nie mają wersji, a zakres funkcjonalny nie jest formalnie opisany.

## Ryzyka
1. Brak wersjonowania zależności utrudnia reprodukcję.
2. Niejasny kontrakt API/modelu i brak README utrudniają ocenę architektury.
3. Duża liczba ciężkich frameworków zwiększa koszt środowiska i powierzchnię zależności.
4. Brak potwierdzonego CI i pokrycia testami.

## Plan
1. Zmapować faktyczny kod, entrypointy, model i pipeline inferencji.
2. Zdefiniować kontrakt wejścia/wyjścia oraz wersję modelu.
3. Przejść na deterministyczne, przypięte zależności i izolowane środowisko.
4. Dodać testy preprocessingu, inferencji i API.
5. Dodać limity rozmiaru wejścia, czasu i pamięci oraz walidację Pydantic.
6. Uporządkować Flask/WSGI i ścieżkę wdrożenia.
7. Dodać CI lint/test/smoke.
8. Utworzyć pełny polski README i dokumentację modelu/licencji.

## Kryterium zakończenia
Udokumentowany pipeline text→image, powtarzalna instalacja, test inferencji i API oraz zweryfikowany build. Nie oznaczać produkcji bez testów zasobowych i bezpieczeństwa.
