# Plan pracy — sim

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: workspace do budowy i zarządzania agentami/workflow AI
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README opisuje self-hosted i cloud workspace z wizualnym builderem, chatem, tabelami, plikami, knowledge base, harmonogramami i integracjami. Stack obejmuje Next.js, Bun, PostgreSQL/Drizzle, Better Auth, Zod, Shadcn/Tailwind, ReactFlow, Socket.io, Trigger.dev oraz izolowane wykonanie kodu przez E2B/isolated-vm. fileciteturn826file0

## Ryzyka
1. Remote/isolated code execution jest granicą krytyczną.
2. Workspace łączy dane, pliki, sekrety, OAuth i narzędzia agentowe.
3. Harmonogramy/webhooki mogą uruchamiać działania bez interakcji użytkownika.
4. Multi-tenant isolation i RBAC wymagają weryfikacji na poziomie danych i narzędzi.
5. Instalator Docker generuje i zapisuje sekrety — wymagany audyt lifecycle.

## Kolejność prac
1. Zmapować tenant/user/workspace/resource authorization.
2. Audytować sandboxing E2B/isolated-vm i przepływ danych do narzędzi.
3. Zweryfikować OAuth, API keys, secrets i log redaction.
4. Przetestować webhook/schedule idempotency i replay protection.
5. Zweryfikować realtime, jobs i recovery po awarii.
6. Zbudować testy izolacji tenantów i permission escalation.

## Kryterium zakończenia
Brak cross-tenant access, bezpieczne wykonywanie kodu, kontrolowane sekrety, deterministyczne joby/webhooki i testy bezpieczeństwa dla każdej granicy narzędziowej.
