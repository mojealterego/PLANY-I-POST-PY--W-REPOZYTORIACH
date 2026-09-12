# Audyt 320 — langflow

## Stan
AUDYT ZAKOŃCZONY — duża platforma AI workflow/agent, referencyjna.

## Ustalenia
README opisuje wizualny builder, Python source access, playground, multi-agent orchestration, API deployment, MCP server, observability oraz desktop dla Windows/macOS. Stos uruchamia się jako pakiet Python lub Docker; repo ma osobną politykę bezpieczeństwa i dokumentację developmentu.

## Ryzyka
Wykonywanie komponentów Python; MCP/API exposure; sekrety integracji; izolacja tenantów; bezpieczeństwo deploymentu i supply chain.

## Priorytet
KRYTYCZNY/REFERENCYJNY.

## Kolejność prac
1. Zmapować backend/frontend i mechanizm custom components.
2. Przeanalizować auth, sandboxing, MCP i API.
3. Zweryfikować testy, CI i obrazy Docker.
4. Używać jako materiału architektonicznego, nie przepisywać bez uzasadnienia.

## Kryterium zakończenia
Zweryfikowane granice wykonania kodu, auth, integracji i deploymentu.