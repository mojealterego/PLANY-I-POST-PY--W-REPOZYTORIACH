# Plan pracy — builder

## Status
AUDYT ZAKOŃCZONY — duży builder aplikacyjny, monorepo.

## Stan faktyczny
Repozytorium zawiera `.changeset`, `.github`, Yarn, Nx, `.nvmrc`, README, SECURITY, `examples/` oraz rozbudowaną strukturę pakietów. Jest to aktywny projekt wymagający analizy modułów zamiast traktowania go jak prosty starter.

## Ryzyka
złożoność monorepo; rozszerzenia i pluginy; generowany kod; build/deploy; zależności npm; konfiguracja EAS; granice bezpieczeństwa między projektami.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapa pakietów i zależności.
2. Pipeline build/test/CI i wersjonowanie Changesets.
3. Analiza pluginów, generatorów i wykonywania kodu.
4. Izolacja projektów i sekretów.
5. Polonizacja warstwy użytkowej i dokumentacji.

## Kryterium zakończenia
Powtarzalny build monorepo, testy modułów krytycznych, zamknięte granice pluginów i kompletna dokumentacja PL.