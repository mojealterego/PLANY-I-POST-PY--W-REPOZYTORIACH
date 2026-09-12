# LocalAI — plan pracy

## Status
AUDYT ZAKOŃCZONY — duży serwer lokalnych modeli AI.

## Stan faktyczny
Repozytorium ok. 100 MB, gałąź domyślna `master`. Projekt wymaga pełnego przeglądu backendu, providerów modeli, API, storage, konteneryzacji i CI. Nie traktować samej obecności kodu jako dowodu produkcyjności.

## Ryzyka
- duża powierzchnia API i providerów;
- wykonywanie modeli/operacji lokalnych może mieć szerokie uprawnienia;
- pobieranie modeli i zasobów z sieci wymaga kontroli źródeł;
- kompatybilność sprzętowa i sterowniki.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Mapa modułów i punktów wejścia.
2. Audyt API/auth/network/storage/model execution.
3. Build/test/CI i reproducibility.
4. Hardening izolacji oraz polityk zasobów.
5. Polonizacja/rebranding po stabilizacji.

## Kryterium zakończenia
Zweryfikowany build, testy API, izolacja operacji modelowych i dokumentacja wdrożeniowa.
