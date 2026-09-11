# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **293**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — **293 repozytoria** |
| Audyt szczegółowy | W TOKU — **38/293** |
| Plany pracy | UTWORZONE — **38/293** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 35 | LTX-Video | Model generowania wideo Python/ML; repozytorium wskazuje LTX-2 jako główny kierunek dalszego rozwoju | KRYTYCZNY | `plan pracy/LTX-Video.md` |
| 36 | agent-starter-pack | CLI/szablony agentowe Google Cloud; projekt w maintenance mode z migracją do agents-cli | WYSOKI | `plan pracy/agent-starter-pack.md` |
| 37 | Agriculture_KnowledgeGraph | Archiwalny projekt Django/Neo4j/NLP; bardzo stary stos, projekt nieutrzymywany | ŚREDNI | `plan pracy/Agriculture_KnowledgeGraph.md` |
| 38 | mini-mobile-7 | Szkielet laboratorium prywatnej sieci LTE/5G; Open5GS, UERANSIM, Kamailio/IMS i RAN, z wyraźnymi bramkami bezpieczeństwa oraz prawnymi | WYSOKI | `plan pracy/mini-mobile-7.md` |

## Poprzednie audyty

Audyty 1–34 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`.

## Postęp

**38 / 293 repozytoriów — 12,97% audytu szczegółowego.**  
**255 repozytoriów pozostaje do audytu.**

## Aktualizacja inwentaryzacji

Portfel wzrósł do **293 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
