# Audyt 167 — sugar

## Status
AUDYT ZAKOŃCZONY — lokalna warstwa pamięci i opcjonalnej autonomicznej pracy agentów.

## Ustalenia
README opisuje SQLite project/global memory, semantic search, MCP, task queue, orkiestrację research-plan-implement-review oraz opcjonalne rozwiązywanie issue GitHub i otwieranie PR.

## Ryzyka
Persistencja kontekstu, prywatność, multi-project isolation, autonomiczne wykonywanie zadań, GitHub write access i ryzyko działania bez ręcznej kontroli.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Model uprawnień → sandbox task runnera → approvals → GitHub scope → retencja/usuwanie pamięci → testy recovery.

## Kryterium zakończenia
Pamięć jest izolowana, usuwalna, audytowalna, a autonomiczne zmiany wymagają jawnego zakresu i kontroli.
