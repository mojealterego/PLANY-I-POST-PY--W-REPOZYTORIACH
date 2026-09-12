# Plan pracy — AgentGPT

## Stan audytu
- **Audyt:** zakończony
- **Klasyfikacja:** duży system webowy do konfiguracji i uruchamiania agentów autonomicznych
- **Priorytet:** KRYTYCZNY
- **Produkcja:** NIE

## Ustalenia
README opisuje architekturę rozdzieloną na CLI, bazę danych, backend FastAPI i frontend Next.js. Wskazany stos obejmuje Next.js/TypeScript, FastAPI, NextAuth, Prisma/SQLModel, bazę SQL, Tailwind/Headless UI, Zod/Pydantic i LangChain. Root zawiera m.in. `.env.example`, Docker Compose, `cli/`, `db/`, `next/`, `platform/`, `scripts/` oraz skrypty instalacyjne dla macOS/Linux i Windows.

## Ryzyka / luki
1. README jest wyraźnie historyczne: wskazuje Next.js 13, Node >=18 i starsze integracje; zgodność obecnego kodu trzeba zweryfikować na podstawie manifestów i lockfile.
2. System wykonuje autonomiczne zadania, więc granice narzędzi, promptów, sieci, kosztów i dostępu do danych wymagają osobnego threat modelu.
3. Należy zweryfikować model autoryzacji użytkowników oraz izolację tenantów/agentów.
4. Docker Compose i skrypty setup muszą zostać sprawdzone pod kątem sekretów, domyślnych portów, baz danych i ekspozycji usług.
5. Integracje z zewnętrznymi dostawcami modeli i wyszukiwania wymagają aktualnej polityki timeoutów, limitów i obsługi błędów.

## Kolejność prac
1. Zmapować `next/`, `platform/`, `db/`, `cli/`, `scripts/` i CI.
2. Ustalić aktualne wersje runtime i zależności na podstawie manifestów/lockfile.
3. Prześledzić pełny lifecycle agenta: konfiguracja → planowanie → narzędzia → wykonanie → wynik → pamięć.
4. Zdefiniować i przetestować granice autoryzacji oraz uprawnień narzędzi.
5. Dodać limity czasu, kosztu, liczby kroków i rozmiaru danych.
6. Zweryfikować izolację danych użytkowników i bezpieczeństwo sekretów.
7. Ustabilizować build frontend/backend oraz migracje DB.
8. Uruchomić testy jednostkowe/integracyjne/E2E i smoke deployment.
9. Dopiero po stabilizacji wykonać pełny rebranding i polonizację własnej warstwy.

## Kryterium zakończenia
Pełny lifecycle agenta musi być testowalny, granice narzędzi i danych jednoznaczne, a build/deployment reprodukowalny. Nie uznawać repozytorium za produkcyjne tylko dlatego, że posiada działający fundament.
