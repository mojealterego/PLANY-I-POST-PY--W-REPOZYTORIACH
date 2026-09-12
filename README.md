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
| Audyt szczegółowy | W TOKU — **66/293** |
| Plany pracy | UTWORZONE — **66/293** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 57 | agent-command-center-sdk | SDK Python/TypeScript z integracjami frameworków; wymagane kontrakty OpenAI-compatible, testy niezależne od gatewaya i audyt sekretów/endpointów | KRYTYCZNY | `plan pracy/agent-command-center-sdk.md` |
| 58 | llm-graph-builder | FastAPI + React + Neo4j, wieloźródłowy RAG/Knowledge Graph i wielu providerów LLM; istotne granice auth, uploadów, URL fetch i izolacji danych | KRYTYCZNY | `plan pracy/llm-graph-builder.md` |
| 59 | Local-Diffusion | Flutter/Android, lokalna inferencja diffusion, FFI i wiele formatów modeli; konieczne testy urządzeniowe, integralność modeli i reprodukowalność benchmarków | WYSOKI | `plan pracy/Local-Diffusion.md` |
| 60 | cookbooks | Katalog niezależnych przykładów AI/RAG/agentów; wartość referencyjna wysoka, wymagane indeksowanie statusów i zależności zamiast wspólnej refaktoryzacji | ŚREDNI | `plan pracy/cookbooks.md` |
| 61 | locally-uncensored | Duże desktopowe studio lokalnego AI z Tauri, ComfyUI, coding agentem i wieloma backendami; krytyczna powierzchnia subprocess/MCP/model downloads | KRYTYCZNY | `plan pracy/locally-uncensored.md` |
| 62 | hermes-agent | Duży wieloplatformowy agent z terminalem, MCP, skills/plugins, gatewayami i sandboxami; OS isolation jest rzeczywistą granicą bezpieczeństwa | KRYTYCZNY | `plan pracy/hermes-agent.md` |
| 63 | gptAssist | Lekki klient Android/WebView dla ChatGPT; kluczowe są allowlista URL, WebView, uploady, intenty i modernizacja SDK | WYSOKI | `plan pracy/gptAssist.md` |
| 64 | simplex-chat | Bardzo duży komunikator wieloplatformowy z kryptografią i Haskell; wymagane audyty protokołu, FFI, storage, zależności Git i reprodukowalności | KRYTYCZNY | `plan pracy/simplex-chat.md` |
| 65 | element-x-android | Duży klient Matrix Android oparty o Compose i Matrix Rust SDK; krytyczne FFI, E2EE, storage, release i separacja upstream/własne zmiany | KRYTYCZNY | `plan pracy/element-x-android.md` |
| 66 | strykerapp | Rootowana aplikacja pentestowa Android z chroot, root/su, Wi-Fi/BLE, USB HID, Metasploit i innymi narzędziami; wymaga ścisłych granic laboratoryjnych | KRYTYCZNY | `plan pracy/strykerapp.md` |

## Poprzednie audyty

Audyty 1–56 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 57–66 są opisane powyżej.

## Postęp

**66 / 293 repozytoriów — 22,53% audytu szczegółowego.**  
**227 repozytoriów pozostaje do audytu.**

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
