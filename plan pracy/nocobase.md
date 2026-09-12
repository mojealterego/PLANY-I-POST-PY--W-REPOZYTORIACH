# NocoBase — plan

- **Audyt:** 296
- **Status:** audyt zakończony; duża platforma low-code/no-code.
- **Ustalenia:** wymagane pełne mapowanie monorepo, pluginów, backendu, auth, bazy i mechanizmu rozszerzeń.
- **Ryzyka:** multi-tenancy, plugin execution, dane biznesowe, sekrety, integracje i uprawnienia.
- **Priorytet:** KRYTYCZNY / REFERENCYJNY.
- **Kolejność:** architektura → auth/RBAC → plugin sandbox → dane → integracje → testy → deployment.
- **Kryterium:** izolacja tenantów, least privilege i testy krytycznych granic.
