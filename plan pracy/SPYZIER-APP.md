# Audyt 169 — SPYZIER-APP

## Status
AUDYT ZAKOŃCZONY — stary Android client-server monitoring/spyware.

## Ustalenia
README deklaruje śledzenie lokalizacji, kontaktów, połączeń, SMS, screen capture i ukryte działanie. Architektura używa Firebase, Google Maps i MediaProjection. Projekt celuje w stare Android Oreo/API 29.

## Ryzyka
Bardzo wysokie: ukryte monitorowanie, dostęp do danych komunikacyjnych i lokalizacyjnych, zdalne sterowanie oraz brak zgody użytkownika.

## Priorytet
KRYTYCZNY — wyłącznie analiza defensywna/forensic.

## Kolejność prac
Nie rozwijać funkcji ukrytego monitorowania. Dokumentacja → klasyfikacja → analiza uprawnień → usunięcie/izolacja sekretów → bezpieczne testy laboratoryjne.

## Kryterium zakończenia
Repozytorium pozostaje materiałem badawczym i nie otrzymuje nowych funkcji spyware ani instrukcji operacyjnych.
