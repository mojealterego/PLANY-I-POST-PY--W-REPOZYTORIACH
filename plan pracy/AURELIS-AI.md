# Plan pracy — AURELIS-AI

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Projekt jest produkcyjnie zorientowaną aplikacją AI typu workspace.
- Stack: Next.js 16 App Router, React 19, AI SDK 6, Vercel AI Gateway, Tailwind 4, Radix/shadcn, Drizzle + PostgreSQL, Auth.js/NextAuth, Vercel Blob, Playwright, OpenTelemetry.
- README deklaruje polski-first oraz istniejący rebranding do AURELIS AI.
- Repozytorium posiada `.env.example`, `.github`, `app`, `components`, `hooks`, konfigurację Drizzle i Biome.
- Dokumentacja już definiuje quality gates: lint, test i build.

## Ryzyka
1. Wysoka liczba integracji zwiększa powierzchnię błędów konfiguracyjnych.
2. Auth, pliki, baza danych i narzędzia AI wymagają osobnego audytu granic autoryzacji.
3. Należy zweryfikować zgodność deklarowanego stacku z faktycznym kodem.
4. Należy sprawdzić migracje DB, polityki przechowywania plików i obsługę sekretów.

## Plan implementacji
1. Zmapować moduły `app`, `components`, `hooks`, warstwę danych i usług AI.
2. Zweryfikować granice Clean Architecture i zależności kierunkowe.
3. Przeprowadzić audyt authn/authz dla każdej trasy danych.
4. Przeprowadzić audyt uploadów, Blob i walidacji wejścia.
5. Zweryfikować Drizzle schema/migracje i transakcje.
6. Zweryfikować streaming AI, tool calls i obsługę błędów.
7. Uruchomić lint, testy, E2E i production build.
8. Uzupełnić polską dokumentację techniczną oraz instrukcje wdrożeniowe.
9. Ujednolicić publiczne identyfikatory marki AURELIS bez naruszania kompatybilności wewnętrznej.
10. Wykonać końcowy przegląd bezpieczeństwa i wydajności.

## Kryterium zakończenia
Pełny build produkcyjny, przechodzące testy, zweryfikowane auth/DB/storage/AI, brak krytycznych błędów oraz kompletna polska dokumentacja.