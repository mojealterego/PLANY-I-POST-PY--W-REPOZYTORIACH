# AUDYT 369 — nocodb

## Status
Audyt wykonany. Duży open-source no-code database platform z UI, API, rolami i App Store integracji.

## Ustalenia
Spreadsheet-like UI, wiele widoków, fine-grained access control, REST/SDK, JWT/social auth, automatyzacje, storage i integracje.

## Ryzyka
Auth/RBAC, public/private views, tokeny, plugin/integration execution, storage, deployment scripts i dane biznesowe.

## Plan prac
Zmapować monorepo, backend/frontend, auth, API, pluginy, storage i deployment. Zweryfikować RBAC, secret handling, SSRF i public sharing. Następnie polonizacja.

## Kryterium zakończenia
Kompletne testy autoryzacji i izolacji danych oraz powtarzalny bezpieczny deployment.
