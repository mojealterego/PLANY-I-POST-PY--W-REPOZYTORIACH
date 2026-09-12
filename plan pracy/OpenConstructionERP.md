# AUDYT 370 — OpenConstructionERP

## Status
Audyt wykonany. Rozbudowana self-hosted platforma ERP dla branży budowlanej.

## Ustalenia
README deklaruje BOQ, CAD/BIM takeoff, harmonogramowanie 4D, model kosztowy 5D, tendering, 195 modułów, 120K+ pozycji kosztowych i 44 języki. AGPL-3.0, signed releases, CodeQL/Scorecard.

## Ryzyka
Duża powierzchnia modułowa, dane finansowe/projektowe, AI providers, import CAD/BIM, plugin/module marketplace i desktop releases.

## Plan prac
Zmapować moduły i manifesty, auth/RBAC, dane projektowe, importery, AI, release signing i CI. Zweryfikować izolację projektów i role. Utrzymać istniejące wsparcie PL, rozszerzając jakość lokalizacji.

## Kryterium zakończenia
Powtarzalny build desktop/server, testy bezpieczeństwa danych i modułów oraz zweryfikowany łańcuch release.
