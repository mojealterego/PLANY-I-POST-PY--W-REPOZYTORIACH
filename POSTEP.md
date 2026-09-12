# Rejestr postępu — ARCH-ENG-CORE-999

## Stan bieżący

- Data aktualizacji: 2026-09-12
- Faza: 1 — audyt globalny i rekonsyliacja
- Inwentaryzacja historyczna: 415 repozytoriów
- Aktualnie dostępne przez połączone konto GitHub: 100 repozytoriów
- Audyt szczegółowy: 390/415
- Ostatnia tura: 20 repozytoriów poddanych analizie; licznik audytu nie został sztucznie zwiększony
- Refaktoryzacja: oczekuje na zamknięcie audytu
- Polonizacja: oczekuje na kwalifikację zakresu
- Nowe projekty: zablokowane do czasu zamknięcia audytu istniejącego ekosystemu

## Rekonsyliacja

Historyczne 415 i bieżące 100 nie są tym samym zbiorem w czasie. Różnica 315 nie jest automatycznie liczbą brakujących audytów. Pozycje bez jednoznacznego obecnego odpowiednika pozostają `RECONCILIATION_REQUIRED`. Licznik 390/415 pozostaje bez zmian do czasu znalezienia dowodu brakującego, unikalnego audytu.

## Tura 2026-09-12 — 20 analiz

### 13 nowych pozycji bieżącego portfela

1. `openai-cookbook` — upstream/reference; rozbudowany katalog przykładów OpenAI API. Kluczowe: provenance przykładów, bezpieczne obchodzenie się z `OPENAI_API_KEY`, rozdzielenie dokumentacji od gwarancji produkcyjnych.
2. `agent-learning-kit` — SDK ewaluacji LLM/agentów: metryki lokalne, LLM-as-judge, guardrails, streaming, AutoEval, feedback/ChromaDB, OTel i backendy rozproszone. Deklaracje wydajnościowe i bezpieczeństwa wymagają reprodukcji; szczególna uwaga na dane wejściowe, PII i telemetrykę.
3. `actions` — zestaw własnych GitHub Actions dla repozytoriów MCP: preview/cleanup Cloudflare Pages, Hugo build oraz slash commands z label/approve/auto-merge. Krytyczne: minimalne uprawnienia GITHUB_TOKEN, walidacja komend i bezpieczne granice automatycznego merge.
4. `Feng-Grants` — repozytorium puste; klasyfikacja `EMPTY/BOOTSTRAP`. Nie tworzyć fikcyjnej zawartości.
5. `ID-Xbox-Grants` — pakiet aplikacyjny „Pieśń Zapomnianych” dla ID@Xbox; grant/pre-submission. Mocna polityka rozdzielenia faktów platformowych od założeń; przed wysłaniem wymagany aktualny fact-check Microsoft/Xbox.
6. `Unity-Grants` — NeuroAdapt AI; grant-facing research foundation dla rehabilitacji/protez/XR. Nie jest oprogramowaniem klinicznie potwierdzonym. A.U.R.A. może adaptować parametry zadań, ale nie diagnozować ani przepisywać terapii. Wymagana governance medyczna, prywatność i dowody kliniczne.
7. `Roblox-Grants` — README nieobecny; klasyfikacja `MINIMAL/NO-README`, do dalszej rekonsyliacji zawartości przed jakąkolwiek modernizacją.
8. `South-Park-Grants` — NeuroSteer; research-stage middleware do activation steering/SAE. Hipotezy są wyraźnie oddzielone od wyników; wymagane benchmarki rekonstrukcji, efektu przyczynowego, latency, pamięci i replikacji. Nie przedstawiać latent steering jako gwarancji bezpieczeństwa/PII.
9. `Neo-residency-Grants` — Aegis State Management; referencyjna implementacja trwałego stanu, checkpointów, optimistic concurrency i replay. Wyraźnie nieprodukcyjna. Braki: produkcyjna persystencja, distributed consensus/locking, enterprise security i dowód przewagi wydajnościowej.
10. `Fellowship-Grants` — LuminaCore; research-stage photonic neuromorphic edge AI. Poprawnie rozdziela E0–E4 evidence. Kluczowe ryzyka: nonlinear response, optical loss, ADC/DAC/control overhead, thermal drift, fabrication variability i packaging.
11. `Anthropic-Grants` — reproducible research scaffold dla subliminal transfer/mechanistic interpretability. Eksperymenty unsafe mają pozostać syntetyczne i sandboxowane. Walidacja wymaga model/checkpoint, dataset, split, seed, revision, uncertainty i manifestu.
12. `Hound-Grants` — HOUND benchmark long-horizon agents pod kątem procedural compliance, authorization, provenance i approval. Benchmark ma działać w izolowanych syntetycznych środowiskach; nie łączyć z produkcją, realnymi credentialami ani nieautoryzowanymi celami.
13. `Knowledge-projects` — centralna baza wiedzy i specyfikacji projektów. Aktualny materiał zawiera m.in. Project 81 Voice-Narrative AI Game Engine MAX oraz Project 72 OmniCore assurance. Obowiązują zasady: capability ≠ authorization, approval ≠ execution, simulation ≠ evidence, unknown authority → fail closed, a projektowa tożsamość jest rozwiązywana przez lineage.

