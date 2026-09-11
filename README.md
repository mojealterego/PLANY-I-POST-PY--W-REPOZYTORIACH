# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** 205  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — 205 repozytoriów |
| Audyt szczegółowy | W TOKU |
| Plany pracy | TWORZONE SEKWENCYJNIE |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANego REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Audyty zakończone w tej sesji

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 1 | ai-game-builder | Projekt Unity; README minimalne; `Assets`, `Packages`, `.github`; manifest zawiera Ads i IAP | KRYTYCZNY | `plan pracy/ai-game-builder.md` |
| 2 | AURELIS-AI | Dojrzała aplikacja Next.js/React/AI; PostgreSQL/Drizzle/Auth/Blob/Playwright/OTel; polski-first | KRYTYCZNY | `plan pracy/AURELIS-AI.md` |
| 3 | kernel-browser-automation-starter | Starter Next.js + Kernel + AI SDK; automatyzacja przeglądarki sterowana agentem | WYSOKI | `plan pracy/kernel-browser-automation-starter.md` |
| 4 | CzatBotSingularity | Repozytorium puste | KRYTYCZNY | `plan pracy/CzatBotSingularity.md` |
| 5 | system-prompts-and-models-of-ai-tools | Duży katalog wiedzy/promtów; README zawiera treści sponsorskie, finansowe i zewnętrzne linki | WYSOKI | `plan pracy/system-prompts-and-models-of-ai-tools.md` |
| 6 | lucidrag | Rozbudowana platforma .NET 10 RAG; multimodalność, GraphRAG, multi-tenancy, lokalne modele | KRYTYCZNY | `plan pracy/lucidrag.md` |
| 7 | tuskbot | Agent Go dla Telegrama; MCP, lokalny RAG, llama.cpp/GGUF, SQLite-vec, shell/filesystem | KRYTYCZNY | `plan pracy/tuskbot.md` |
| 8 | reor | Lokalny desktopowy PKM/RAG; Ollama, Transformers.js, LanceDB, AGPL-3.0 | WYSOKI | `plan pracy/reor.md` |
| 9 | Kalynt | Rozbudowany projekt wielopakietowy; ARCHITECTURE/CHANGELOG/SECURITY, apps/packages/examples | KRYTYCZNY | `plan pracy/Kalynt.md` |
| 10 | enklayve | Tauri 2 + React/TS + Rust; lokalne LLM, szyfrowanie, biometria, dokumenty, GPU | KRYTYCZNY | `plan pracy/enklayve.md` |
| 11 | CCR-WORLD | Minimalny stan dokumentacyjny; README tylko „GAME AAA ANDROIFD” | KRYTYCZNY | `plan pracy/CCR-WORLD.md` |

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
