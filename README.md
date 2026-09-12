# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **299**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — **299 repozytoriów** |
| Audyt szczegółowy | W TOKU — **76/299** |
| Plany pracy | UTWORZONE — **76/299** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 67 | developerPortfolio | Stary szablon portfolio React/CRA; React 16, CRA 3.2, node-sass i historyczne zależności wymagają modernizacji oraz bezpiecznej integracji GitHub API | ŚREDNI | `plan pracy/developerPortfolio.md` |
| 68 | eSim | Duży projekt EDA z PyQt6 oraz KiCad/Ngspice/GHDL/Verilator/OpenModelica; wymaga macierzy kompatybilności i testów regresyjnych symulacji | WYSOKI | `plan pracy/eSim.md` |
| 69 | PyPhone | Eksperymentalny klient VoIP/PyQt z MySQL, socketami, PyAudio i ngrok; krytyczne bezpieczeństwo transportu, sekretów i współbieżności | WYSOKI | `plan pracy/PyPhone.md` |
| 70 | telephony | Platforma telekomunikacyjna VoxImplant z konfiguracją stref, routingu, harmonogramów i CI/CD; wymaga walidacji konfiguracji i kontroli sekretów | WYSOKI | `plan pracy/telephony.md` |
| 71 | Issabel-PBX | Konteneryzowany PBX z macvlan, reverse proxy, wieloma portami i NET_ADMIN; wymaga minimalizacji ekspozycji i uprawnień | WYSOKI | `plan pracy/Issabel-PBX.md` |
| 72 | plasmic | Duży monorepo visual buildera z codegen, CMS, auth/RBAC i wieloma pakietami; dodatkowo zawiera mechanizmy safehouse dla automatyzacji agentowej | KRYTYCZNY | `plan pracy/plasmic.md` |
| 73 | dcache | Duży rozproszony system storage z wieloma protokołami; Java 21, Maven i Jenkins, wymagane testy recovery/interoperacyjności | KRYTYCZNY | `plan pracy/dcache.md` |
| 74 | ai | Lokalny generator obrazu/wideo 18+ oparty o Wan 2.5 i LoRA; krytyczne provenance modeli, supply chain i guardraile treściowe | KRYTYCZNY | `plan pracy/ai.md` |
| 75 | stumblybot | Historyczny eksperyment robotyki Marty + Google Assistant/DialogFlow; README wskazuje brak własnego auth/encryption routera | ŚREDNI | `plan pracy/stumblybot.md` |
| 76 | grapesjs | Duży monorepo visual web buildera; pnpm/Node 20+, TypeScript, Jest, lint/typecheck i osobne pakiety core/CLI/docs | WYSOKI | `plan pracy/grapesjs.md` |

## Poprzednie audyty

Audyty 1–66 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 67–76 są opisane powyżej.

## Postęp

**76 / 299 repozytoriów — 25,42% audytu szczegółowego.**  
**223 repozytoria pozostają do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **299 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
