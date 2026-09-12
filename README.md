# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **376**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKTUALIZOWANA — **376 repozytoriów** |
| Audyt szczegółowy | W TOKU — **337/376** |
| Plany pracy | UTWORZONE — **337/376** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty — przebieg po wykryciu 376 repozytoriów

Po ponownej inwentaryzacji potwierdzono **376 repozytoriów**. W tej turze dodano **20 nowych, unikalnych planów**, podnosząc stan z 317 do **337/376**. Repozytoria posiadające wcześniejsze plany nie zostały ponownie doliczone.

| Nr | Repozytorium | Wynik audytu | Priorytet |
|---:|---|---|---|
| 318 | termux-app | Upstream Android terminal; build/release, pluginy, signing i supply chain | WYSOKI/REFERENCYJNY |
| 319 | TaskingAI | BaaS dla agentów LLM; FastAPI, multi-tenancy, tools, RAG, Docker i SDK | KRYTYCZNY |
| 320 | langflow | Visual AI workflow/agent builder; API, MCP, custom Python components i deployment | KRYTYCZNY/REFERENCYJNY |
| 321 | OpenLLM | Runtime/serwer LLM; API, modele, zasoby GPU i deployment | WYSOKI/REFERENCYJNY |
| 322 | datadog-agent | Duży agent obserwowalności; collectors, permissions, telemetry i integracje | WYSOKI/REFERENCYJNY |
| 323 | lume | Duże repozytorium web/3D; renderowanie, assety i build | ŚREDNI/WYSOKI/REFERENCYJNY |
| 324 | UserLAnd | Linux na Androidzie; procesy, filesystem, sieć i integracja systemowa | WYSOKI/REFERENCYJNY |
| 325 | openinterpreter | Agent z wykonaniem kodu i działań systemowych | KRYTYCZNY |
| 326 | AutoGPT | Autonomiczny agent z planowaniem, pamięcią i narzędziami | KRYTYCZNY |
| 327 | SuperAGI | Platforma agentowa z narzędziami/pamięcią i wykonaniem | KRYTYCZNY/REFERENCYJNY |
| 328 | ChatDev | Wieloagentowy development i generowanie artefaktów | KRYTYCZNY |
| 329 | OGAM | On-device AI Android/iOS/macOS; LLM, vision, audio, tools i MCP | KRYTYCZNY |
| 330 | Cz-owiek-Roku-Film | Kanoniczne repozytorium produkcji filmu AI; source-lock i continuity-lock | KRYTYCZNY |
| 331 | google-analytics-mcp | Eksperymentalny MCP dla Google Analytics; OAuth/ADC i read-only API | WYSOKI |
| 332 | mailtm_client | Dart wrapper mail.tm; konta, JWT, wiadomości i załączniki | ŚREDNI/WYSOKI |
| 333 | ComfyUI-LTXVideo | Custom nodes/workflows dla LTX-2.3; modele, LoRA, HDR, audio/video | WYSOKI/REFERENCYJNY |
| 334 | rust-sdk | SDK Rust; publiczne API, Cargo, kompatybilność i testy | ŚREDNI/WYSOKI |
| 335 | agents | Komponenty agentowe; runtime, tools, policy i observability | WYSOKI |
| 336 | maid | Android React Native; llama.cpp/GGUF, remote LLM, Supabase i model downloads | KRYTYCZNY |
| 337 | actions | GitHub Actions dla repozytoriów MCP; deploy, cleanup i automatyczny merge | KRYTYCZNY DLA CI/CD |

## Dodatkowe ustalenia tej tury

- Przed dodaniem batcha ponownie pobrano aktualną inwentaryzację; portfel nadal wynosi **376 repozytoriów**.
- Kandydaci z istniejącymi planami nie zostali doliczeni ponownie. Próby zapisu do istniejących planów zwracały konflikt SHA i były traktowane jako duplikaty.
- Dla nowych pozycji sprawdzono dostępność repozytorium oraz, gdzie było to wymagane, rzeczywistą zawartość README przed przygotowaniem planu.
- Szczególną uwagę poświęcono execution boundaries, credentials, MCP, signing, model provenance i prywatności danych.

## Poprzednie audyty

Audyty 1–317 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Numeracja audytów jest numeracją rejestrową; przy kolejnych turach licznik ma być zwiększany wyłącznie o nowe, unikalne repozytoria.

## Postęp

**337 / 376 repozytoriów — 89,63% audytu szczegółowego.**  
**39 repozytoriów pozostaje do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **376 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
