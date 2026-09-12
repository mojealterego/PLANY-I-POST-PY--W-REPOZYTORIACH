# Plan pracy — llm-graph-builder

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: aplikacja RAG / Knowledge Graph z Neo4j
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIE POTWIERDZONO

## Ustalenia
Projekt łączy backend FastAPI/Python z frontendem React i Neo4j. Obsługuje dokumenty, YouTube, web, S3/GCS, wiele dostawców LLM, embeddingi, tryby wyszukiwania oraz śledzenie użycia. README wymaga Neo4j >=5.23 i APOC. Backend requirements są mocno rozbudowane i ściśle przypięte, obejmując m.in. PyTorch CPU, LangChain, wiele integracji LLM, Neo4j, unstructured, FastAPI i narzędzia RAG. README zawiera jednocześnie konfiguracje historyczne i aktualizowane przykłady modeli, dlatego kontrakt runtime trzeba zweryfikować względem kodu.

## Ryzyka
1. Bardzo szeroki stos zależności zwiększa powierzchnię utrzymania i konfliktów wersji.
2. Dokumentacja pokazuje możliwość pominięcia logowania oraz przykładowe domyślne dane Neo4j — wymaga to bezwzględnego fail-closed w produkcji.
3. Upload dokumentów, web/YouTube oraz zewnętrzne źródła wymagają limitów, walidacji, SSRF protection i kontroli zasobów.
4. Wielu providerów LLM wymaga jednolitego kontraktu błędów, timeoutów i secret management.
5. Należy zweryfikować izolację tenantów/użytkowników i zakres dostępu do grafów.

## Kolejność prac
1. Zmapować backend, frontend, Neo4j, pipeline ekstrakcji i chat.
2. Zweryfikować auth/authz oraz izolację danych.
3. Zabezpieczyć upload, URL fetch, GCS/S3/YouTube i limity tokenów.
4. Zbudować testy parserów, ekstrakcji grafu, embeddingów i zapytań.
5. Zbudować testy kontraktowe providerów LLM i Neo4j.
6. Uporządkować dependency/runtime matrix i CI.
7. Następnie polonizacja, rebranding i integracja z własną warstwą wiedzy.

## Kryterium zakończenia
Powtarzalny build backendu/frontendu, testy izolacji danych i pipeline'u RAG/graph, bezpieczna konfiguracja oraz zweryfikowane kontrakty Neo4j/LLM.
