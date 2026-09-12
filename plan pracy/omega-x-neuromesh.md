# Plan pracy — omega-x-neuromesh

## Status audytu
- Klasyfikacja: projekt bezpieczeństwa/sterowania dla automatyzacji Unreal Engine.
- Audyt: wykonany na podstawie README, referencyjnego prototypu i testów.
- Produkcja: NIE — integracja z rzeczywistym Unreal Engine 5.8 i MCP pozostaje nieweryfikowana.

## Ustalenia
- Architektura deklaruje łańcuch `PROPOSE -> POLICY -> SAFETY GATE -> AUTHORIZATION -> APPROVAL -> SNAPSHOT -> APPLY -> VERIFY -> COMMIT -> AUDIT`.
- Referencyjny prototyp jest bez zależności zewnętrznych i implementuje default-deny, allowlistę capability, chronione zasoby, wymaganie akceptacji dla wysokiego ryzyka, walidację geometrii, rollback oraz ślad audytowy.
- Testy referencyjne obejmują 8 przypadków, w tym odmowy capability, zasobu chronionego, brak akceptacji, wartości niefinitywne, przekroczenie limitu i rollback po nieudanej weryfikacji postcondition.
- README jawnie rozdziela obecny prototyp od runtime Unreal i wire-level MCP.

## Priorytety
1. Odtworzyć plugin w rzeczywistym UE 5.8 i zweryfikować kompilację.
2. Zweryfikować kontrakt MCP, transport lokalny, timeouty, autoryzację i granice zasobów.
3. Utrzymać default-deny także poza prototypem; nie ufać samemu klientowi/modelowi.
4. Dodać testy integracyjne plugin ↔ control plane oraz testy awarii/rollbacku.
5. Ustandaryzować identyfikację operatora, approval i audyt z ochroną integralności.
6. Dodać fuzz/property tests dla parserów, policy engine i walidacji geometrii.
7. Zdefiniować benchmarki dopiero jako mierzalne eksperymenty, nie jako deklarowane osiągnięcia.
8. Przejrzeć dokumentację grantową tak, aby każde twierdzenie miało źródło albo oznaczenie założenia.
9. Pełna polonizacja/rebranding dopiero po ustabilizowaniu kontraktów technicznych.

## Kryterium zakończenia
Gotowość kolejnego etapu wymaga reprodukowalnego builda UE 5.8, działającego kontraktu MCP, przechodzących testów bezpieczeństwa i regresji oraz dowodów na działanie kontroli w realnym środowisku.
