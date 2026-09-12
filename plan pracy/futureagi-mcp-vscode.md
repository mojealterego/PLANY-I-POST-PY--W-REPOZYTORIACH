# futureagi-mcp-vscode — plan pracy

## Status
AUDYT ZAKOŃCZONY — mały adapter MCP/VS Code.

## Stan faktyczny
Repozytorium ma niewielki rozmiar i jest przeznaczone do integracji Future AGI z VS Code przez MCP. Zakres implementacyjny wymaga utrzymania zgodności z aktualnym protokołem MCP i konfiguracją klienta.

## Ryzyka
- mały rozmiar zwiększa ryzyko brakującej walidacji;
- konfiguracja MCP może nadawać niezamierzone uprawnienia;
- zależność od zmian VS Code/MCP/Future AGI.

## Priorytet
ŚREDNI

## Kolejność prac
1. Zweryfikować manifest, entrypoint i konfigurację MCP.
2. Sprawdzić zakres narzędzi i uprawnień.
3. Dodać smoke test klienta/serwera.
4. Uporządkować dokumentację i polonizację.

## Kryterium zakończenia
Działająca integracja MCP z ograniczonym zakresem uprawnień i testem start/stop.
