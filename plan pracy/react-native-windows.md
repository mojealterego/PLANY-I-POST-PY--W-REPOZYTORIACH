# Plan pracy — react-native-windows

## Status
AUDYT ZAKOŃCZONY — duży upstream framework React Native dla Windows.

## Stan faktyczny
Repozytorium Microsoftu dodaje obsługę Windows SDK do React Native, obejmując aplikacje desktopowe, Xbox i urządzenia wspierane przez Windows. README wskazuje Paper/Fabric, WinAppSDK, dokumentację, przykłady i testy.

## Ryzyka
- ogromny zakres natywnego C++/C#/JS;
- kompatybilność Windows SDK i architektury Fabric;
- natywne uprawnienia i interop;
- koszt utrzymania forkowania upstream.

## Priorytet
WYSOKI — REFERENCJA.

## Kolejność prac
1. Mapowanie packages, native code i CI.
2. Weryfikacja macierzy wersji RN/Windows SDK.
3. Testy buildów i E2E.
4. Polonizacja wyłącznie warstwy dokumentacyjnej wymaganej w portfelu.

## Kryterium zakończenia
Zweryfikowana kompatybilność i build; brak niepotrzebnego odchodzenia od upstream.
