# Audyt 171 — opencode

## Status
AUDYT ZAKOŃCZONY — duży open-source AI coding agent z terminalowym i beta desktopowym interfejsem.

## Ustalenia
README opisuje agentów `build` i read-only `plan`, subagenta general, wiele instalatorów, desktop macOS/Windows/Linux oraz wielojęzyczną dokumentację. Repo posiada osobne pakiety console/web i branch developerski.

## Ryzyka
Pełny agent build ma szeroki dostęp do plików i poleceń, więc granice narzędzi, approvals, sandbox i trust model są kluczowe. Istotne są też auto-update/install scripts i supply chain.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Permissions → sandbox → approvals → MCP/tool boundary → update/signing → telemetry → test matrix → polonizacja.

## Kryterium zakończenia
Agent ma jawny model uprawnień, bezpieczny tryb planowania i weryfikowalne artefakty dystrybucyjne.
