# Plan pracy — lucidrag

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Duża platforma RAG w .NET 10, deklarowana jako open-source i local-first.
- Obejmuje multimodalne pipeline'y dokumentów, obrazów, danych, wideo i audio.
- Architektura obejmuje GraphRAG, hybrydowe wyszukiwanie BM25 + semantic, agentowe rozkładanie zapytań, specjalistów domenowych i routing modeli.
- Występują wymagania PostgreSQL 16+ z pgvector, Node.js oraz opcjonalnie Ollama.
- README deklaruje multi-tenancy schema-per-tenant, RBAC, cache, circuit breaker i OpenTelemetry.
- Projekt jest aktywnie rozwijany, więc deklaracje dokumentacji wymagają potwierdzenia w kodzie.

## Ryzyka
1. Bardzo szeroki zakres funkcjonalny zwiększa sprzężenie i ryzyko regresji.
2. Multi-tenancy wymaga szczegółowego audytu izolacji danych.
3. Pipeline multimodalny wymaga kontroli kosztów CPU/GPU/RAM i odporności na uszkodzone pliki.
4. Routing modeli i fallbacki muszą mieć deterministyczne zasady oraz obserwowalność.
5. Należy zweryfikować zgodność dokumentacji z implementacją.

## Plan implementacji
1. Zmapować rozwiązanie .NET i zależności projektowe.
2. Zidentyfikować warstwy domenowe, aplikacyjne, infrastrukturalne i API.
3. Przeprowadzić audyt tenant isolation i RBAC.
4. Przeanalizować pipeline registry oraz kontrakty między pipeline'ami.
5. Zweryfikować indeksowanie, RRF, embeddingi i GraphRAG.
6. Zweryfikować odporność backendów LLM, retry/circuit breaker i cache.
7. Dodać/uzupełnić testy integracyjne dla każdego pipeline'u.
8. Wykonać testy obciążeniowe dla wyszukiwania i przetwarzania multimediów.
9. Uporządkować konfigurację wdrożeniową i obserwowalność.
10. Przygotować pełną polską dokumentację użytkownika i administratora.

## Kryterium zakończenia
Powtarzalny build .NET 10, testy jednostkowe/integracyjne przechodzące, zweryfikowana izolacja tenantów, mierzalna wydajność oraz zgodność README z rzeczywistą implementacją.