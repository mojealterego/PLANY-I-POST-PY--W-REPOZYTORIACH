# Audyt 331 — google-analytics-mcp

## Stan
AUDYT ZAKOŃCZONY — eksperymentalny MCP server dla Google Analytics.

## Ustalenia
README opisuje lokalny serwer MCP używający Google Analytics Admin/Data API, z narzędziami do kont, właściwości, raportów, lejków i realtime. Uwierzytelnianie opiera się na Google ADC/OAuth, a zalecany scope Analytics jest read-only.

## Ryzyka
Credential handling; ekspozycja danych analitycznych przez MCP; prompt injection; zbyt szeroki zakres projektu Google Cloud; błędy mapowania właściwości.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zweryfikować OAuth/ADC i minimalne scopes.
2. Zmapować każdy MCP tool i walidację parametrów.
3. Dodać testy autoryzacji i błędnych identyfikatorów.
4. Ograniczyć logowanie danych analitycznych.

## Kryterium zakończenia
Read-only access by default, minimalne uprawnienia i testy granic MCP.