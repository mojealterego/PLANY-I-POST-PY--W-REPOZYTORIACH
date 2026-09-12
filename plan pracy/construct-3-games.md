# Plan pracy — construct-3-games

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: archiwum wielu projektów gier Construct 3
- Priorytet: ŚREDNI / REFERENCYJNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README opisuje monorepo wielu małych gier i prototypów tworzonych w Construct 3, m.in. roguelite, puzzle, gry karciane, multiplayer/couch oraz projekty mobilne. Projekty są przeznaczone do otwierania w wizualnym edytorze Construct 3, a kod nie jest traktowany jako ręcznie utrzymywana aplikacja. README rozlicza również pochodzenie assetów, kodu i fontów. fileciteturn843file0

## Ryzyka
1. Duża liczba historycznych projektów i różny stan ukończenia.
2. Asset/licensing provenance wymaga zachowania przy ponownym wykorzystaniu.
3. Folder-based saves ograniczają sens klasycznego refaktoru kodu.
4. Projekty zewnętrznych jamów mogą mieć zależności od starych wersji Construct.

## Kolejność prac
1. Zindeksować każdy projekt i jego stan.
2. Rozdzielić gry ukończone, prototypy, testy i projekty porzucone.
3. Zweryfikować asset provenance/licencje.
4. Zachować oryginalne projekty jako referencję przed migracją.
5. Tylko wybrane projekty migrować do nowej architektury i polonizacji.

## Kryterium zakończenia
Każdy podprojekt ma status, źródła assetów i wymagania środowiskowe; zachowany jest oryginał, a wybrane gry posiadają powtarzalny eksport i test podstawowych ścieżek.
