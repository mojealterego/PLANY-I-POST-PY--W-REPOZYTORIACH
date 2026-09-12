# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **319**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — **319 repozytoriów** |
| Audyt szczegółowy | W TOKU — **217/319** |
| Plany pracy | UTWORZONE — **217/319** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty — 198–217

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 198 | alexandria-audiobook | Lokalny generator audiobooków: LLM, Qwen3-TTS, voice cloning, LoRA, Docker/Colab | WYSOKI | `plan pracy/alexandria-audiobook.md` |
| 199 | Shadowbroker | Platforma geospatial OSINT z FastAPI/Next.js, Shodan, recon i kanałem agentowym | KRYTYCZNY | `plan pracy/Shadowbroker.md` |
| 200 | builder | Duże monorepo buildera z Nx/Yarn, EAS, przykładami i systemem zmian | WYSOKI | `plan pracy/builder.md` |
| 201 | langchain | Duży framework agentowy/LLM i ekosystem integracji | WYSOKI/REFERENCYJNY | `plan pracy/langchain.md` |
| 202 | ComfyUI-audio | Eksperymentalne rozszerzenie audio dla ComfyUI; development wstrzymany | NISKI/ŚREDNI | `plan pracy/ComfyUI-audio.md` |
| 203 | AhMyth-Android-RAT | Android RAT: panel Electron + backdoor; tylko analiza defensywna/laboratoryjna | KRYTYCZNY | `plan pracy/AhMyth-Android-RAT.md` |
| 204 | agnes-ai-video-suite | EchoSync — self-hosted prototyper wideo z TTS, napisami i avatarem | WYSOKI | `plan pracy/agnes-ai-video-suite.md` |
| 205 | MumbleLink | Klientowy mod Minecraft Forge dla positional audio Mumble | NISKI/ŚREDNI | `plan pracy/MumbleLink.md` |
| 206 | unity-mcp | MCP dla Unity: 47 narzędzi do scen, assetów, kodu, testów i buildów | KRYTYCZNY | `plan pracy/unity-mcp.md` |
| 207 | USB-Uncensored-LLM | Przenośne lokalne AI z Ollama/GGUF, skryptami wieloplatformowymi i UI LAN | WYSOKI | `plan pracy/USB-Uncensored-LLM.md` |
| 208 | agent | 1MCP unified runtime: agregacja MCP, CLI, filtrowanie i progressive discovery | KRYTYCZNY | `plan pracy/agent.md` |
| 209 | Claude-Code-Game-Studios | System 49 agentów, 73 skills, hooks, rules i templates dla produkcji gier | WYSOKI | `plan pracy/Claude-Code-Game-Studios.md` |
| 210 | krypton-byte.github.io | GitProfile: React/Vite automatyczny builder portfolio GitHub | ŚREDNI | `plan pracy/krypton-byte.github.io.md` |
| 211 | baresip-studio | Android SIP/VoIP user agent oparty na baresip/libbaresip | WYSOKI | `plan pracy/baresip-studio.md` |
| 212 | GDevelop | Duży no-code silnik/IDE 2D/3D/multiplayer z React/Electron/WASM | WYSOKI/REFERENCYJNY | `plan pracy/GDevelop.md` |
| 213 | getbelmo | MCP CLI do auth, workspace, GitHub, deploymentów, env vars i domen | KRYTYCZNY | `plan pracy/getbelmo.md` |
| 214 | citibank-van | Historyczny nieoficjalny klient Citibank Virtual Account Numbers | KRYTYCZNY | `plan pracy/citibank-van.md` |
| 215 | eSIM-Tools | Webowe narzędzie eSIM dla Giffgaff/Simyo z auth/OTP i QR | KRYTYCZNY | `plan pracy/eSIM-Tools.md` |
| 216 | elevenlabs-android | Oficjalny SDK ElevenAgents dla Android/Kotlin, LiveKit/WebRTC i WebSocket | WYSOKI | `plan pracy/elevenlabs-android.md` |
| 217 | ai-email-generator-2 | React/Vite + Express + Supabase + LLM generator wiadomości | ŚREDNI/WYSOKI | `plan pracy/ai-email-generator-2.md` |

## Poprzednie audyty

Audyty 1–197 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 198–217 zostały dodane w bieżącym przebiegu.

## Postęp

**217 / 319 repozytoriów — 68,03% audytu szczegółowego.**  
**102 repozytoria pozostają do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **319 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
