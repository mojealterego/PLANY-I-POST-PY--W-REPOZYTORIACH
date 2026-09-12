# Plan pracy — AhMyth-Android-RAT

## Status
AUDYT ZAKOŃCZONY — narzędzie RAT, wyłącznie analiza defensywna/laboratoryjna.

## Stan faktyczny
README jasno rozdziela Electronowy panel sterowania i aplikację Android określaną jako backdoor. Projekt jest beta i opisuje budowę binariów oraz APK.

## Ryzyka
zdalne sterowanie urządzeniem; dostęp do danych; persistence; malware supply chain; podpisywanie APK; brak bezpiecznej granicy użycia.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Nie rozwijać funkcji operacyjnych RAT.
2. Zmapować komponenty wyłącznie pod kątem analizy i detekcji.
3. Udokumentować IOC, uprawnienia i powierzchnię ataku na poziomie defensywnym.
4. Izolować build/test w laboratorium.
5. Dodać polską dokumentację analityczną.

## Kryterium zakończenia
Repo jednoznacznie oznaczone jako badawcze, bez instrukcji zwiększających zdolność do nieautoryzowanego monitorowania.