# Plan pracy — stumblybot

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: historyczny eksperyment robotyki/voice assistant
- Priorytet: ŚREDNI
- Status produkcyjny: NIE

## Ustalenia
StumblyBot jest małym projektem integrującym robota Marty, Google Assistant SDK i DialogFlow. README opisuje router, serwer na Raspberry Pi, webhooki DialogFlow oraz komunikację z robotem. Dokumentacja wprost wskazuje brak właściwego szyfrowania i uwierzytelniania routera oraz konieczność konfiguracji HTTPS przez reverse proxy. fileciteturn238file0

## Ryzyka
1. Historyczne zależności Google Assistant/DialogFlow mogą być nieaktualne.
2. Router wystawiany do Internetu bez własnego auth/encryption nie nadaje się do produkcji.
3. Adresy IP i konfiguracja są częściowo zaszyte w kodzie według README.
4. Projekt wymaga fizycznego hardware i testów integracyjnych.

## Kolejność prac
1. Ustalić, czy projekt ma być reaktywowany, czy zachowany jako archiwum.
2. Jeśli reaktywacja: zmodernizować komunikację i konfigurację.
3. Wprowadzić uwierzytelnianie, szyfrowanie i ograniczenie powierzchni sieciowej.
4. Zastąpić twardo zakodowane endpointy konfiguracją.
5. Dodać testy routera/protokołu i testy sprzętowe.

## Kryterium zakończenia
Dla archiwum: kompletna dokumentacja historyczna. Dla reaktywacji: bezpieczny transport, konfiguracja bez hardcode, testy i aktualny stos zależności.
