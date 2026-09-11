# Plan pracy — mojealterego.github.io

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: osobista strona/portal treściowy React + Vite
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- Repozytorium działa jako centralny portal świata MojeAlterego i zawiera rozbudowany ledger treści właściciela.
- README wymaga zachowania tekstów źródłowych, śledzenia braków i aktualizacji README po każdej zmianie.
- Deklarowany stos to React + Vite, z wieloma trasami tematycznymi obejmującymi fotografię, książki, film, aplikacje, agentów i projekty.
- Dokumentacja rozróżnia źródło kanoniczne od skróconych tekstów implementacyjnych oraz jawnie oznacza materiał nieodzyskany.

## Ryzyka
1. Duża objętość treści i ryzyko rozbieżności między źródłami kanonicznymi a UI.
2. Nie wolno automatycznie parafrazować materiału właściciela.
3. Dane biograficzne, osiągnięcia, linki zewnętrzne i statystyki wymagają źródeł oraz kontroli zmian.
4. Wielostronicowa aplikacja wymaga kontroli routingu, SEO, dostępności i wydajności.

## Kolejność prac
1. Zmapować `src`, trasy, komponenty, zasoby i dokumenty źródłowe.
2. Ustalić jednoznaczny model treści kanonicznej i mechanizm wykrywania rozbieżności.
3. Zabezpieczyć teksty źródłowe przed przypadkową utratą i dodać walidację kompletności.
4. Zmodernizować architekturę React/Vite bez zmiany treści właściciela.
5. Dodać testy routingu, treści, dostępności, SEO i build produkcyjny.
6. Zweryfikować wszystkie linki, media i dane dynamiczne.
7. Przeprowadzić kontrolowaną polonizację UI i ujednolicić branding.

## Kryterium zakończenia
Build jest powtarzalny, każda trasa ma źródło treści, brakujące materiały są jawnie oznaczone, testy przechodzą, a zmiany nie naruszają kanonicznych treści właściciela.
