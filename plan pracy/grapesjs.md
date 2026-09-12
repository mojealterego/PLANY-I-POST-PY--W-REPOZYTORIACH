# Plan pracy — grapesjs

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: duży monorepo visual web builder / framework
- Priorytet: WYSOKI
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Repozytorium jest monorepo GrapesJS. Gałąź `dev` zawiera pnpm 9.10.0, Node >=20, skrypty build/test/lint/typecheck i osobne pakiety core, CLI oraz dokumentacji. Stos obejmuje TypeScript, Jest, ESLint, Babel i Prettier. fileciteturn239file0 README nie zostało poprawnie odczytane przez konektor, dlatego treść dokumentacji wymaga osobnej weryfikacji.

## Ryzyka
1. Duże monorepo wymaga analizy zależności między pakietami i release train.
2. Build/test są rozproszone po workspace.
3. Konieczna jest weryfikacja kompatybilności Node/pnpm oraz artefaktów publikowanych do npm.
4. Własne zmiany należy oddzielić od upstreamu przed rebrandingiem.

## Kolejność prac
1. Zmapować workspace i pakiety.
2. Zweryfikować build, test, lint, format i typecheck.
3. Przeanalizować publiczne API core/CLI i kontrakty między pakietami.
4. Zweryfikować proces release/publish i provenance artefaktów.
5. Dodać/uzupełnić testy kontraktowe dla kluczowego API.
6. Następnie polonizacja i rebranding wyłącznie warstwy własnej.

## Kryterium zakończenia
Powtarzalny build monorepo, pełny zestaw testów i kontroli jakości, zweryfikowany release/publish oraz rozdzielenie własnych zmian od upstreamu.
