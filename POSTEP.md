# Rejestr postępu — ARCH-ENG-CORE-999

## Stan bieżący

- Data aktualizacji: 2026-09-12
- Faza: 1 — audyt globalny i rekonsyliacja
- Inwentaryzacja historyczna: 415 repozytoriów
- Aktualnie dostępne przez połączone konto GitHub: 100 repozytoriów
- Audyt szczegółowy: 390/415
- Ostatnia tura: 20 repozytoriów zweryfikowanych bez sztucznego zwiększania licznika
- Refaktoryzacja: oczekuje na wyniki audytu
- Polonizacja: oczekuje na kwalifikację zakresu
- Nowe projekty: zablokowane do czasu zamknięcia audytu istniejącego ekosystemu

## Rekonsyliacja

Historyczna liczba 415 i bieżący wynik 100 nie opisują tego samego zbioru w czasie. 415 to inwentaryzacja historyczna, natomiast 100 to repozytoria aktualnie zwracane przez połączone konto GitHub. Nie wolno utożsamiać różnicy 315 z brakującymi audytami.

Pozycje historyczne bez jednoznacznego odpowiednika pozostają `RECONCILIATION_REQUIRED`. Licznik 390/415 pozostaje bez zmian do czasu znalezienia dowodu brakującego, unikalnego audytu.

## Ostatnia tura — 20 repozytoriów

Zweryfikowano rzeczywistą zawartość README i dostępne informacje projektowe dla: `plasmic`, `budibase`, `grapesjs`, `ZeroAI`, `lonlybot`, `FastGPT`, `anything-llm`, `ragflow`, `visionclaw`, `Ptero`, `lore`, `PaulaAI`, `NetGuard`, `agent-command-center-sdk`, `FastRecvSMS`, `exiftool`, `chappie-bot`, `tempmail`, `OnlineSimBot2`, `26CP3600177-ai-email-generator`.

### Najważniejsze ustalenia

- `plasmic` — duży open-source visual builder/CMS; kluczowe są codegen, integracje z codebase, RBAC, webhooki i kontrola wersji pakietów.
- `budibase` — monorepo platformy operations/apps/agents/automations; krytyczne są API, integracje danych, uprawnienia i wykonywanie działań przez agentów.
- `grapesjs` — README nie został odczytany przez aktualny konektor; wymagane dalsze rozpoznanie drzewa przed dopisaniem nowych twierdzeń.
- `ZeroAI` — eksperymentalny Android AI agent Kotlin/Rust/UniFFI z usługą działającą w tle, kanałami Telegram/Discord/Messages, terminalem, SSH, MCP/pluginami i sandboxowanym Rhai; bardzo wysoki priorytet bezpieczeństwa.
- `lonlybot` — Next.js AI companion z wieloma providerami, pamięcią localStorage i silnie antropomorfizującym promptem; wymagają kontroli prywatności, sekretów, retencji oraz granic produktu.
- `FastGPT` — rozbudowana platforma Agent/RAG/Flow/MCP; dokumentacja zawiera domyślne dane logowania, co wymaga hardeningu wdrożeniowego.
- `anything-llm` — duża platforma desktop/web z agentami, MCP, scheduled tasks, RAG, multi-user i wieloma providerami; krytyczne są izolacja narzędzi, uprawnienia i sandbox.
- `ragflow` — duży RAG/agent engine z code executorem wymagającym sandboxa/gVisor; kluczowe są izolacja wykonania, sekrety, uploady i granice wielodostępności.
- `visionclaw` — visionOS/RealityKit voice AI companion z Bonjour/WebSocket bridge do Maca; krytyczne są zaufanie sieci lokalnej, autoryzacja i prywatność audio.
- `Ptero` — prosty multi-model AI chat z deklarowaną lokalną historią i integracją WordPress; trzeba zweryfikować rzeczywiste granice backendu i prywatności względem deklaracji README.
- `lore` — upstreamowy system kontroli wersji Epic Games, Rust/content-addressed/Merkle/binary-first; traktowany jako referencja technologiczna, nie projekt do sztucznego rebrandingu.
- `PaulaAI` — faktyczna zawartość to prosty Streamlit GDP dashboard, więc nazwa repozytorium nie odpowiada aktualnej funkcji; wymagane uporządkowanie tożsamości projektu.
- `NetGuard` — Android firewall oparty na VPNService; bezpieczeństwo polityki sieciowej, kompatybilność Androida i poprawność filtrowania są pierwszoplanowe.
- `agent-command-center-sdk` — Python/TypeScript SDK dla gatewaya OpenAI-compatible z routingiem, guardrailami, budżetami i integracjami frameworków; kluczowe są kontrakty SDK i bezpieczeństwo credentials.
- `FastRecvSMS` — CLI/MCP do zakupu numerów i odbioru SMS; pozostaje w ścisłym zakresie audytu bezpieczeństwa, zgodności i poprawności API, bez rozbudowy mechanizmów obchodzenia zabezpieczeń.
- `exiftool` — README nie został odczytany; dalsza klasyfikacja wymaga odczytu drzewa/plików.
- `chappie-bot` — historyczny wielofunkcyjny bot Python z licznymi komendami pobierania i mediami; wymaga klasyfikacji archiwalnej oraz przeglądu zależności/API.
- `tempmail` — README wskazuje minimalny interfejs narzędzia Trashx; wymaga sprawdzenia rzeczywistego kodu i zależności.
- `OnlineSimBot2` — bot Telegram wykorzystujący wirtualne numery i skrzynkę SMS; konfiguracja tokenu w pliku jest problemem bezpieczeństwa, a zakres użycia wymaga compliance review.
- `26CP3600177-ai-email-generator` — edukacyjny/template'owy projekt z niespójnym, szerokim opisem stacku i placeholderami; nie należy traktować deklarowanego backendu jako potwierdzonej implementacji.

