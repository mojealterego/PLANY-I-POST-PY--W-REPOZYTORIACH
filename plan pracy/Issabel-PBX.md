# Plan pracy — Issabel-PBX

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: konteneryzowany PBX / konfiguracja infrastruktury
- Priorytet: WYSOKI
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README jest bardzo krótki i opisuje uruchomienie Issabel PBX w Dockerze z macvlan, reverse proxy oraz dużym zestawem wystawionych portów telekomunikacyjnych. Kontener otrzymuje `NET_ADMIN`, używa trwałych wolumenów dla `/etc`, `/var/www`, `/var/log`, `/var/lib` i `/home`, a konfiguracja zakłada zewnętrzny reverse proxy i automatyczne obrazy Docker Hub.

## Ryzyka
1. Bardzo szeroka powierzchnia sieciowa wynikająca z licznych portów PBX/HTTP/SIP/RTP.
2. `NET_ADMIN` zwiększa uprzywilejowanie kontenera.
3. README zawiera przykładowe placeholdery adresacji i nazw hostów; konfiguracja musi być rozdzielona od instrukcji.
4. Brak widocznej dokumentacji hardeningu obrazu, aktualizacji i backup/restore.
5. PBX wymaga szczególnej kontroli ekspozycji SIP, panelu administracyjnego i usług zarządzających.

## Kolejność prac
1. Zmapować rzeczywisty Dockerfile, obraz bazowy i skrypty inicjalizacji.
2. Ograniczyć porty i capability do niezbędnego minimum.
3. Zweryfikować TLS, reverse proxy, SIP/RTP oraz panel administracyjny.
4. Dodać healthcheck, backup/restore i procedurę aktualizacji obrazu.
5. Przeprowadzić testy izolacji kontenera i konfiguracji sieci.
6. Uporządkować dokumentację i dopiero później polonizować własne materiały.

## Kryterium zakończenia
Minimalne uprawnienia i ekspozycja sieciowa, zweryfikowane TLS/SIP/RTP, reprodukowalny obraz, backup/restore oraz testy wdrożeniowe.
