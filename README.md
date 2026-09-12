# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **415**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKTUALIZOWANA — **415 repozytoriów** |
| Audyt szczegółowy | W TOKU — **368/415 (88,67%)** |
| Plany pracy | UTWORZONE — **368/415** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnia tura — 20 repozytoriów zweryfikowanych

W tej turze przeanalizowano rzeczywistą zawartość 20 repozytoriów. Pięć pozycji miało już wcześniej utworzone plany i dlatego nie zostało ponownie doliczonych.

Nowe, unikalne plany utworzone w tej turze:

| Nr | Repozytorium | Wynik audytu | Priorytet |
|---:|---|---|---|
| 354 | duix-doc | Dokumentacja Mintlify; publikacja zależna od synchronizacji GitHub App | ŚREDNI |
| 355 | webstudio | Visual development platform; AGPL core + proprietary package | WYSOKI |
| 356 | open-router-android-client | Android/Kotlin Clean Architecture; Room, Retrofit, Hilt, OpenRouter | WYSOKI |
| 357 | ext-skills | Eksperymentalne Skills Over MCP; SEP-2640, threat model | WYSOKI/REFERENCYJNY |
| 358 | Ptero | Wielomodelowy czat AI + WordPress/PHP; lokalny storage | WYSOKI |
| 359 | Meta3D | Low-code Web3D editor/engine/platform | WYSOKI |
| 360 | Llamatik | Kotlin Multiplatform; llama.cpp, whisper.cpp, stable-diffusion.cpp | KRYTYCZNY |
| 361 | autogen | Microsoft multi-agent framework; maintenance mode | WYSOKI/REFERENCYJNY |
| 362 | anything-llm | RAG/Agents/MCP/multi-user; Vite/React + Node/Express | KRYTYCZNY |
| 363 | ragflow | RAG engine z agentami, MCP i code executor sandbox | KRYTYCZNY |
| 364 | visionclaw | visionOS/RealityKit; 3D AI companion, STT/TTS, Bonjour/WebSocket | KRYTYCZNY |
| 365 | AI_Offensive_MCP_Using_KaliLinux | MCP bridge do Kali, narzędzia ofensywne i Metasploit | KRYTYCZNY — LAB ONLY |
| 366 | Librechat-Mobile | Natywny klient Android/iOS LibreChat; KMP, secure storage, SSE, MCP | KRYTYCZNY |
| 367 | nocodb | No-code database; RBAC, REST/SDK, automatyzacje | KRYTYCZNY |
| 368 | OpenConstructionERP | ERP budowlany; BOQ/BIM/4D/5D, 195 modułów, AGPL | KRYTYCZNY |

Repozytoria sprawdzone w tej turze, ale posiadające już plan: `open-agent-platform`, `alexandria-audiobook`, `open-agent-builder`, `AutoGPT`, `termux-app`.

## Najważniejsze obserwacje

- `open-agent-platform` jest zdeprecjonowany i powinien pozostać materiałem referencyjnym.
- `autogen` jest w maintenance mode; nowe prace należy kierować do Microsoft Agent Framework.
- `anything-llm` i `ragflow` mają dużą powierzchnię integracyjną: agenci, MCP, dokumenty, vector DB, providerzy i wielodostępność.
- `AI_Offensive_MCP_Using_KaliLinux` może wykonywać polecenia na hoście Kali; utrzymujemy wyłącznie granicę autoryzowanego laboratorium.
- `visionclaw` wymaga kontroli kanału Vision Pro↔Mac, Bonjour, WebSocket oraz danych głosowych.
- `Llamatik` ma natywną warstwę C++ i wieloplatformowe zarządzanie modelami; kluczowe są lifecycle, concurrency, pamięć i provenance modeli.
- `OpenConstructionERP` ma dużą powierzchnię modułową i dane biznesowe; konieczne są testy RBAC, izolacji projektów, importów i release chain.

## Postęp

**368 / 415 repozytoriów — 88,67% audytu szczegółowego.**  
**47 repozytoriów pozostaje do jednoznacznego rozliczenia/audytu.**

Wzrost liczby repozytoriów z 376 do 415 został wykryty w aktualnej inwentaryzacji GitHub. Nowe repozytoria nie są automatycznie uznawane za zbadane.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko nazwy i metadanych. Dla dużych repozytoriów analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. Projekty archiwalne i dokumentacyjne są dodatkowo oceniane pod kątem aktualności i pochodzenia.

## Klasy priorytetów

- **KRYTYCZNY** — duże ryzyko architektoniczne/bezpieczeństwa albo wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający modernizacji, polonizacji lub zabezpieczenia.
- **ŚREDNI** — projekt użyteczny bez natychmiastowej blokady ekosystemu.
- **NISKI** — referencje, archiwa, katalogi lub projekty o ograniczonym zakresie.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
