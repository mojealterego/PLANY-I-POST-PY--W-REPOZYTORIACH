# Plan pracy — PyPhone

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: eksperymentalna aplikacja VoIP/PyQt
- Priorytet: WYSOKI
- Status produkcyjny: NIE

## Ustalenia
README deklaruje Python/PyQt5, MySQL, PyAudio i tunelowanie przez ngrok. Kod `PyPhone.py` otwiera lokalny socket TCP, uruchamia ngrok, pobiera publiczny adres tunelu, zapisuje port w bazie MySQL i przesyła audio przez socket. Konfiguracja zawiera dane połączeniowe do bazy oraz token ngrok w plikach konfiguracyjnych. Projekt sam deklaruje wczesną fazę, brak stabilności i potrzebę lepszego error handlingu.

## Ryzyka
1. Dane dostępowe są pobierane z plików lokalnych bez pokazanej warstwy bezpiecznego sekret management.
2. Surowy TCP/audio przez tunel wymaga zaprojektowania uwierzytelniania, integralności i poufności.
3. Występuje współbieżność oparta o globalny stan i wątki bez widocznego modelu lifecycle.
4. SQL jest składany bezpośrednio w kodzie; wymaga parametryzacji i walidacji.
5. Brak potwierdzonego zestawu testów automatycznych i CI.

## Kolejność prac
1. Zdefiniować protokół połączenia i model zagrożeń.
2. Oddzielić konfigurację/sekrety od kodu.
3. Przebudować transport na uwierzytelniony i szyfrowany kanał.
4. Zastąpić globalny stan jawnym modelem sesji/call lifecycle.
5. Parametryzować SQL i dodać obsługę błędów/reconnect.
6. Dodać testy protokołu, jednostkowe i integracyjne.
7. Dopiero po stabilizacji polonizacja i rebranding.

## Kryterium zakończenia
Bezpieczny transport, brak sekretów w repozytorium, deterministyczne zarządzanie połączeniami, testy i powtarzalny build.
