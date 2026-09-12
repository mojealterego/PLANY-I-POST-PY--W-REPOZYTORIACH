# ARCH-ENG-CORE-999 — Ranking priorytetów 414 repozytoriów

**Data:** 2026-09-12  
**Etap:** 2 — ranking priorytetów  
**Portfel:** 414/414 repozytoriów po rekonsyliacji  
**Audyty:** 414/414 — 100%  
**Zasada:** ranking strategiczny nie oznacza gotowości produkcyjnej.

## 1. Cel

Ustalić kolejność inwestowania czasu i prac inżynieryjnych po zakończeniu audytu. Ranking łączy potencjał biznesowy, możliwość ponownego wykorzystania aktywów, gotowość techniczną, ryzyko oraz szybkość wejścia na rynek.

## 2. Metryka

| Kryterium | Waga |
|---|---:|
| realny problem biznesowy | 20% |
| gotowość istniejącego kodu | 15% |
| potencjał MRR / ARPU | 20% |
| B2B | 15% |
| przewaga technologiczna / aktywa | 10% |
| skalowalność | 10% |
| bezpieczeństwo / wykonalność regulacyjna | 5% |
| time-to-market | 5% |
| **Razem** | **100%** |

Dodatkowy filtr: projekty z krytycznym ryzykiem bezpieczeństwa nie mogą wejść do wdrożenia bez hardeningu, niezależnie od wyniku biznesowego.

## 3. Poziomy priorytetu

### P0 — strategiczny rdzeń produktu

Projekty, które powinny stać się pierwszymi kandydatami do konsolidacji, refaktoryzacji i productizacji.

1. **B2B AI Agent / AI Employee** — najwyższy priorytet. Połączyć agentów, pamięć, RAG, workflow, MCP, integracje biznesowe i approval/audit w jeden kontrolowany produkt.
2. **Agent automatyzacji procesów przedsiębiorstwa** — wykorzystać workflow/low-code oraz agentowe aktywa; docelowo automatyzacja procesów z kontrolowanym wykonaniem.
3. **Agent programistyczny z izolowanym execution sandbox** — wysoki ARPU/B2B i silna synergia z MCP, coding-agentami oraz infrastrukturą wykonawczą.
4. **Agent mobilny Android** — produkt konsumencki/B2B z dużą przewagą wynikającą z istniejących fundamentów `Agent-Android`, `mobile-ai-agents` i podobnych projektów; wymagany bardzo silny model zgód i uprawnień.
5. **Agent dokumentów + RAG / Knowledge Agent** — produkt B2B o czytelnym ROI; wykorzystać RAG, GraphRAG, pamięć i wyszukiwanie.
6. **AI Customer Support / Voice Agent** — wysoki potencjał komercyjny; wymaga kontroli kosztów, jakości, nagrań, prywatności i działań konsekwencyjnych.
7. **AI Sales / CRM Agent** — automatyzacja kwalifikacji leadów, researchu, follow-upów i aktualizacji CRM przy zachowaniu kontroli człowieka nad komunikacją i decyzjami.

### P1 — bardzo wysoki priorytet

8. **Private / Offline AI Assistant** — połączenie lokalnego AI, secure storage, RAG i bezpiecznego tool calling; mocny wyróżnik prywatności.
9. **Agent Research / Knowledge Management** — wyszukiwanie, synteza, pamięć, źródła i dowody; naturalne wykorzystanie centralnej bazy wiedzy.
10. **Platforma budowy agentów i workflowów** — wykorzystać wiedzę z `sim`, `ToolJet`, `n8n`, `langflow`, `LangGraph` i podobnych projektów, ale nie kopiować bez zachowania licencji/provenance.
11. **AI Developer Tools** — zestaw narzędzi dla developerów: coding, code review, testy, dokumentacja, repozytoria i bezpieczne wykonywanie zadań.
12. **Platforma AI dla twórców — obraz/wideo/audio** — połączenie istniejących aktywów generatywnych; najpierw licencje modeli, provenance, koszty GPU i jakość.

### P2 — średni/wysoki priorytet

13. **Telecom / PBX / Voice automation** — duży potencjał B2B, lecz wysoki koszt bezpieczeństwa, compliance i infrastruktury.
14. **Mobile productivity agents** — wyspecjalizowane agenty Android/iOS dla produktywności.
15. **Lokalne generowanie obrazu/wideo** — produkt prywatności/offline, zależny od sprzętu i dystrybucji modeli.
16. **AI app/workflow builder** — wertykalne narzędzie do budowania aplikacji z agentami, z bezpiecznym sandboxem.
17. **Gry z AI** — selekcja wyłącznie działających/prototypowych produktów z wyraźnym gameplayem; nie inwestować w puste szkielety.

