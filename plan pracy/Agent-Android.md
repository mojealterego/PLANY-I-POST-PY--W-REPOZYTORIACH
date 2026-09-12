# Audyt 80 — Agent-Android

## Stan
AUDYT ZAKOŃCZONY — świeża foundation platformy Android AI agent.

## Ustalenia
Repo ma `apps/mobile`, `services/agent-api`, `services/mcp-server`, `plugins/agent-android`, `packages/shared` i CI. README deklaruje server-side authorization, explicit approval dla działań konsekwentnych, brak kluczy w repo i obserwowalność. Root `package.json` v0.2.0 używa workspace'ów i wymaga Node >=22.13; check wykonuje typecheck, lint, test i build.

## Ryzyka
- realne granice uprawnień MCP i API muszą być zweryfikowane kodem, nie tylko dokumentacją;
- sesje/authz i approval state;
- Android bridge/WebView/EAS supply chain;
- brak dowodu produkcyjnej gotowości samego audytu.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Auth/session → tool authorization → approval state machine → MCP isolation → shared contracts → mobile permissions → E2E/emulator → EAS/release.

## Kryterium zakończenia
Nieautoryzowana akcja jest niemożliwa w testach kontraktowych, build EAS jest reprodukowalny, a wszystkie uprzywilejowane interfejsy mają wersjonowane kontrakty.