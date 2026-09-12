# Audyt 336 — actions

## Stan
AUDYT ZAKOŃCZONY — repozytorium GitHub Actions dla zarządzania repozytoriami MCP.

## Ustalenia
README wymienia akcje Cloudflare Pages preview/cleanup, Hugo build oraz slash commands. Szczególnie uprzywilejowana jest obsługa `/lgtm`, która może labelować, zatwierdzać i auto-merge'ować PR-y dla core maintainers; approval jest unieważniane przy pushu.

## Ryzyka
Automatyczny merge; uprawnienia GitHub tokenów; deploy/cleanup Cloudflare; zaufanie do maintainers; obsługa komend PR.

## Priorytet
KRYTYCZNY DLA CI/CD.

## Kolejność prac
1. Zweryfikować permissions każdego workflow.
2. Przetestować `/lgtm`, `/hold`, `/stageblog` i invalidację approval.
3. Ograniczyć token scope i chronić gałęzie.
4. Zweryfikować deploy/cleanup idempotency.

## Kryterium zakończenia
Brak możliwości nieautoryzowanego merge/deploy, minimalne permissions i testy workflow.