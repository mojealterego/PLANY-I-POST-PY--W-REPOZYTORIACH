# Audyt: hackerai

## Stan
AUDYT — Next.js + Convex, WorkOS, Trigger.dev i E2B; AI-powered penetration testing assistant z agent mode i izolowanym wykonywaniem.

## Ryzyka
Projekt ma zdolność uruchamiania zadań pentestowych i korzysta z cloud sandbox. Konieczne są ścisłe scope/authorization, izolacja E2B, sekrety workerów, rate limits, audit log i blokada działań poza autoryzowanym zakresem.

## Priorytet
KRYTYCZNY — LAB/AUTHORIZED ONLY.

## Kolejność
Autoryzacja celu → sandbox/egress → tool policy → secrets → durable jobs/idempotency → audit → testy.

## Kryterium zakończenia
Każda operacja ofensywna wymaga jawnego autoryzowanego scope, jest izolowana i audytowalna; brak możliwości niekontrolowanego wykonania.
