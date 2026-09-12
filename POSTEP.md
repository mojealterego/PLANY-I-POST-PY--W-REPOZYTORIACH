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

Zweryfikowano rzeczywistą zawartość README i dostępne informacje projektowe dla: `Problemy-milenijne`, `aider`, `free-claude-code`, `MCP-Server-Eleven-Labs`, `Longview-Philanthropy-Grant`, `packages`, `elevenlabs-swift-sdk`, `cli`, `elevenlabs-js`, `elevenlabs-python`, `elevenlabs-android`, `plugin`, `examples`, `homebrew-tap`, `scoop-bucket`, `ui`, `elevenlabs-mcp-player`, `elevenlabs-n8n`, `unity`, `Alibaba-Grants`.

### Najważniejsze ustalenia

- `Problemy-milenijne` — prywatny projekt badawczy formalizujący TRS i odnoszący się do P≠NP, RH, Hodge i BSD; README utrzymuje status hipotez jako OPEN i wymaga niezależnej falsyfikacji. Priorytet: rygor formalny, śledzenie dowodów i oddzielenie hipotez od twierdzeń.
- `aider` — duży upstreamowy agent pair-programming w terminalu z obsługą wielu LLM, mapowaniem codebase, Git, testów i voice-to-code; traktować jako referencję technologiczną, nie jako własny produkt do ślepego rebrandingu. Kluczowe są granice wykonywania zmian, sekrety i kontrola skutków poleceń.
- `free-claude-code` — rozbudowany lokalny proxy/router dla wielu providerów i agentów kodujących, z fallbackiem modeli, UI administracyjnym, lokalną historią i integracjami desktop/IDE/telefon; bardzo wysoki priorytet dla credentiali, powierzchni proxy, instalatorów zdalnych, izolacji narzędzi i kontroli kosztów.
- `MCP-Server-Eleven-Labs` — produkcyjnie ukierunkowany serwer MCP dla głosu, z osobnym tokenem MCP, rate limitingiem, limitami wejścia/audio, correlation IDs, Docker/Render i JSON state; migracja MCP SDK v2 jest świadomie odłożona do wspólnej migracji kodu i testów. Przed publicznym wdrożeniem potrzebny trwały storage i pełna weryfikacja protokołu.
- `Longview-Philanthropy-Grant` — dossier badawcze AI integrity/secret loyalties oraz digital minds; README rozdziela fakty, hipotezy i status aplikacji. Kluczowe są provenance, reproducibility, responsible disclosure i brak nieudokumentowanych twierdzeń o kwalifikacjach lub wynikach.
- `packages` — upstreamowy monorepo ElevenAgents SDK dla JS/TS/React/React Native/widgetów; obejmuje WebRTC, client tools i audio. Traktować jako kod referencyjny/upstream; priorytetem są zgodność API, bezpieczeństwo client tools i aktualność zależności.
- `elevenlabs-swift-sdk` — SDK Swift dla iOS/macOS/visionOS/tvOS oparte na LiveKit WebRTC, z Client Tools i MCP; README ostrzega przed umieszczaniem API key w aplikacji. Kluczowe: concurrency, tokeny tymczasowe, uprawnienia audio/sieciowe i sandbox client tools.
- `cli` — oficjalny CLI ElevenLabs z pełnym API, Agents as Code, lokalnymi konfiguracjami JSON, synchronizacją push/pull, testami oraz data residency; szczególnie istotne są operacje mutujące, dry-run, TLS overrides i rozdzielenie testów E2E od zwykłego API key.
- `elevenlabs-js` — oficjalny Node SDK generowany programatycznie, z TTS, streamingiem, Speech Engine, retry/timeout i WebSocket auth; wyraźna powierzchnia bezpieczeństwa to Speech Engine, gdzie wyłączenie auth wymaga zewnętrznego ograniczenia sieciowego.
- `elevenlabs-python` — oficjalny Python SDK generowany programatycznie, obejmujący TTS, voice cloning, ElevenAgents, ClientTools i Speech Engine; wymaga rygorystycznego auth i kontroli narzędzi po stronie serwera.
- `elevenlabs-android` — oficjalny Android SDK Kotlin z LiveKit/WebRTC, text-only WebSocket, tokenami prywatnych agentów i client tools; nie należy umieszczać API keys w aplikacji. Kluczowe: runtime permissions, lifecycle, audio thread, transport security i ograniczenie lokalnych narzędzi agenta.
- `plugin` — plugin ElevenLabs dla Cursor/Claude Code/Codex z drzewem skills i hostowanym MCP OAuth; upstream/reference. Kluczowe są scope OAuth, uprawnienia narzędzi i rozdzielenie skills od mutujących operacji MCP.
- `examples` — repozytorium przykładów ElevenLabs generowanych z promptów, obejmujące TTS/STT/music/sound effects/agents, z template'ami i automatycznym generowaniem. Krytyczne: provenance generowanego kodu, reprodukowalność oraz kontrola prompt-runnera.
- `homebrew-tap` — automatycznie generowany tap Homebrew dla CLI; repozytorium dystrybucyjne, nie projekt do ręcznej refaktoryzacji. Należy kontrolować provenance artefaktów i integralność release pipeline.
- `scoop-bucket` — automatycznie generowany bucket Scoop dla CLI; traktować jako artefakt dystrybucyjny i kontrolować podpis/provenance manifestów.
- `ui` — upstreamowa biblioteka komponentów ElevenLabs UI oparta na shadcn/ui, instalowana przez CLI/registry; kluczowe są bezpieczeństwo zdalnego registry, integralność komponentów i kompatybilność Tailwind/shadcn.
- `elevenlabs-mcp-player` — repozytorium MCPB dla Claude Desktop z TTS/audio/music/local playback, jawnie zdeprecjonowane na rzecz hostowanego MCP i nieutrzymywane. Klasyfikacja: ARCHIVAL/REFERENCE; local audio path access wymagałby sandboxu, gdyby projekt był reaktywowany.
- `elevenlabs-n8n` — oficjalny node n8n dla ElevenLabs z operacjami Speech/Voice; README ma niedokończoną sekcję Usage. Priorytet: credential handling, compatibility matrix, test coverage i dokumentacja operacji mutujących.
- `unity` — wczesny ElevenAgents Unity SDK dla Unity 6.3 LTS, z platformami standalone/mobile/Editor/WebGL, WebRTC i lifecycle sesji; status early-stage. Kluczowe: cross-platform audio, WebGL ograniczenia, lifecycle, client tools i test matrix.
- `Alibaba-Grants` — pakiet aplikacyjno-architektoniczny OMEGA-X dla Alibaba Cloud AI Catalyst, jawnie rozdzielający capability demonstrated/proposed i wymagający źródeł dla twierdzeń o programie. Kluczowe: evidence discipline, aktualność warunków programu, security/compliance oraz brak gwarantowania benefitów bez oficjalnego potwierdzenia.

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

## Reguła integralności

Ten rejestr jest źródłem stanu procesu. Każda zakończona jednostka pracy powinna otrzymać wpis z datą, repozytorium, operacją i wynikiem. Stan repozytorium nie może być oznaczony jako produkcyjny na podstawie samego przeglądu metadanych.
