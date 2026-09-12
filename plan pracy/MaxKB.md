# Plan pracy — MaxKB

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: platforma enterprise AI Agent/RAG/workflow
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README opisuje MaxKB jako open-source platformę do budowy agentów enterprise. Obejmuje RAG z uploadem/crawlingiem dokumentów, workflow, MCP, integracje z modelami lokalnymi i chmurowymi oraz multimodalność. Stack wskazany w README to Vue.js, Python/Django, LangChain oraz PostgreSQL/pgvector. fileciteturn817file0

## Ryzyka
1. Ingestion dokumentów i URL-i wymaga kontroli SSRF, parserów i nieufnych treści.
2. MCP/workflow może przekazywać działania do zewnętrznych narzędzi.
3. PostgreSQL/pgvector i RAG wymagają ścisłej izolacji danych użytkowników/tenantów.
4. README pokazuje domyślne dane administratora — nie mogą pozostać aktywne w wdrożeniu.
5. Integracje wielu providerów modeli zwiększają powierzchnię sekretów i kosztów.
6. GPLv3 musi zostać zachowana przy redystrybucji zmian.

## Kolejność prac
1. Auth/RBAC/tenant isolation.
2. RAG ingestion, URL validation i parser sandboxing.
3. MCP/tool policy, approval gates i limity.
4. Secrets, model provider credentials i redakcja logów.
5. Workflow quotas, timeouty, idempotency i observability.
6. Testy bezpieczeństwa oraz powtarzalny Docker/self-hosted deployment.

## Kryterium zakończenia
Zweryfikowana izolacja danych, bezpieczny RAG, kontrolowane narzędzia MCP, brak domyślnych sekretów w produkcji i przechodzące testy wdrożeniowe.
