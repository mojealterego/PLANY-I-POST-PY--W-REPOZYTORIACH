# Kartografia — plan pracy

## Stan audytu
**AUDYT ZAKOŃCZONY — mobilna gra React/Vite z PWA i konfiguracją Capacitor Android.**

## Ustalenia
- README opisuje sześć faz rozgrywki, mechaniki kart, mapę ciała, napięcie, rynek/progresję, scenariusze, statystyki i lokalną persystencję.
- Dostępne są skrypty Vite oraz przygotowanie/synchronizacja/budowanie Android przez Capacitor.
- `package.json` używa wersji `latest` dla React, Vite, Capacitor i pluginu React, co osłabia reprodukowalność.
- Jest podstawowy `node --check` i deklarowane CI build validation; nie potwierdzono jeszcze zakresu testów funkcjonalnych.
- README wyraźnie nie deklaruje podpisanego artefaktu release bez rzeczywistej walidacji środowiska Android.

## Ryzyka
1. `latest` w zależnościach może powodować nieprzewidywalne zmiany builda.
2. Brak widocznej rozbudowanej warstwy testów gameplayu.
3. Konfiguracja Capacitor wymaga walidacji uprawnień, storage i zachowania offline.

## Plan
1. Przypiąć zależności do kontrolowanych wersji.
2. Zmapować model gry i sześć faz jako osobne kontrakty domenowe.
3. Dodać testy mechanik kart, progów napięcia, scenariuszy i persystencji.
4. Dodać testy PWA/offline i migracji local storage.
5. Zweryfikować konfigurację Capacitor, Android permissions i lifecycle.
6. Dodać test E2E podstawowej ścieżki gry.
7. Ustabilizować CI: lint, build web, testy i debug APK.
8. Przygotować pełną polską dokumentację i rebranding po ustabilizowaniu funkcji.

## Kryterium zakończenia
Powtarzalny web build, testy domeny gry, zweryfikowany offline/PWA i Android debug build. Release dopiero po walidacji podpisanego artefaktu.
