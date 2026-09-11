# Plan pracy — tuskbot

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Agent AI napisany w Go, działający przez Telegram.
- Architektura opiera się na MCP jako mechanizmie narzędziowym.
- Posiada lokalny RAG z SQLite-vec i llama.cpp/GGUF oraz wsparcie Ollama.
- Narzędzia obejmują filesystem, shell execution i zarządzanie MCP.
- Konfiguracja obejmuje token Telegrama, identyfikator właściciela, modele, embeddingi i dostawców LLM.
- README wskazuje niezrealizowane elementy roadmapy: MCP Skills, cron/heartbeat i multi-agent orchestration.

## Ryzyka
1. Shell i filesystem tworzą wysokie ryzyko wykonania nieautoryzowanych działań.
2. Należy bezwzględnie zweryfikować izolację właściciela Telegrama.
3. MCP lifecycle wymaga kontroli procesu, timeoutów i uprawnień.
4. Lokalny RAG wymaga testów jakości i wydajności.
5. Roadmapa sugeruje istotne brakujące funkcje.

## Plan implementacji
1. Zmapować pakiety Go i granice odpowiedzialności.
2. Zweryfikować middleware autoryzacji Telegram Owner ID.
3. Wprowadzić policy engine dla filesystem/shell/MCP.
4. Dodać timeouty, limity zasobów i izolację procesów.
5. Zweryfikować pipeline embeddingów i SQLite-vec.
6. Ujednolicić konfigurację i obsługę sekretów.
7. Dodać testy jednostkowe/integracyjne dla narzędzi i agent loop.
8. Zaprojektować Skills, heartbeat i multi-agent orchestration jako osobne moduły.
9. Przeprowadzić testy odporności na błędy dostawców LLM i MCP.
10. Spolonizować dokumentację i komunikaty użytkownika.

## Kryterium zakończenia
Agent bezpiecznie izoluje użytkownika, ma testowalne polityki narzędzi, odporną obsługę procesów i kompletną dokumentację produkcyjną.