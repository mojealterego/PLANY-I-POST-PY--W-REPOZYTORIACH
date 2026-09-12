# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **299**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — **299 repozytoriów** |
| Audyt szczegółowy | W TOKU — **96/299** |
| Plany pracy | UTWORZONE — **96/299** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 77 | builder-www | Frappe Builder; low-code builder z AI, CMS, skryptami, publikacją i analityką; workspace frontend/Frappe UI | WYSOKI | `plan pracy/builder-www.md` |
| 78 | futureagi-sdk | SDK ewaluacji/observability/guardrails/RAG dla Python + TypeScript; kluczowe dane ewaluacyjne i sekrety API | WYSOKI | `plan pracy/futureagi-sdk.md` |
| 79 | MATS-Grants | Reproducowalny syntetyczny harness badawczy z CI, testami i safety boundary; brak roszczeń o realne scheming | WYSOKI | `plan pracy/MATS-Grants.md` |
| 80 | Agent-Android | Foundation Android AI agent z Expo/RN, API, MCP, skills i approval gates; Node >=22.13 | KRYTYCZNY | `plan pracy/Agent-Android.md` |
| 81 | skills | Biblioteka ElevenLabs Agent Skills z trigger/functional evals i izolowanymi workspace'ami testowymi | WYSOKI | `plan pracy/skills.md` |
| 82 | engram | MCP-native pamięć agentów; verbatim transcripts, semantic search, multi-tenancy, Cloudflare Workers/D1/Vectorize | KRYTYCZNY | `plan pracy/engram.md` |
| 83 | git-lfs | Duży upstreamowy projekt Git LFS w Go z CI, podpisywanymi release'ami i rozbudowaną specyfikacją | ŚREDNI | `plan pracy/git-lfs.md` |
| 84 | softphone | Eksperymentalny SIP/RTP softphone PHP/Swoole z bridge RTP↔PCM i aktywną gałęzią inbound | KRYTYCZNY | `plan pracy/softphone.md` |
| 85 | SMS-MAN-vs-OnlineSIM-2026-disposable-numbers-from-0.01-service-compariso | Mikro-repo porównawcze usług numerów tymczasowych; brak podstaw do klasyfikacji jako aplikacja | NISKI | `plan pracy/SMS-MAN-vs-OnlineSIM-2026-disposable-numbers-from-0.01-service-compariso.md` |
| 86 | FastRecvSMS | CLI/MCP do usług SMS verification; multi-provider, zakup numerów i operacje na zamówieniach | KRYTYCZNY | `plan pracy/FastRecvSMS.md` |
| 87 | astro | hermitAI: Astro + Gemini/Vertex + Bright Data + MongoDB RAG + JWT/credits + wiele narzędzi web | KRYTYCZNY | `plan pracy/astro.md` |
| 88 | layla-sdk | TypeScript SDK dla mini-aplikacji Layla; WebView bridge, SQLite/files, multimodal, audio i generowanie treści | WYSOKI | `plan pracy/layla-sdk.md` |
| 89 | pentagram | Niezależny memory substrate w TypeScript/S-expression z evaluator sandbox, MCP, HNSW, provenance i tenant isolation | KRYTYCZNY | `plan pracy/pentagram.md` |
| 90 | agenticSeek | Lokalny/autonomiczny agent z browsingiem, wykonywaniem kodu, Docker/SearXNG/Redis i wieloma providerami LLM | KRYTYCZNY | `plan pracy/agenticSeek.md` |
| 91 | cli | ElevenLabs CLI/Agents as Code; Rust, OpenAPI-generated SDK, push/pull agentów, tools/tests i data residency | WYSOKI | `plan pracy/cli.md` |
| 92 | elevenlabs-mcp | Historyczny lokalny MCP ElevenLabs, jednoznacznie deprecated na rzecz hosted MCP; repo nie jest aktywnie utrzymywane | NISKI | `plan pracy/elevenlabs-mcp.md` |
| 93 | freemail | Cloudflare Workers/D1/R2 temporary-mail service z REST API, forwardingiem, auth i wieloma providerami wysyłki | KRYTYCZNY | `plan pracy/freemail.md` |
| 94 | 26CP3600177-ai-email-generator | Bardzo mały projekt akademicki z README o charakterze szablonowym i licznymi niezweryfikowanymi alternatywami stacku | NISKI | `plan pracy/26CP3600177-ai-email-generator.md` |
| 95 | mailtm-client | Lekki Python wrapper MailTM do tworzenia skrzynek, JWT i odczytu inboxu; README zawiera placeholder repo URL | ŚREDNI | `plan pracy/mailtm-client.md` |
| 96 | krypton-byte | Repozytorium profilowe agregujące projekty autora; m.in. neonize/tryx/thundra i narzędzia komunikatorowe | NISKI/ŚREDNI | `plan pracy/krypton-byte.md` |

## Poprzednie audyty

Audyty 1–76 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 77–96 są opisane powyżej.

## Postęp

**96 / 299 repozytoriów — 32,11% audytu szczegółowego.**  
**203 repozytoria pozostają do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **299 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
