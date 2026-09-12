# Plan pracy — plasmic

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: duży monorepo visual builder / platforma webowa
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Repozytorium jest dużym monorepo Plasmic. README opisuje visual builder, CMS, codegen, integracje React, dane, auth/RBAC i hosting. Manifest używa pnpm 11.10.0 i Node >=20; posiada Vitest, typecheck, lint, build oraz rozbudowane skrypty setupu. Występują również mechanizmy safehouse dla agentów, sprawdzające dostęp do systemu plików i sieci przed uruchomieniem trybu automatycznego. fileciteturn233file0 fileciteturn234file0

## Ryzyka
1. Bardzo duża złożoność monorepo i wiele pakietów.
2. Platforma łączy edycję wizualną, codegen, dane, auth i deployment — wymagane kontrakty między warstwami.
3. Automatyzacja agentowa i MCP wymaga ścisłych granic systemowych.
4. Różne licencje dla części platformy wymagają zachowania provenance.

## Kolejność prac
1. Zmapować workspace/pakiety i granice platformy.
2. Zweryfikować build, testy, typecheck i CI.
3. Przeanalizować auth/RBAC, webhooks, codegen i integracje danych.
4. Zweryfikować sandbox/safehouse oraz wszystkie operacje filesystem/network.
5. Zbudować macierz zależności i kontraktów.
6. Dopiero potem ocenić, które własne warstwy mogą zostać rebrandowane/polonizowane.

## Kryterium zakończenia
Powtarzalny build monorepo, przechodzące testy i typecheck, zweryfikowane granice bezpieczeństwa oraz kompletna mapa zależności i licencji.
