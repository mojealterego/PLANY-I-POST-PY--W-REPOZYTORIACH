# Plan pracy — pegasus-skills

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: katalog umiejętności dla agentów AI
- Priorytet: ŚREDNI
- Gałąź: `main`

## Ustalenia
- Repozytorium dostarcza umiejętności Markdown dla Django/SaaS Pegasus.
- Obecnie opisane są dwa główne moduły: rozwiązywanie konfliktów aktualizacji oraz aktualizacja Pegasus.
- README zakłada integrację z Claude Code/plugin marketplace i narzędziem CLI.
- Artefakt jest bardziej biblioteką wiedzy/procedur niż aplikacją wykonywalną.

## Ryzyka
1. Umiejętności mogą zawierać instrukcje zależne od wersji narzędzi i frameworków.
2. Brak kontraktowych testów poprawności metadanych i triggerów może powodować błędny dobór umiejętności.
3. Linki i instrukcje instalacyjne wymagają okresowej weryfikacji.

## Kolejność prac
1. Zindeksować wszystkie `SKILL.md` i metadane.
2. Ujednolicić schemat umiejętności, triggerów, preconditions i rezultatów.
3. Dodać testy strukturalne i walidację linków.
4. Rozdzielić wiedzę stabilną od instrukcji zależnych od wersji.
5. Dodać polskie wersje dokumentacji bez naruszania kompatybilnych identyfikatorów technicznych.
6. Zdefiniować proces aktualizacji i testów regresyjnych.

## Kryterium zakończenia
Każda umiejętność ma jednoznaczne metadane, aktualne instrukcje, walidowalne przykłady i przechodzące testy strukturalne.
