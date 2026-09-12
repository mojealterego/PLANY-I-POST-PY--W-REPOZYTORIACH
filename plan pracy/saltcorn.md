# Plan pracy — saltcorn

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: extensible open-source no-code database application builder
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Saltcorn jest rozszerzalnym no-code builderem aplikacji web/mobile opartych o bazę danych. README opisuje self-hosting, tryb wielodzierżawny, PostgreSQL, Node.js, Express, pluginy, CLI, Socket.io, testy Jest oraz instalację przez npm/npx/Docker. fileciteturn848file0

## Ryzyka
1. Multi-tenant hosting wymaga twardej izolacji danych i zasobów.
2. System wspiera live plugins, co tworzy krytyczną granicę wykonywania obcego kodu.
3. Konfiguracja PostgreSQL i session secrets wymaga bezpiecznego secret management.
4. Instalatory `npx`/skrypty systemowe mają szeroki wpływ na hosta.
5. Dynamiczne aplikacje, API i Socket.io wymagają auth, CSRF/CORS i rate limiting.

## Kolejność prac
1. Audyt tenant isolation i authorization.
2. Sandbox/provenance dla pluginów i dynamicznego kodu.
3. Secrets, session lifecycle i bezpieczna konfiguracja DB/SSL.
4. API/Socket.io security oraz limity zasobów.
5. Testy security regression i multi-tenant.
6. Reproducible build/deployment i dopiero potem polonizacja własnych warstw.

## Kryterium zakończenia
Brak cross-tenant access, kontrolowane plugin execution, bezpieczne sekrety/sesje, testy API i powtarzalny deployment bez niekontrolowanych uprawnień hosta.
