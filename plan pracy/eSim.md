# Plan pracy — eSim

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: duży projekt EDA / symulacja elektroniki
- Priorytet: WYSOKI
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
eSim to rozbudowane środowisko EDA z GUI PyQt6 oraz integracjami KiCad, Ngspice, GHDL, Verilator, OpenModelica i PDK. Repozytorium zawiera `src/`, biblioteki komponentów, przykłady, dokumentację Sphinx, pakowanie Flatpak/AppImage/Snap/Docker oraz konfigurację CI/CD. README wskazuje wersję 2.5. `requirements.txt` miesza zależności ściśle przypięte z szerokimi zakresami; część stosu jest historyczna.

## Ryzyka
1. Duża liczba zewnętrznych silników i formatów zwiększa powierzchnię integracyjną.
2. Konieczna weryfikacja zgodności wersji KiCad/Ngspice/GHDL/Qt/Python.
3. Konwertery netlist i plików projektowych wymagają testów regresyjnych na fixture'ach.
4. Pakowanie wieloplatformowe wymaga reprodukowalnych buildów.
5. Dane bibliotek/PDK oraz ich licencje i provenance wymagają osobnego przeglądu.

## Kolejność prac
1. Zmapować moduły GUI, symulacji, konwersji i integracji.
2. Zdefiniować macierz wersji narzędzi zewnętrznych.
3. Dodać testy parserów, konwerterów i podstawowych przepływów symulacji.
4. Uporządkować zależności i środowiska build.
5. Zweryfikować CI oraz wszystkie kanały pakowania.
6. Dopiero potem polonizacja dokumentacji i rebranding własnej warstwy.

## Kryterium zakończenia
Reprodukowalny build, zweryfikowane integracje EDA, testy regresyjne konwersji/symulacji, poprawne pakiety oraz aktualna dokumentacja.
