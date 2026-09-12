# Plan pracy — Temp-SMS-Receive

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: narzędzie CLI do pobierania publicznie dostępnych numerów tymczasowych i wiadomości SMS
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia z kodu
README opisuje CLI w Pythonie z `requests`, `colorama`, `pyfiglet`, `pyperclip` i `pycryptodome`. Program pobiera listę krajów, numery i wiadomości z zewnętrznego API, a także posiada automatyczne pobieranie zależności i aktualizację przez Git. Kod `tempsms.py` zawiera zakodowany klucz AES/CBC używany do odszyfrowania klucza autoryzacyjnego API. fileciteturn810file0 fileciteturn814file0

## Ryzyka
1. Klucz kryptograficzny jest zapisany bezpośrednio w kodzie.
2. Program komunikuje się z zewnętrznym API i automatycznie pobiera dane SMS.
3. Automatyczne `pip install` i `git pull` z poziomu programu zwiększają powierzchnię łańcucha dostaw.
4. Mechanizm aktualizacji nie weryfikuje kryptograficznie artefaktu przed uruchomieniem.
5. README opisuje użycie narzędzi do dekompilacji i przechwytywania ruchu; wymaga zachowania wyłącznie badawczego/compliance.
6. Brak widocznej warstwy testów i kontraktów API.

## Kolejność prac
1. Usunąć sekret kryptograficzny z kodu i zaprojektować bezpieczny mechanizm autoryzacji.
2. Zweryfikować legalność i warunki użycia dostawcy numerów/SMS.
3. Wprowadzić timeouty, walidację odpowiedzi, obsługę błędów i limity zapytań.
4. Oddzielić aktualizację od wykonania oraz dodać weryfikację integralności wydań.
5. Dodać testy jednostkowe i kontraktowe bez kontaktu z prawdziwą usługą.
6. Ograniczyć dokumentację do bezpiecznego, autoryzowanego użycia.

## Kryterium zakończenia
Brak sekretów w źródłach, deterministyczne testy API na mockach, zweryfikowany lifecycle aktualizacji, bezpieczne zarządzanie danymi SMS oraz udokumentowane ograniczenia zgodności.
