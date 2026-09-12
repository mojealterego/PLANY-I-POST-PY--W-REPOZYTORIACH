# MetaGPT — plan pracy

## Stan audytu
**AUDYT ZAKOŃCZONY — duży framework wieloagentowy i repozytorium referencyjne.**

## Ustalenia
- Framework modeluje zespół programistyczny jako system ról agentowych i SOP.
- README opisuje generowanie wymagań, architektury, kodu, dokumentacji oraz integracje z wieloma modelami.
- Dokumentacja instalacyjna wskazuje historyczne ograniczenie Python >=3.9 i <3.12; wymaga to sprawdzenia względem aktualnego kodu i deklaracji pakietu.
- Projekt ma znaczny rozmiar i szeroki zakres, dlatego audyt należy prowadzić modułowo zamiast traktować README jako pełny obraz.
- Repozytorium zawiera materiały, przykłady i zależności wymagające kontroli kompatybilności.

## Ryzyka
1. Rozbieżność między deklarowanymi wersjami Pythona a aktualnym środowiskiem.
2. Wieloagentowość zwiększa koszty, nieprzewidywalność i ryzyko propagacji błędnych decyzji.
3. Integracje z modelami i narzędziami zewnętrznymi wymagają izolacji sekretów i polityk uprawnień.
4. Historyczne benchmarki/claims wymagają oddzielenia od aktualnie reprodukowalnych wyników.

## Plan
1. Zmapować strukturę core, roles, actions, tools, memory i examples.
2. Ustalić aktualną macierz Python/LLM/provider/framework.
3. Zidentyfikować granice agent→narzędzie→efekt zewnętrzny.
4. Wprowadzić deterministyczne policy gates dla działań skutkujących efektami ubocznymi.
5. Dodać testy kontraktowe ról, workflow/SOP, pamięci i obsługi błędów.
6. Zbudować smoke suite dla reprezentatywnych scenariuszy bez realnych efektów ubocznych.
7. Zweryfikować licencje, przykłady, zależności i dokumentację.
8. Dopiero po stabilizacji przygotować polski indeks/README i rebranding własnych warstw.

## Kryterium zakończenia
Zweryfikowana macierz kompatybilności, testowalny rdzeń wieloagentowy, bezpieczne granice narzędzi i reprodukowalne scenariusze. Projekt referencyjny nie powinien być oznaczany jako produkcyjny bez niezależnej walidacji.
