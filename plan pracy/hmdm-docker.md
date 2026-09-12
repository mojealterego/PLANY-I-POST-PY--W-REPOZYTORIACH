# Audyt 302 — hmdm-docker

## Stan
AUDYT ZAKOŃCZONY — infrastruktura kontenerowa dla systemu HMDM.

## Ustalenia
Repozytorium jest małe i skupione na uruchomieniu komponentów HMDM w Dockerze.

## Ryzyka
Sekrety w konfiguracji, ekspozycja portów, trwałość danych, obrazy bazowe, aktualizacje i backup.

## Priorytet
WYSOKI

## Plan prac
Inwentaryzacja compose/env → hardening obrazów → sieć → wolumeny/backup → healthchecki → aktualizacje i skanowanie obrazów.

## Kryterium
Powtarzalne uruchomienie, brak sekretów w repozytorium, ograniczona ekspozycja sieciowa i sprawdzony recovery.
