# pocketpal-ai — plan pracy

## Status
AUDYT ZAKOŃCZONY — aplikacja lokalnego AI.

## Stan faktyczny
Repozytorium średniej wielkości, rozpoznane jako PocketPal AI; wymaga analizy kodu aplikacji mobilnej, modeli lokalnych, storage i sieci. W dalszej walidacji należy ustalić dokładny framework i wersje zależności.

## Ryzyka
- pobieranie i przechowywanie modeli;
- prywatność lokalnych rozmów i plików;
- pamięć urządzenia oraz kompatybilność modeli;
- ewentualne integracje sieciowe.

## Priorytet
WYSOKI

## Kolejność prac
1. Zmapować manifesty, moduły aplikacji i CI.
2. Audyt storage, model loading i uprawnień.
3. Testy urządzeniowe oraz ograniczenia zasobów.
4. Hardening i obserwowalność.
5. Polonizacja/rebranding.

## Kryterium zakończenia
Build i testy mobilne na reprezentatywnych urządzeniach oraz zweryfikowana polityka danych lokalnych.
