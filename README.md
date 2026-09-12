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
| Audyt szczegółowy | W TOKU — **177/299** |
| Plany pracy | UTWORZONE — **177/299** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 158 | youpac-ai | React Router 7/React 19 + Convex/Clerk/OpenAI/ElevenLabs; agentic tworzenie treści YouTube i canvas | KRYTYCZNY/WYSOKI | `plan pracy/youpac-ai.md` |
| 159 | tmpsms | Archiwalny POSIX sh wrapper; README potwierdza, że usługa Upmasked już nie działa | NISKI | `plan pracy/tmpsms.md` |
| 160 | twilio-pbx | Node/Firebase PBX dla Twilio; połączenia, SMS, DTMF, forwarding i alerty e-mail | WYSOKI | `plan pracy/twilio-pbx.md` |
| 161 | Hands-on-with-SMS-MAN-complete-virtual-number-benchmark2026 | Publikacja benchmarkowa usług numerów; ceny i dostępność dynamiczne | NISKI/ŚREDNI | `plan pracy/Hands-on-with-SMS-MAN-complete-virtual-number-benchmark2026.md` |
| 162 | esim-response-selection | Historyczny ESIM dla wieloturowego wyboru odpowiedzi; Python 2.7/TensorFlow 1.x | NISKI/ŚREDNI | `plan pracy/esim-response-selection.md` |
| 163 | superpowers | Metodologia skills dla agentów kodujących: TDD, planowanie, worktree, subagenty i review | WYSOKI | `plan pracy/superpowers.md` |
| 164 | JieMa_2025 | Chińskojęzyczna publikacja o usługach wirtualnych numerów/SMS z tabelami i linkami afiliacyjnymi | NISKI/ŚREDNI | `plan pracy/JieMa_2025.md` |
| 165 | OpenMontage | Agentic pipeline produkcji wideo z Backlot, approval gates, provider registry, Remotion/FFmpeg/Blender | KRYTYCZNY/WYSOKI | `plan pracy/OpenMontage.md` |
| 166 | hhvm | Duży upstreamowy runtime HHVM/JIT dla Hack z Proxygen/FastCGI i wieloma licencjami | ŚREDNI | `plan pracy/hhvm.md` |
| 167 | promptfoo | CLI/biblioteka do evals i red-teamingu LLM, CI/CD i code scanning | WYSOKI | `plan pracy/promptfoo.md` |
| 168 | unsloth | Desktop/Studio/Core do uruchamiania i treningu modeli lokalnych, MCP, RAG i API | KRYTYCZNY/WYSOKI | `plan pracy/unsloth.md` |
| 169 | bulk-email-scraper | Bardzo małe repozytorium; funkcja sugerowana przez nazwę wymaga potwierdzenia kodem | ŚREDNI | `plan pracy/bulk-email-scraper.md` |
| 170 | Nowe-projekty | Puste repozytorium przeznaczone potencjalnie na przyszłe projekty | KRYTYCZNY | `plan pracy/Nowe-projekty.md` |
| 171 | Cinematic-Agents | Mały prototyp o niepotwierdzonym stosie; nazwa wskazuje na agentów filmowych | ŚREDNI/WYSOKI | `plan pracy/Cinematic-Agents.md` |
| 172 | TorBot | Narzędzie OSINT/Tor o podwyższonym ryzyku dual-use | WYSOKI | `plan pracy/TorBot.md` |
| 173 | work-companion-pro | Mały prototyp narzędzia produktywności; stos wymaga dalszego mapowania | ŚREDNI | `plan pracy/work-companion-pro.md` |
| 174 | AI-Email-Generator | Bardzo mały generator e-maili AI; zakres wymaga mapowania | ŚREDNI | `plan pracy/AI-Email-Generator.md` |
| 175 | homebrew-engram | Minimalny kanał dystrybucji Homebrew dla Engram | NISKI/ŚREDNI | `plan pracy/homebrew-engram.md` |
| 176 | graphify | Knowledge graph repozytoriów z tree-sitter, zapytaniami/path/explain i integracją skills | WYSOKI | `plan pracy/graphify.md` |
| 177 | mars | Repo ~38 MB bez dostępnego README; zakres nie został zgadnięty | ŚREDNI | `plan pracy/mars.md` |

## Poprzednie audyty

Audyty 1–157 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 158–177 są opisane powyżej.

## Postęp

**177 / 299 repozytoriów — 59,20% audytu szczegółowego.**  
**122 repozytoria pozostają do audytu.**

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
