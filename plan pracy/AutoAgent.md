# AutoAgent — plan

- **Audyt:** 283
- **Status:** audyt zakończony; zero-code/self-developing framework agentów LLM.
- **Ustalenia:** natural-language agent/workflow editor, deep research, Docker, CLI, wiele dostawców LLM, możliwość generowania narzędzi i modyfikowania własnego repozytorium przez środowisko wykonawcze.
- **Ryzyka:** generowanie kodu, automatyczne klonowanie/zmiany repo, kontenery, klucze API, tool execution.
- **Priorytet:** KRYTYCZNY.
- **Kolejność:** sandbox → uprawnienia narzędzi → izolacja repozytoriów → sekrety → approval gates → testy generowanego kodu → audyt działań.
- **Kryterium:** żadna wygenerowana zmiana ani akcja zewnętrzna nie może uzyskać niejawnej autoryzacji; wszystkie granice są testowane.
- **Uwaga:** audyt nie oznacza gotowości produkcyjnej.
