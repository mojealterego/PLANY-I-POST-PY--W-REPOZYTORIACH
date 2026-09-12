# Audyt 301 — hmdm-android

## Stan
AUDYT ZAKOŃCZONY — klient Android systemu zarządzania urządzeniami.

## Ustalenia
Repozytorium zawiera kod aplikacyjny Android; wymaga kontroli manifestu, usług systemowych, polityk urządzenia, komunikacji z serwerem oraz procesu build/release.

## Ryzyka
Uprawnienia administracyjne urządzenia, zdalne polecenia, dane urządzeń, TLS/auth, przechowywanie sekretów i odporność na utratę połączenia.

## Priorytet
WYSOKI

## Plan prac
Manifest → permissions → auth/TLS → lifecycle usług → storage → testy urządzeń → build podpisany → obserwowalność → polonizacja.

## Kryterium
Minimalny zestaw uprawnień, bezpieczne kanały komunikacji i powtarzalny build Android.
