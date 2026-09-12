# Plan pracy — hermes-agent

## Stan audytu
**AUDYT ZAKOŃCZONY — projekt duży, aktywny, wysokiego ryzyka operacyjnego.**

## Zakres i charakter
Hermes Agent jest wieloplatformowym agentem AI z TUI, gatewayem komunikacyjnym, pamięcią, umiejętnościami, harmonogramem, MCP oraz wieloma backendami wykonawczymi. README deklaruje obsługę CLI, Telegrama, Discorda, Slacka, WhatsApp, Signal i innych powierzchni. `pyproject.toml` wskazuje Python >=3.11, wersję 0.13.146, szeroki zestaw providerów i opcjonalnych integracji oraz rozbudowany zestaw testów.

## Ustalenia
- Domyślna ścieżka terminalowa może wykonywać polecenia na hoście.
- Projekt sam wskazuje izolację OS jako rzeczywistą granicę bezpieczeństwa; approval gate i filtry treści są heurystykami, nie sandboxem.
- SECURITY.md rozróżnia izolację backendu terminalowego od izolacji całego procesu.
- Powierzchnie sieciowe wymagają allowlisty; identyfikator sesji nie jest granicą autoryzacji.
- Pluginy i skills działają w procesie agenta i należy traktować je jako kod uprzywilejowany.
- `pyproject.toml` zawiera wiele mocno przypiętych zależności oraz komentarze dotyczące incydentów supply-chain; jednocześnie występuje niespójność: `tzdata` jest zadeklarowane dwukrotnie z różnymi zakresami.
- Profil `all` nadal odwołuje się do `hermes-agent[mistral]`, mimo że opis poniżej deklaracji extra wskazuje usunięcie extra Mistral po incydencie PyPI. To wymaga weryfikacji przed budowaniem profilu all.
- Testy są skonfigurowane pod katalog `tests`, domyślnie bez integracji; potrzebne jest rozdzielenie wyników unit/integration/e2e.

## Ryzyka
1. Krytyczne: wykonywanie kodu, MCP, pluginów, skills i subprocessów poza ograniczeniem backendu terminalowego.
2. Krytyczne: błędna konfiguracja zewnętrznych gatewayów/API może rozszerzyć powierzchnię dostępu.
3. Wysokie: supply-chain przy dużej liczbie providerów, extras i instalowanych komponentów.
4. Wysokie: wieloplatformowość Linux/macOS/Windows/Termux/Android zwiększa macierz regresji.
5. Średnie: niespójność deklaracji zależności i profili instalacyjnych.

## Priorytet
**KRYTYCZNY**

## Kolejność prac
1. Zmapować pełny graf modułów: agent → tools → gateway → terminal/MCP → plugins/skills.
2. Zweryfikować wszystkie granice OS sandbox oraz ścieżki omijające terminal backend.
3. Zweryfikować autoryzację każdej powierzchni sieciowej i lokalnego IPC.
4. Naprawić i przetestować deklaracje extras/dependencies, w tym profil `all` i duplikat `tzdata`.
5. Uruchomić testy jednostkowe, integracyjne i smoke na wspieranych platformach.
6. Dodać testy kontraktowe dla allowlist, credential scoping, izolacji i fail-closed.
7. Zweryfikować instalatory oraz integralność pobieranych komponentów.
8. Dopiero po stabilizacji wykonać rebranding i pełną polonizację własnej warstwy dokumentacyjnej.

## Kryterium zakończenia
Brak niezweryfikowanych ścieżek wykonania poza deklarowaną granicą bezpieczeństwa, przechodzące testy krytycznych powierzchni, spójne zależności i reprodukowalna instalacja/build. Audyt nie oznacza statusu produkcyjnego.