### 7 kontroli pogłębionych w bieżącym portfelu

14. `AURELIS-AI` — potwierdzono spójność produktu premium/Polish-first z Next.js 16, React 19, AI SDK, Drizzle/PostgreSQL, Auth.js, Blob, Playwright i OTel. Security baseline wymaga untrusted-input handling, authz na routes, secret isolation i jawnego approval dla działań konsekwencyjnych.
15. `lucidrag` — aktywnie rozwijana platforma .NET 10 RAG z multimodalnymi pipeline'ami, GraphRAG, model routingiem i multi-tenancy. Deklaracje typu sub-50ms oraz enterprise-ready wymagają benchmarków i testów; szczególnie ważne są tenant isolation, upload/SSRF, credentials i granice pluginów.
16. `tuskbot` — Go autonomous agent dla Telegrama z MCP, lokalnym RAG, filesystemem i shell execution. Owner ID i workspace boundary są krytyczne; shell/filesystem/MCP wymagają capability-level authorization, sandboxingu i audytowalnych operacji.
17. `reor` — lokalny desktop PKM/RAG; dane mają pozostać lokalne, ale pobieranie modeli i integracje OpenAI-compatible są zaufaniem zewnętrznym. Wymagane: provenance modeli, bezpieczny download, sandbox filesystemu i weryfikacja deklaracji prywatności.
18. `enklayve` — Tauri 2 + React/Rust lokalna analiza dokumentów, szyfrowanie i biometria deklarowane jako podstawowe funkcje. README zawiera instrukcję usuwania quarantine z aplikacji na macOS oraz placeholderowe URL-e repozytorium; wymaga weryfikacji podpisywania, aktualnych zależności i zgodności deklaracji „100% offline” z implementacją.
19. `hermes-agent` — duży wieloplatformowy agent z terminalem, gatewayami komunikacyjnymi, pamięcią, skillami, cronem, subagentami i wieloma backendami wykonawczymi. Najwyższy priorytet: command approval, pairing/identity, izolacja backendów, secrets migration, skill integrity i granice autonomicznego działania.
20. `omega7-messenger` / `JARVIS-2.0` / `AgentGPT` — trzy pogłębione kontrole bezpieczeństwa i gotowości wykonane w tej turze jako grupa kontrolna. `omega7-messenger` nadal nie jest certyfikowanym E2EE; `JARVIS-2.0` pozostaje foundation z JSON state i wymaga dalszego hardeningu backendu; `AgentGPT` pozostaje upstream/reference-style autonomous-agent application z szerokim zakresem narzędzi i wymaga izolacji oraz weryfikacji stanu względem bieżącej gałęzi.

> Uwaga: pozycja 20 obejmuje trzy repozytoria kontrolne, dlatego fizycznie przeanalizowano 22 repozytoria w tej turze. Do dziennika jakościowego tura pozostaje zapisana jako 20 jednostek audytowych: 13 nowych + 7 bloków kontroli. Licznik 390/415 nie został zwiększony.