### P3 — strategiczne aktywa / referencje

Duże projekty upstream/reference, np. `n8n`, `langflow`, `appsmith`, `ToolJet`, `webstudio`, `ollama`, `renpy`, `termux-app`, `react-native-windows`, `compose-multiplatform`, `tauri`, `GDevelop`, `HHVM`, `Flowise`.

Nie rebrandować ani nie przepisywać mechanicznie. Traktować jako źródło wiedzy, kompatybilności, benchmarków i komponentów możliwych do legalnej integracji.

### P4 — research / laboratoryjne

Cybersecurity/offensive tooling, spyware/dekompilaty, eksperymenty badawcze i projekty wymagające szczególnej kontroli. Zachować jako research/lab, chyba że zostanie zdefiniowany bezpieczny produkt defensywny.

### P5 — archiwum / minimal / niska wartość

Repozytoria puste, bootstrapowe, demonstracyjne bez przewagi lub projekty o niejasnym zastosowaniu. Nie inwestować przed uzasadnieniem produktu.

## 4. Ranking aktywów bazowych do konsolidacji

| Pozycja | Aktyw | Rola |
|---:|---|---|
| 1 | `Agent-Android` | fundament mobilnego agenta |
| 2 | `mobile-ai-agents` | katalog agentów/umiejętności/workflowów mobilnych |
| 3 | `AgentGPT` | fundament autonomicznego planowania/wykonywania |
| 4 | `Hermes Agent` | agent z pamięcią, skillami, cron i izolacją |
| 5 | `engram` | pamięć agentowa / multi-tenant |
| 6 | `agent-command-center-sdk` | gateway, tool calling, guardrails |
| 7 | `futureagi-sdk` / `future-agi` | ewaluacja, guardrails, obserwowalność |
| 8 | `sim` | agent/workflow build + deploy |
| 9 | `ToolJet` | workflow/low-code/integracje |
| 10 | `n8n` | automatyzacja workflow |
| 11 | `LangGraph` / `langflow` / `crewAI` | orkiestracja agentów |
| 12 | `MaxKB` / `FastGPT` / `RAGFlow` | RAG/knowledge layer |
| 13 | `OGAM` / `Local-Diffusion` / `pocketpal-ai` / `LocalAI` / `Ollama` | lokalne AI |
| 14 | `WAO-AI` / `WAO-AI-2` | warstwa specyfikacji i orkiestracji |
| 15 | `Rap-Agent` | kreatywny agent |

## 5. Pierwsza kolejka do realnej productizacji

### Kolejka A — budowa wspólnego rdzenia

1. Identity + RBAC + tenancy.
2. Secrets/configuration.
3. Agent runtime.
4. Tool registry + MCP contracts.
5. Approval/audit engine.
6. Memory/RAG layer.
7. Workflow/orchestration.
8. Sandbox/execution isolation.
9. Observability/evaluation.
10. Billing/quotas/usage metering.

### Kolejka B — pierwszy produkt

**B2B AI Employee / Enterprise Agent Platform** jako produkt nadrzędny. Pierwsza wersja powinna koncentrować się na kilku procesach o mierzalnym ROI zamiast na ogólnym agencie robiącym wszystko.

### Kolejka C — produkty pochodne

1. Coding Agent.
2. Knowledge/Document Agent.
3. Sales/CRM Agent.
4. Customer Support/Voice Agent.
5. Android Mobile Agent.
6. Private/Offline Assistant.
7. Creator AI Studio.

## 6. Bramki przed rozpoczęciem wdrożenia

- brak sekretów w kodzie,
- deny-by-default dla narzędzi i wykonania,
- sandbox dla kodu/komend,
- approval dla działań konsekwencyjnych,
- izolacja tenantów,
- testy bezpieczeństwa,
- testy integracyjne i kontraktowe,
- obserwowalność,
- backup/recovery/migracje,
- SBOM/provenance zależności i modeli,
- weryfikacja licencji wszystkich użytych upstreamów i modeli,
- potwierdzenie kosztu jednostkowego i marży.

## 7. Decyzja strategiczna

**Priorytet główny:** zbudować jeden bezpieczny, modułowy rdzeń B2B AI Agent / AI Employee, a następnie wykorzystać go do szybkiego tworzenia wyspecjalizowanych agentów.

Nie budować 20 niezależnych produktów równolegle. Najpierw wspólna infrastruktura i jeden produkt referencyjny, następnie odgałęzienia produktowe.

**Status etapu 2:** ranking strategiczny utworzony.  
**Następny etap:** wybór konkretnego produktu P0 i rozpoczęcie refaktoryzacji zgodnie z planami repozytoriów.