## Sekwencja wykonawcza

### Etap 1 — audyt globalny

Dla każdego repozytorium należy ustalić strukturę, stack, build, punkt wejścia, konfigurację, CI/CD, testy, dokumentację, placeholdery, architekturę, sekrety, gotowość wdrożeniową, zakres polonizacji/rebrandingu oraz zależności ekosystemowe.

### Etap 2 — modernizacja

**AUDYT → PLAN ZMIAN → IMPLEMENTACJA → KOMPILACJA → TESTY → WERYFIKACJA → REBRANDING → POLONIZACJA → RAPORT → ZAMKNIĘCIE**

Nie oznaczać repozytorium jako zakończonego bez dowodu poprawnej implementacji i weryfikacji.

### Etap 3 — inkubacja nowych projektów

Po zamknięciu audytu istniejącego portfela wykorzystać `Knowledge-projects` jako źródło materiałów do projektowania nowych aplikacji, agentów, narzędzi i gier.

## Dziennik zmian

| Data | Repozytorium | Operacja | Wynik |
|---|---|---|---|
| 2026-09-11 | PLANY-I-POST-PY--W-REPOZYTORIACH | Utworzenie rejestru | OK |
| 2026-09-11 | wszystkie 100 repozytoriów | Inwentaryzacja globalna | OK |
| 2026-09-12 | 27 repozytoriów | Weryfikacja README + porównanie planów | OK — bez podwójnego naliczenia |
| 2026-09-12 | PLANY-I-POST-PY--W-REPOZYTORIACH | Rekonsyliacja 415 vs 100 | OK — licznik 390/415 zachowany |
| 2026-09-12 | 20 repozytoriów | Weryfikacja README + klasyfikacja | OK — bez podwójnego naliczenia |

## Reguła integralności

Ten rejestr jest źródłem stanu procesu. Każda zakończona jednostka pracy powinna otrzymać wpis z datą, repozytorium, operacją i wynikiem. Stan repozytorium nie może być oznaczony jako produkcyjny na podstawie samego przeglądu metadanych.
