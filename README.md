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
| Audyt szczegółowy | W TOKU — **61/293** |
| Plany pracy | UTWORZONE — **61/293** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 52 | Agentic-Cinema-The-Blockbuster-Hackathon | StudioSync: agentowa warstwa odzyskiwania produkcji filmowej; deterministyczne demo jest rozdzielone od live, ale live runner/session ADK wymaga dokończenia | KRYTYCZNY | `plan pracy/Agentic-Cinema-The-Blockbuster-Hackathon.md` |
| 53 | Nebius-x-NVIDIA-Global-AI-Hackathon | InfraSentinel: evidence-first SRE z deterministyczną polityką, governance i symulatorem; realna infrastruktura wymaga osobnych adapterów i kontroli blast radius | KRYTYCZNY | `plan pracy/Nebius-x-NVIDIA-Global-AI-Hackathon.md` |
| 54 | ChatGPT-CodeReview | Probot/GitHub Action do automatycznego code review; historyczna dokumentacja, szerokie permissions w przykładzie i błędne `homepage` wymagają uporządkowania | WYSOKI | `plan pracy/ChatGPT-CodeReview.md` |
| 55 | AgentGPT | Duży system webowy do uruchamiania agentów autonomicznych; historyczny stos Next/FastAPI wymaga aktualizacji i ponownej weryfikacji granic narzędzi | KRYTYCZNY | `plan pracy/AgentGPT.md` |
| 56 | mcp-coding-agent | Builder agentów i oprogramowania przez MCP; silne ograniczenia workspace, ale potrzebna twarda izolacja wykonania niezaufanego kodu | KRYTYCZNY | `plan pracy/mcp-coding-agent.md` |
| 57 | agent-command-center-sdk | SDK Python/TypeScript z integracjami frameworków; wymaga kontraktów OpenAI-compatible, testów niezależnych od gatewaya i audytu sekretów/endpointów | KRYTYCZNY | `plan pracy/agent-command-center-sdk.md` |
| 58 | llm-graph-builder | FastAPI + React + Neo4j, wieloźródłowy RAG/Knowledge Graph i wielu providerów LLM; istotne granice auth, uploadów, URL fetch i izolacji danych | KRYTYCZNY | `plan pracy/llm-graph-builder.md` |
| 59 | Local-Diffusion | Flutter/Android, lokalna inferencja diffusion, FFI i wiele formatów modeli; konieczne testy urządzeniowe, integralność modeli i reprodukowalność benchmarków | WYSOKI | `plan pracy/Local-Diffusion.md` |
| 60 | cookbooks | Katalog niezależnych przykładów AI/RAG/agentów; wartość referencyjna wysoka, wymagane indeksowanie statusów i zależności zamiast wspólnej refaktoryzacji | ŚREDNI | `plan pracy/cookbooks.md` |
| 61 | locally-uncensored | Duże desktopowe studio lokalnego AI z Tauri, ComfyUI, coding agentem i wieloma backendami; krytyczna powierzchnia subprocess/MCP/model downloads | KRYTYCZNY | `plan pracy/locally-uncensored.md` |

## Poprzednie audyty

Audyty 1–51 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 52–61 są opisane powyżej.

## Postęp

**61 / 293 repozytoriów — 20,82% audytu szczegółowego.**  
**232 repozytoria pozostają do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **293 repozytoria**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
