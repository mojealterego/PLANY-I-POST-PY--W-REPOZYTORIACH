# Plan pracy — element-x-android

## Stan audytu
**AUDYT ZAKOŃCZONY — duży, aktywnie rozwijany klient Android Matrix; krytyczny dla analizy bezpieczeństwa i jakości mobilnej.**

## Ustalenia
README opisuje całkowity rewrite Element X Android oparty o Matrix Rust SDK, Jetpack Compose i Appyx, z minimalnym Android SDK 24. Repozytorium ma CI, SonarCloud i Codecov. Katalog wersji wskazuje nowoczesny Kotlin 2.4.10, AGP 9.3.2, Compose BOM 2026.08.00, SQLDelight, SQLCipher, Tink, OkHttp, Retrofit i Matrix SDK.

## Ryzyka i braki
- duża złożoność Kotlin/Compose + Rust FFI;
- krytyczne znaczenie poprawności warstwy Matrix Rust SDK i FFI;
- użycie części zależności alpha wymaga świadomej polityki aktualizacji;
- należy zweryfikować target/min SDK, podpisywanie, konfiguracje release i ochronę sekretów;
- storage SQLCipher/SQLDelight oraz migracje wymagają testów na realnych upgrade paths;
- konieczne są testy urządzeniowe, screenshot/regression i synchronizacji Matrix;
- repo jest upstreamowym projektem Element, więc rebranding musi być wykonany wyłącznie na warstwach należących do użytkownika i po analizie licencji dual-license.

## Priorytet
**KRYTYCZNY**

## Kolejność prac
1. Zmapować moduły Android, FFI Rust i konfigurację buildów.
2. Zweryfikować Matrix SDK API oraz wersję FFI.
3. Audytować storage, szyfrowanie, klucze i migracje.
4. Uruchomić unit/instrumentation/UI tests i CI.
5. Zweryfikować release signing, proguard/R8, permissions i network security.
6. Zbudować testy regresji dla logowania, synchronizacji, E2EE, media i migracji DB.
7. Ustalić zakres własnych zmian względem upstreamu.
8. Dopiero po tym rozpocząć rebranding/polonizację zgodną z licencją.

## Kryterium zakończenia
Reprodukowalny build release, przechodzące testy Android/FFI/storage, zweryfikowane granice E2EE oraz jasna separacja zmian własnych od upstreamu. Audyt nie oznacza statusu produkcyjnego.
