# Plan pracy — dify

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: platforma do budowy aplikacji LLM/Agent/RAG/LLMOps
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Dify łączy wizualne workflow, obsługę setek modeli/providerów, Prompt IDE, RAG, agentów, LLMOps i API. README dokumentuje self-hosting przez Docker Compose, wielojęzyczność oraz osobny mechanizm raportowania podatności bezpieczeństwa. Repo ma własną licencję opartą na Apache 2.0 z dodatkowymi warunkami. fileciteturn837file0

## Ryzyka
1. Wielu providerów modeli i narzędzi zwiększa powierzchnię sekretów i integracji.
2. RAG ingestuje dokumenty; konieczne są kontrole plików, URL-i i danych nieufnych.
3. Agent tools i workflow mogą wykonywać działania zewnętrzne.
4. Self-hosting wymaga poprawnej konfiguracji auth, sieci, storage i sekretów.
5. Licencja i warunki dodatkowe muszą zostać zachowane przy wykorzystaniu kodu.

## Kolejność prac
1. Mapa usług, tenantów i granic autoryzacji.
2. Audyt narzędzi agentowych, pluginów i workflow.
3. RAG security: upload, URL, parsery, izolacja danych.
4. Secrets management i redakcja logów/telemetrii.
5. Testy multi-tenant, API i webhooków.
6. Reprodukowalny self-hosted build oraz zgodność licencyjna.

## Kryterium zakończenia
Zweryfikowana izolacja danych, kontrolowane wykonywanie narzędzi, bezpieczny RAG, kompletne zarządzanie sekretami i przechodzące testy self-hosted.
