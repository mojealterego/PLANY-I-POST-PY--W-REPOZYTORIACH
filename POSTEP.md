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

Zweryfikowano rzeczywistą zawartość README i dostępne informacje projektowe dla: `ToolJet`, `babyagi`, `sim`, `sannabotapp`, `builder-www`, `futureagi-sdk`, `MATS-Grants`, `skills`, `engram`, `EchoPBX`, `softphone`, `freemail`, `mailtm-client`, `compose-multiplatform`, `eSim`, `AI_Offensive_MCP_Using_KaliLinux`, `Agent-Android`, `MaxKB`, `llm-graph-builder`, `Local-Diffusion`.

### Najważniejsze ustalenia

- `ToolJet` — duża platforma low-code/internal tools z AI, MCP, JS/Python execution, integracjami danych, RBAC i środowiskami; kluczowe są izolacja wykonywania kodu, uprawnienia agentów, sekrety i granice danych.
- `babyagi` — eksperymentalny framework self-building agenta z bazą funkcji, zależnościami, sekretami, triggerami i generowaniem kodu; README jawnie oznacza projekt jako eksperymentalny i nieprodukcyjny. Priorytet: sandbox, autoryzacja i kontrola rekurencyjnych/automatycznych wykonań.
- `sim` — rozbudowana platforma budowania/deployowania agentów i workflowów z Next.js/Bun/PostgreSQL, Better Auth, E2B i isolated-vm; krytyczne są sekrety, izolacja kodu, jobs, integracje i uprawnienia.
- `sannabotapp` — Android voice-first agent wykonujący działania przez Accessibility, scheduler i sub-agentów; bardzo wysoki priorytet bezpieczeństwa: zgody użytkownika, ograniczenie działań wysokiego skutku, ochrona danych lokalnych i lifecycle usług w tle.
- `builder-www` — Frappe Builder, low-code website builder z AI page generation, CMS, scriptingiem i one-click publishing; upstream/reference, nie należy ślepo rebrandować. Szczególna uwaga na wykonywanie skryptów, CSRF i domyślne dane developerskie.
- `futureagi-sdk` — SDK Python/TypeScript dla ewaluacji, guardrails, prompt versioning, RAG i observability; deklarowane benchmarki typu sub-100ms wymagają reprodukcji przed użyciem jako twierdzenia produkcyjne.
- `MATS-Grants` — dossier badawcze z bezpiecznym syntetycznym vertical slice; wyraźna granica między infrastrukturą badawczą a dowodem dotyczącym scheming/deceptive alignment. Zachować provenance, reproducibility i niezależne autorstwo aplikacji zgodnie z aktualnymi zasadami programu.
- `skills` — oficjalny katalog ElevenLabs Agent Skills z ewaluacjami trigger/functional; upstream/reference. Kluczowe są integralność instrukcji, credential handling i izolacja środowiska ewaluacyjnego.
- `engram` — MCP-native infrastruktura pamięci agenta, przechowująca pełne transkrypcje i wyszukiwanie semantyczne, z OAuth i multi-tenancy; najwyższa uwaga na prywatność, retencję, izolację tenantów i zakres dostępu do historii.
- `EchoPBX` — beta PBX na Asterisk z webowym zarządzaniem SIP; nieprodukcyjny status wymaga hardeningu, ograniczenia sieciowego, auth i kontroli uprawnień administracyjnych.
- `softphone` — eksperymentalny SpechPhone PHP/Swoole z SIP/RTP/PCM bridge, WebSocketami i bez WebRTC; kluczowe są NAT traversal, TLS, RTP exposure, SIP auth, state consistency i bezpieczne przechowywanie konfiguracji.
- `freemail` — Cloudflare Workers/D1/R2 tymczasowa poczta z wysyłką wieloma providerami, JWT i panelem użytkownika; szczególnie istotne są dane pocztowe, auth, retencja, routing, uprawnienia i domyślne credentials dokumentowane dla demo.
- `mailtm-client` — lekki klient MailTM automatyzujący tworzenie kont, JWT i odczyt skrzynki; zakres compliance/reliability, bez rozbudowy zastosowań obchodzących systemy weryfikacyjne.
- `compose-multiplatform` — upstream JetBrains Compose Multiplatform; klasyfikacja REFERENCE/UPSTREAM. Audyt służy mapowaniu kompatybilności i wykorzystania, nie sztucznemu rebrandingowi.
- `eSim` — duży upstreamowy projekt FOSSEE/IIT Bombay do EDA, symulacji SPICE, mixed-signal i PCB; klasyfikacja REFERENCE/UPSTREAM. Priorytetem są provenance, licencje, kompatybilność narzędzi i reproducibility.
- `AI_Offensive_MCP_Using_KaliLinux` — MCP bridge do Kali z arbitralnym wykonywaniem narzędzi i opcjonalnym persistent Metasploit; krytyczne są izolacja, auth, ograniczenie sieciowe i wyłącznie autoryzowane środowiska testowe. Nie rozwijać funkcji ofensywnych poza bezpieczny audyt.
- `Agent-Android` — produkcyjnie ukierunkowana podstawa Android AI agent z Expo/React Native, API, MCP, skills i pluginami; dobre zasady security-by-design: brak sekretów w repo, server-side authz, approval dla działań konsekwencyjnych. Wymaga dalszej weryfikacji implementacji względem deklaracji.
- `MaxKB` — duża platforma enterprise agent/RAG/MCP, Vue + Django + LangChain + PostgreSQL/pgvector; README zawiera domyślne dane logowania, więc wdrożenie wymaga natychmiastowego hardeningu i wymuszenia zmiany credentials.
- `llm-graph-builder` — FastAPI/React/Neo4j Knowledge Graph Builder z uploadami, wieloma LLM i trybami chat; kluczowe są SSRF, upload isolation, auth, Neo4j credentials, tenant boundaries i fakt, że README dopuszcza konfigurację pomijającą logowanie.
- `Local-Diffusion` — Flutter/Android lokalna generacja obrazów z szerokim zakresem modeli i pobieraniem z zewnętrznych źródeł; priorytet: integralność modeli, provenance, pamięć urządzenia, bezpieczeństwo pobierania oraz testy kompatybilności GPU/Android.

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
| 2026-09-12 | 20 repozytoriów | Audyt README + kwalifikacja architektoniczna | OK — bez podwójnego naliczenia |
| 2026-09-12 | 20 repozytoriów | Audyt README + kwalifikacja bezpieczeństwa/architektury | OK — bez podwójnego naliczenia |

## Reguła integralności

Ten rejestr jest źródłem stanu procesu. Każda zakończona jednostka pracy powinna otrzymać wpis z datą, repozytorium, operacją i wynikiem. Stan repozytorium nie może być oznaczony jako produkcyjny na podstawie samego przeglądu metadanych.
