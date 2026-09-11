# Plan pracy — kernel-browser-automation-starter

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Starter Next.js 15/App Router przeznaczony do agentowej automatyzacji przeglądarki.
- Wykorzystuje Kernel SDK, Kernel AI SDK, Vercel AI SDK i OpenAI.
- README pokazuje osobne endpointy tworzenia/usuwania przeglądarki oraz agenta.
- Agent wykonuje kod Playwright przez narzędzie AI SDK i ma limit 20 kroków.
- Konfiguracja wymaga kluczy Kernel i OpenAI oraz wdrożenia Vercel.

## Ryzyka
1. Narzędzie agenta wykonujące automatyzację przeglądarki jest granicą wysokiego zaufania.
2. Sesje przeglądarek i ich identyfikatory muszą być izolowane między użytkownikami.
3. Należy zweryfikować walidację promptów, URL-i i wyników narzędzia.
4. Dokumentacja nadal zawiera język i identyfikatory startera źródłowego.

## Plan implementacji
1. Audyt route handlers i lifecycle sesji przeglądarki.
2. Wprowadzić silną walidację wejścia i kontrolę dozwolonych operacji.
3. Zabezpieczyć identyfikatory sesji przed wyciekiem między klientami.
4. Dodać timeouty, limity zasobów i obsługę awarii Kernel.
5. Zdefiniować model logowania działań agenta bez ujawniania sekretów.
6. Dodać testy jednostkowe i E2E dla utworzenia, wykonania i zamknięcia sesji.
7. Ujednolicić konfigurację środowiskową.
8. Przepisać dokumentację na język polski i przygotować instrukcję produkcyjną.
9. Zweryfikować deployment Vercel.

## Kryterium zakończenia
Bezpieczna izolacja sesji, testy automatyzacji, poprawna obsługa błędów i timeoutów, produkcyjny build oraz pełna polska dokumentacja.