# threema-android — plan pracy

## Status
AUDYT ZAKOŃCZONY — duży klient Android komunikatora.

## Stan faktyczny
Repozytorium ok. 114 MB, gałąź `main`. Jest to rozbudowana aplikacja Android związana z bezpieczną komunikacją. Szczególny nacisk audytu: kryptografia, E2EE, storage, uprawnienia, sieć i aktualność zależności.

## Ryzyka
- krytyczny kod bezpieczeństwa i prywatności;
- migracje danych oraz kluczy;
- native/crypto dependencies;
- regresje bezpieczeństwa przy polonizacji lub rebrandingu.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Zweryfikować Gradle modules, manifesty i CI.
2. Audyt granic kryptograficznych i storage.
3. Testy instrumentacyjne oraz migracyjne.
4. Dependency/security scanning.
5. Dopiero potem polonizacja interfejsu.

## Kryterium zakończenia
Brak regresji kryptograficznej, reproducible build Android i przechodzące testy bezpieczeństwa.
