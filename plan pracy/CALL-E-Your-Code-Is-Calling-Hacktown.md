# Plan pracy — CALL-E-Your-Code-Is-Calling-Hacktown

## Status audytu
AUDYT ZAKOŃCZONY — repozytorium #43 w bieżącym przebiegu.

## Stan faktyczny
**AegisFleet — Incident Voice Command** to TypeScriptowy prototyp sterowanego workflow telefonicznego dla incydentów logistycznych. README opisuje maszynę stanów, policy gate, idempotency reservation, symulator dry-run, adapter CALL-E, walidację wyniku, evidence/confidence gate, eskalację do człowieka, deduplikację webhooków i ledger audytowy. Demo lokalne nie wykonuje połączeń.

Repo zawiera `src/`, `tests/`, dokumentację bezpieczeństwa/architektury, `package.json`, `tsconfig.json`, konfigurację Vitest i CI.

## Mocne strony
- domyślny dry-run bez efektów zewnętrznych;
- jawny opt-in tryb live;
- walidacja E.164 i ochrona numerów fixture;
- idempotency przed I/O providera;
- wymaganie dowodu i wysokiej pewności przed automatycznym rozwiązaniem incydentu;
- testy regresyjne i CI.

## Ryzyka / backlog produkcyjny
README prawidłowo wskazuje brak m.in. trwałego idempotency store, trwałego audytu, uwierzytelnionych webhooków, RBAC, zarządzania sekretami, polityk retencji/prywatności, globalnego kill switcha, integracji TMS/ERP i testów obciążeniowych/fault injection.

## Kolejność prac
1. Zweryfikować wszystkie moduły domeny, FSM, policy, validation, ledger i webhook.
2. Uruchomić testy, typecheck i CI.
3. Zabezpieczyć provider webhook signature/authentication przed dopuszczeniem live ingress.
4. Wprowadzić trwałą idempotencję i trwały audit ledger z weryfikacją integralności.
5. Dodać RBAC, secret rotation, retencję i kill switch.
6. Testy integracyjne, obciążeniowe i fault injection.
7. Polonizacja dokumentacji i rebranding.

## Kryterium zakończenia
Live execution może być uznane za gotowe dopiero po spełnieniu wszystkich kontroli bezpieczeństwa, trwałości i audytowalności; sam działający dry-run nie jest statusem produkcyjnym.
