# Plan pracy — JARVIS-2.0

## Status audytu
- Klasyfikacja: aktywny prototyp aplikacji Android + backend Node.js.
- Audyt: wykonany na podstawie README, manifestu aplikacji, `eas.json`, workflow EAS oraz backendu.
- Produkcja: NIE — audyt nie jest certyfikacją produkcyjną.

## Ustalenia
- Aplikacja Android używa Expo Router, React Native 0.86.2 i Expo SDK 57; korzysta m.in. z Secure Store, powiadomień, audio, systemu plików i syntezy mowy.
- Backend wymaga Node.js >=22, używa `busboy` i `pg`, ale bieżąca warstwa stanu nadal zapisuje dane do pliku JSON.
- CI uruchamia kontrolę TypeScript, konfigurację Expo i zdalny build APK przez EAS; profil produkcyjny buduje Android App Bundle.
- README deklaruje ochronę sekretów przez zmienne środowiskowe oraz Secure Store po stronie klienta.

## Krytyczne punkty do hardeningu
1. Zastąpić plikowy stan transakcyjną bazą danych; wykorzystać przygotowaną zależność PostgreSQL i zaprojektować migracje.
2. Usunąć domyślne zachowanie `authorized()`, które przy braku `JARVIS_API_TOKEN` dopuszcza żądania bez uwierzytelnienia. Tryb produkcyjny ma fail-closed.
3. Ograniczyć CORS z `*` do jawnie skonfigurowanych originów.
4. Dodać limity rozmiaru JSON i uploadów audio, limity czasu żądań oraz ochronę przed nadużyciem endpointów.
5. Walidować schematy wejściowe zamiast wykonywać bezpośrednie `String(...)`/`Object.assign(...)` na danych klienta.
6. Rozdzielić autoryzację na użytkownika/organizację/rolę; zatwierdzenia muszą być powiązane z tożsamością operatora i audytowalnym kontekstem.
7. Dodać testy API, testy regresyjne dla approval gate oraz testy integracyjne OpenAI/transkrypcji z mockami.
8. Wprowadzić bezpieczną retencję i ochronę danych dla pamięci, historii rozmów i audytu.
9. Dodać health/readiness checks, obserwowalność i kontrolę błędów bez ujawniania sekretów lub nadmiarowych szczegółów.
10. Zweryfikować konfigurację EAS, pinowanie wersji narzędzi oraz deterministyczność instalacji (`npm ci` + lockfile).

## Kolejność implementacji
1. Kontrakt API i walidacja wejścia.
2. Fail-closed auth + CORS + rate limiting + limity payloadów.
3. PostgreSQL, migracje i warstwa repozytoriów.
4. Approval/audit jako jawny model domenowy z kontrolą uprawnień.
5. Testy jednostkowe, integracyjne i smoke test Android/Backend.
6. CI: lint/typecheck/test/build oraz weryfikacja EAS.
7. Pełna polonizacja dokumentacji i interfejsu oraz rebranding zgodny z centralną strategią.
8. Dopiero po przejściu buildów i testów: ocena gotowości produkcyjnej.

## Kryterium zakończenia
Repozytorium uznajemy za przygotowane do kolejnego etapu dopiero po zweryfikowanym buildzie Android, przechodzących testach backendu, fail-closed security baseline, trwałej warstwie danych, audytowalnym approval gate i kompletnej dokumentacji wdrożeniowej.
