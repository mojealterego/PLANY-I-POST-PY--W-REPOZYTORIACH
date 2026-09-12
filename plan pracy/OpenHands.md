# Audyt 240 — OpenHands

## Status
AUDYT ZAKOŃCZONY — Agent Canvas/self-hosted control center dla agentów programistycznych.

## Stan faktyczny
README opisuje Node.js frontend, Agent Server, automatyzacje, wiele backendów, ACP oraz integracje z GitHub/Slack/Linear. Możliwy jest tryb bez sandboxa z pełnym dostępem agenta do systemu oraz tryb Docker sandbox.

## Ryzyka
Krytyczna granica filesystem/shell, wieloagentowe backendy, webhooki i integracje zewnętrzne, automatyzacje harmonogramowane oraz sekrety.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Sandbox i workspace isolation.
2. Permissions/approval model.
3. MCP/ACP/tool boundary.
4. Integracje i webhook auth.
5. Testy bezpieczeństwa i recovery.
6. Polonizacja interfejsu zależnego.

## Kryterium zakończenia
Każda operacja agenta ma jawny zakres, sandbox lub równoważną izolację oraz weryfikowalne logi i testy.
