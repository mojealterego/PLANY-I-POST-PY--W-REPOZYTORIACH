# Audyt 328 — ChatDev

## Stan
AUDYT ZAKOŃCZONY — framework wieloagentowego developmentu.

## Ustalenia
Projekt automatyzuje współpracę wielu ról/agendów przy tworzeniu oprogramowania. Kluczowe są komunikacja agentów, generowanie artefaktów, wykonanie kodu i kontrola jakości.

## Ryzyka
Wykonywanie wygenerowanego kodu; prompt injection; pętla agentowa; brak deterministycznej walidacji; koszty.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Rozdzielić generowanie od wykonania.
2. Dodać sandbox, testy i approval gates.
3. Zachować provenance artefaktów.

## Kryterium zakończenia
Każdy artefakt jest testowalny, śledzalny i wykonywany w kontrolowanym środowisku.