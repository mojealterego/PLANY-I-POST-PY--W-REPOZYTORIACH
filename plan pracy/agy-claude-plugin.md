# agy-claude-plugin — plan pracy

## Status
AUDYT ZAKOŃCZONY — mały plugin Claude Code.

## Stan faktyczny
Plugin integrujący CLI `agy` z trzema komendami: review, personas i ask. Centralny wrapper `scripts/agy-pipe.sh` buforuje prompt, używa stdin i twardych timeoutów. README opisuje `.claude-plugin/plugin.json`, commands i skrypt wrappera.

## Ryzyka
- wykonywanie zewnętrznego CLI z kontekstu Claude Code;
- wejścia promptów/diffów mogą zawierać dane wrażliwe;
- zależność od niezweryfikowanego w audycie kontraktu `agy` i dostępności `timeout`.

## Priorytet
ŚREDNI

## Kolejność prac
1. Zweryfikować plugin manifest i skrypt shell.
2. Dodać testy timeoutów, exit codes i pustych wejść.
3. Ograniczyć środowisko subprocess i przepływ danych.
4. Udokumentować kompatybilność platform.
5. Polonizacja/rebranding.

## Kryterium zakończenia
Deterministyczne smoke testy, bezpieczny subprocess i jasna polityka danych wejściowych.
