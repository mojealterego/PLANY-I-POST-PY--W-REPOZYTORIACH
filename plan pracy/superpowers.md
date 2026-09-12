# Audyt: superpowers

## Status
AUDYT ZAKOŃCZONY — metodologia/zbiór skills dla agentów kodujących.

## Stan faktyczny
README opisuje workflow od specyfikacji przez plan, worktree, TDD, subagenty, review i finalizację. Wspiera wiele harnessów, w tym Claude Code, Codex, Cursor, Gemini CLI, OpenCode i Hermes. Ma testy skills/infrastruktury oraz opcjonalną telemetrię wizualną.

## Ryzyka
Kompatybilność wielu harnessów, automatyczne triggery skills, wpływ promptów/instrukcji na agenta, telemetry opt-in i zależność od zewnętrznych marketplace.

## Priorytet
WYSOKI — istotne źródło metodologii dla ekosystemu.

## Kolejność prac
1. mapowanie skills i triggerów;
2. testy deterministyczności i konfliktów;
3. provenance/licencje;
4. izolacja telemetrii;
5. adaptacja wybranych wzorców do centralnego procesu audytów.

## Kryterium zakończenia
Każdy adoptowany workflow ma test, jasno określony trigger i brak niejawnego dostępu do danych.
