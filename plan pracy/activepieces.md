# Plan pracy — activepieces

## Status
AUDYT ZAKOŃCZONY — duża platforma automatyzacji/workflow; referencja infrastrukturalna.

## Stan faktyczny
Repozytorium ma ponad 700 MB i `main`. Ze względu na zakres integracji wymaga analizy silnika workflow, connectorów, sekretów, workerów i multi-tenancy.

## Ryzyka
- wykonywanie workflow i connectorów;
- sekrety integracji;
- izolacja tenantów;
- webhooki i SSRF;
- duża powierzchnia zależności.

## Priorytet
KRYTYCZNY — REFERENCJA.

## Kolejność prac
1. Mapa runtime/connectorów.
2. Auth/secrets/tenant isolation.
3. Sandbox i webhook security.
4. CI/testy regresji.

## Kryterium zakończenia
Udokumentowane granice wykonania i bezpieczne zarządzanie sekretami.
