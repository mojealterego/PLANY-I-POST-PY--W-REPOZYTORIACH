# Plan pracy — sms-verification-platforms

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: repozytorium badawczo-porównawcze / publikacja techniczna
- Priorytet: ŚREDNI
- Gałąź: `main`

## Ustalenia
- README jest obszernym materiałem porównującym usługi tymczasowych numerów i weryfikacji SMS.
- Dokumentacja jawnie rozróżnia dane oficjalne, testy publiczne i twierdzenia dostawców oraz zaznacza ograniczenia próbek.
- Część danych jest dynamiczna: ceny, zapasy, liczba krajów i dostępność usług.
- Projekt nie powinien być traktowany jak aplikacja produkcyjna bez dodatkowej implementacji.

## Ryzyka
1. Szybkie starzenie się danych cenowych i dostępności.
2. Ryzyko mieszania danych własnych, marketingowych i niezależnych bez silnego oznaczenia źródła.
3. Materiał może ułatwiać obchodzenie mechanizmów weryfikacyjnych, dlatego publikacja powinna pozostać na poziomie porównania usług i metodologii, bez instrukcji nadużyć.
4. Brak automatycznego systemu wersjonowania i walidacji źródeł.

## Kolejność prac
1. Zbudować schemat danych dla dostawcy, źródła, daty weryfikacji, próbki i poziomu pewności.
2. Oddzielić dane historyczne od bieżących.
3. Dodać automatyczne wykrywanie wygasłych linków i niekompletnych rekordów.
4. Wprowadzić audyt cytowań i konfliktów źródeł.
5. Polonizować dokumentację, zachowując neutralny, analityczny charakter.
6. Jeśli ma powstać aplikacja, wydzielić warstwę danych od prezentacji i dodać testy.

## Kryterium zakończenia
Każda istotna liczba ma datę, źródło i ocenę jakości dowodu; publikacja nie przedstawia deklaracji marketingowych jako niezależnie potwierdzonych faktów.