## Zidentyfikowane priorytety

- `CRITICAL/HIGH`: agenci z shell/filesystem/MCP, mobilni agenci Accessibility, PBX/SIP, pamięć agentów, uploady/SSRF, narzędzia bezpieczeństwa oraz systemy wykonujące działania konsekwencyjne.
- `REFERENCE/UPSTREAM`: OpenAI Cookbook i inne przejęte projekty upstreamowe nie powinny być ślepo rebrandowane.
- `RESEARCH`: grant/research repositories wymagają evidence ledger, reproducibility i ścisłego rozdzielenia hipotez od faktów.
- `EMPTY/MINIMAL`: puste repozytoria należy kwalifikować, a nie wypełniać fikcyjną implementacją.

## Ostatnie wcześniejsze tury

- `ToolJet`, `babyagi`, `sim`, `sannabotapp`, `builder-www`, `futureagi-sdk`, `MATS-Grants`, `skills`, `engram`, `EchoPBX`, `softphone`, `freemail`, `mailtm-client`, `compose-multiplatform`, `eSim`, `AI_Offensive_MCP_Using_KaliLinux`, `Agent-Android`, `MaxKB`, `llm-graph-builder`, `Local-Diffusion` — zweryfikowane w poprzedniej turze.
- Wcześniejsze audyty obejmują m.in. `ai-game-builder`, `AURELIS-AI`, `kernel-browser-automation-starter`, `lucidrag`, `tuskbot`, `reor`, `Kalynt`, `enklayve`, `omega7-messenger`, `JARVIS-2.0`, `hermes-agent`, `gptAssist`, `simplex-chat`, `element-x-android`, `AgentGPT`, `mcp-coding-agent`, `Knowledge-projects` oraz wiele kolejnych pozycji portfolio.

## Sekwencja wykonawcza

### Etap 1 — audyt globalny

Dla każdego repozytorium ustalić strukturę, stack, build, entry point, konfigurację, CI/CD, testy, dokumentację, placeholdery, architekturę, sekrety, gotowość wdrożeniową, zakres rebrandingu/polonizacji oraz zależności ekosystemowe.

### Etap 2 — modernizacja

**AUDYT → PLAN ZMIAN → IMPLEMENTACJA → KOMPILACJA → TESTY → WERYFIKACJA → REBRANDING → POLONIZACJA → RAPORT → ZAMKNIĘCIE**

Nie oznaczać repozytorium jako produkcyjne na podstawie samego audytu.

### Etap 3 — inkubacja nowych projektów

Po zamknięciu audytu wykorzystać `Knowledge-projects` jako źródło materiałów do projektowania nowych aplikacji, agentów, narzędzi i gier.

## Dziennik zmian

| Data | Zakres | Operacja | Wynik |
|---|---|---|---|
| 2026-09-11 | PLANY-I-POST-PY--W-REPOZYTORIACH | Utworzenie rejestru | OK |
| 2026-09-11 | wszystkie 100 repozytoriów | Inwentaryzacja globalna | OK |
| 2026-09-12 | 27 repozytoriów | Weryfikacja README + porównanie planów | OK — bez podwójnego naliczenia |
| 2026-09-12 | 415 vs 100 | Rekonsyliacja | OK — licznik 390/415 zachowany |
| 2026-09-12 | 20 repozytoriów | README + klasyfikacja | OK — bez podwójnego naliczenia |
| 2026-09-12 | 20 repozytoriów | README + architektura | OK — bez podwójnego naliczenia |
| 2026-09-12 | 20 repozytoriów | README + bezpieczeństwo/architektura | OK — bez podwójnego naliczenia |
| 2026-09-12 | 13 nowych + 7 bloków kontroli | Audyt pogłębiony bieżącego portfela | OK — licznik 390/415 zachowany |

## Reguła integralności

Ten rejestr jest źródłem stanu procesu. Każda zakończona jednostka pracy otrzymuje wpis z datą, zakresem, operacją i wynikiem. Stan repozytorium nie może być oznaczony jako produkcyjny na podstawie samego przeglądu metadanych.
