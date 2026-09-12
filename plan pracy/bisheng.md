# Audyt: bisheng

## Stan
AUDYT — duża platforma LLM/RAG/agent/workflow; wymaga pełnej mapy usług i integracji.

## Ryzyka
Providerzy modeli, dokumenty, vector/RAG, pluginy, wielodostępność i wykonywanie narzędzi tworzą dużą powierzchnię bezpieczeństwa.

## Priorytet
KRYTYCZNY.

## Kolejność
Auth/tenancy → secrets → RAG/data isolation → tool execution → network egress → tests → deployment.

## Kryterium zakończenia
Zweryfikowana izolacja tenantów, narzędzi i danych oraz reprodukowalny deployment.
