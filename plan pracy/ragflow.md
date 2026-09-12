# AUDYT 364 — ragflow

## Status
Audyt wykonany. Duży open-source RAG engine z agentic workflow, MCP i code executor sandbox.

## Ustalenia
Docker, Python 3.13+, DeepDoc, wieloźródłowe dokumenty, reranking, cytowania, LLM/embedding providers i kanały komunikacyjne.

## Ryzyka
Code executor, dokumenty użytkowników, sekrety LLM, sieć/Docker, wielodostępność i duża powierzchnia integracji.

## Plan prac
Zmapować architekturę usług i docker-compose, auth/storage, parsery, executor, providerów i API. Zweryfikować sandbox gVisor, SSRF, upload, secret handling i tenant isolation. Lokalizacja PL po hardeningu.

## Kryterium zakończenia
Powtarzalny deployment, testy izolacji i bezpieczne wykonanie kodu oraz przetwarzanie dokumentów.
