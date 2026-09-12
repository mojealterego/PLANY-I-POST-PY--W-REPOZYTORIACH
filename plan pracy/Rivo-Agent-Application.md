# Plan pracy — Rivo-Agent-Application

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: Android local-first AI assistant
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia z repozytorium
Rivo jest aplikacją React Native 0.85.3 z TypeScript, `llama.rn`, Firebase Auth/Google Sign-In, AsyncStorage, background downloaderem oraz własnymi modułami Kotlin do walidacji i operacji na plikach GGUF. README deklaruje lokalne wnioskowanie po pobraniu modelu, do siedmiu wątków, pamięć lokalną, rekomendacje modeli i weryfikację plików. Repozytorium zawiera również skaffold iOS oraz stronę towarzyszącą. fileciteturn818file0 Manifest potwierdza zależności RN, `llama.rn`, Firebase, downloader, Jest i TypeScript. fileciteturn820file0

## Ryzyka
1. Model jest pobierany z zewnętrznego hostingu — konieczna integralność, provenance i licencje.
2. Dane rozmów, pamięć i metadane modeli są przechowywane lokalnie; AsyncStorage wymaga oceny pod kątem danych wrażliwych.
3. README wskazuje, że bieżący release nadal używa debug keystore — blokada przed produkcyjnym wydaniem.
4. Firebase/Google Sign-In i konfiguracja OAuth wymagają rozdzielenia danych publicznych od sekretów.
5. Operacje kopiowania/usuwania modeli i logout wymagają atomowości oraz bezpiecznego recovery.
6. Wydajność inference zależy od urządzenia i modelu; potrzebne testy fizycznych urządzeń.

## Kolejność prac
1. Zweryfikować model download → checksum/provenance → install → delete lifecycle.
2. Zabezpieczyć lokalną pamięć i wyznaczyć klasy danych wrażliwych.
3. Zastąpić debug signing produkcyjnym podpisem i zweryfikować release build.
4. Audytować Firebase/OAuth, deep links i konfigurację środowisk.
5. Dodać testy urządzeniowe dla pobierania, walidacji, inference i cleanup.
6. Zmierzyć RAM/VRAM/CPU/baterię i czas pierwszego uruchomienia modeli.

## Kryterium zakończenia
Powtarzalny release APK, produkcyjne podpisywanie, bezpieczne przechowywanie danych, zweryfikowany supply chain modeli oraz testy na rzeczywistych urządzeniach.
