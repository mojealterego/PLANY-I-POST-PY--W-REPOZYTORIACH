# No-code_AI_app_builder

## Status
AUDYT ZAKOŃCZONY — generator aplikacji AI na Next.js.

## Stan faktyczny
README opisuje Next.js 14, React 18, TypeScript, Tailwind, Firebase Auth/Firestore, Gemini i Vercel. System generuje kod React z promptu i udostępnia podgląd. Dokumentacja deklaruje limity, sandbox podglądu i skalowanie, które wymagają niezależnej weryfikacji.

## Ryzyka
Najważniejszy obszar to wykonywanie wygenerowanego kodu, izolacja podglądu, sekrety API, Firebase rules i wielodostępność. Deklaracje wydajności nie są dowodem.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Audyt API generation i preview sandbox.
2. Izolacja kodu nieufnego.
3. Weryfikacja auth/rules/tenant isolation.
4. Limity kosztowe i rate limiting.
5. Testy bezpieczeństwa, build i polonizacja.

## Kryterium zakończenia
Wygenerowany kod nie może uzyskać niekontrolowanego dostępu do hosta ani sekretów; auth, limity i testy są zweryfikowane.