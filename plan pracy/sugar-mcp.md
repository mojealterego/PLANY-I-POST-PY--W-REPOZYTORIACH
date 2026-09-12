# Audyt: sugar-mcp

## Stan
AUDYT — MCP integration layer powiązana z pamięcią Sugar.

## Ryzyka
Granica MCP ↔ lokalna pamięć i agent jest krytyczna: walidacja wejścia, ścieżki plików, zakres pamięci, prompt injection i uprawnienia zapisu.

## Priorytet
KRYTYCZNY.

## Kolejność
MCP contract → storage boundaries → authorization → injection resistance → tests → docs.

## Kryterium zakończenia
Każde narzędzie ma minimalne uprawnienia, walidację i testy negatywne.
