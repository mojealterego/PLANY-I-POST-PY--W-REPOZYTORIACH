# Plan pracy — FastGPT

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: platforma AI Agent/RAG/workflow
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
FastGPT deklaruje wizualną orkiestrację Agent Skill, workflow, MCP, RAG, pluginy, pełne logi wywołań, ewaluację i API. README opisuje wdrożenie Docker oraz obsługę wielu modeli i formatów dokumentów. Projekt ma własną licencję open-source z dodatkowymi warunkami komercyjnymi. fileciteturn827file0

## Ryzyka
1. Agent/workflow może wykonywać działania zewnętrzne przez pluginy i MCP.
2. RAG przyjmuje dokumenty i URL-e, więc potrzebne są kontrole upload/SSRF/provenance.
3. Publiczne/udostępniane aplikacje wymagają ścisłego auth i tenant isolation.
4. Integracja wielu providerów zwiększa ryzyko wycieku kluczy i niejednolitych limitów.
5. Domyślne dane logowania z README nie mogą być używane w środowisku produkcyjnym.
6. Licencja wymaga osobnego audytu przed rebrandingiem/dystrybucją.

## Kolejność prac
1. Auth/RBAC/tenant isolation.
2. MCP/plugin execution policy i approval gates.
3. RAG upload/URL ingestion oraz SSRF i malware controls.
4. Secrets/provider credentials i redakcja logów.
5. Workflow idempotency, quotas, timeouty i observability.
6. Reprodukowalny Docker/CI build i testy bezpieczeństwa.

## Kryterium zakończenia
Wszystkie działania agentowe są autoryzowane, RAG jest bezpieczny, dane tenantów są izolowane, sekrety nie trafiają do logów, a licencja i provenance są rozliczone.
