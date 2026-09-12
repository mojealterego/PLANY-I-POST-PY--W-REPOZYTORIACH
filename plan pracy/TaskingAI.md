# Audyt 319 — TaskingAI

## Stan
AUDYT ZAKOŃCZONY — platforma BaaS dla agentów LLM, wysoki priorytet.

## Ustalenia
README opisuje self-hosted platformę z FastAPI, zunifikowanymi modelami, narzędziami, RAG, asystentami, historią rozmów, multi-tenancy, Docker Compose i SDK klienta. Występują integracje z OpenAI, Anthropic, Ollama, LM Studio i LocalAI. README podaje domyślne dane logowania `admin`/`TaskingAI321` dla instalacji lokalnej.

## Ryzyka
Domyślne credentials; multi-tenancy; klucze API; narzędzia zewnętrzne; RAG i dane rozmów; migracje danych; ekspozycja konsoli.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zweryfikować auth, sekret management i izolację tenantów.
2. Usunąć/zmienić domyślne credentials w deploymentach.
3. Zmapować API, tools, RAG i storage.
4. Zweryfikować Docker, migracje, testy i rate limiting.

## Kryterium zakończenia
Brak domyślnych poświadczeń produkcyjnych, zweryfikowana izolacja tenantów, kontrola sekretów i testy krytycznych endpointów.