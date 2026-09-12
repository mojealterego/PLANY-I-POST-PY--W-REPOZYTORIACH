# eSim-Cloud — plan pracy

## Status
AUDYT ZAKOŃCZONY — duży projekt eSIM/EDA.

## Stan faktyczny
Repozytorium ok. 54 MB, gałąź `master`. Zakres wymaga audytu usług chmurowych, integracji eSIM, storage i API. Nie należy utożsamiać podobieństwa nazwy z repozytorium `eSim`.

## Ryzyka
- dane abonentów/profili eSIM;
- operacje provisioningowe i uprawnienia;
- sekrety dostawców oraz API;
- zgodność i audyt operacji telekomunikacyjnych.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Zmapować moduły, manifesty i deployment.
2. Audyt auth, secrets, API i storage.
3. Testy izolacji tenantów i operacji provisioningowych.
4. Observability i audyt zmian.
5. Polonizacja/rebranding po hardeningu.

## Kryterium zakończenia
Bezpieczne provisioning/auth, testy integracyjne i pełny audit trail operacji.
