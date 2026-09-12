# Plan pracy — sanna

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: infrastruktura governance dla agentów AI / Python SDK + gateway
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README opisuje kryptograficzne receipts, konstytucję governance w YAML, Ed25519, gateway/interceptor oraz pięć deterministycznych coherence checks. Ważne rozróżnienie: dekorator obserwacyjny działa post-execution, natomiast gateway/interceptor egzekwują politykę pre-execution. Projekt deklaruje wersjonowanie fingerprintów, zakresów invariants i podpisów. fileciteturn822file0

## Ryzyka
1. Błąd w enforcement surface może dopuścić akcję przed kontrolą.
2. Klucze podpisujące konstytucję i receipts wymagają rotacji, ochrony i separacji ról.
3. Receipts mogą zawierać dane wejściowe/wyjściowe i informacje o agentach.
4. Polityki `cannot_execute` / `must_escalate` / `can_execute` muszą być jednoznaczne i deterministyczne.
5. Integracja z MCP wymaga odporności na złośliwe lub błędne tool calls.

## Kolejność prac
1. Formalnie przetestować pre-execution enforcement.
2. Audytować key management, rotację i provenance konstytucji.
3. Zweryfikować deterministyczność fingerprintów i schematu receipts.
4. Testy fuzz/negative dla policy matching i parametrów narzędzi.
5. Testy integracyjne gateway ↔ MCP oraz recovery po awarii.
6. Udokumentować retencję i redakcję danych w receipts.

## Kryterium zakończenia
Każda niedozwolona akcja jest blokowana przed wykonaniem, receipts są kryptograficznie weryfikowalne, a polityki i lifecycle kluczy są pokryte testami negatywnymi.
