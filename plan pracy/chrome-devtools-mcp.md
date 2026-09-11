# Plan pracy — chrome-devtools-mcp

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- MCP server dla agentów umożliwiający sterowanie i inspekcję Chrome DevTools.
- Funkcje obejmują debugging, tracing, sieć, screenshoty, konsolę i automatyzację Puppeteer.
- Dostęp do zawartości przeglądarki jest uprzywilejowany i może obejmować dane wrażliwe.
- Statystyki użycia są domyślnie włączone, z możliwością opt-out.
- Narzędzie wykonuje sprawdzanie aktualizacji npm, a część funkcji może wysyłać trace URL do CrUX.

## Ryzyka
1. MCP ma bardzo szerokie uprawnienia nad sesją Chrome.
2. Dane stron, cookies, formularze i nagłówki mogą być ujawnione klientowi MCP.
3. Domyślna telemetria wymaga jasnej polskiej dokumentacji i konfiguracji prywatności.
4. Aktualizacje `@latest` zwiększają ryzyko niekontrolowanej zmiany wersji.

## Plan implementacji
1. Zmapować serwer MCP, CLI i warstwę Puppeteer.
2. Zdefiniować model uprawnień narzędzi i granice klienta.
3. Dodać bezpieczne domyślne ustawienia prywatności.
4. Udokumentować wszystkie kanały telemetryczne i sieciowe.
5. Dodać testy narzędzi MCP, sesji Chrome i błędów transportu.
6. Zweryfikować wersjonowanie zależności i release process.
7. Dodać testy regresji dla narzędzi DevTools.
8. Wykonać polonizację dokumentacji bez tłumaczenia nazw API/komend.

## Kryterium zakończenia
Zweryfikowany model uprawnień, testy MCP, jednoznaczne ustawienia prywatności, stabilne wersjonowanie i kompletna polska dokumentacja.