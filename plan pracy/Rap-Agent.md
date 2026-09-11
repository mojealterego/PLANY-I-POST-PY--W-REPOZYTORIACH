# Plan pracy — Rap-Agent

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: autonomiczny silnik kreatywny AI + API + MCP
- Priorytet: KRYTYCZNY
- Gałąź: `main`

## Ustalenia
- Kanoniczny runtime znajduje się w `src/omega/`; istnieją moduły kompatybilności w katalogu głównym oraz `legacy/`.
- Projekt ma `api.py`, `mcp_server.py`, `mcp.json`, `pyproject.toml`, `requirements.txt`, Dockerfile, Railway i katalog testów.
- Model trwałości opiera się na SQLite, z pamięcią skojarzeniową, stanem afektywnym, wydarzeniami ciągłości i kanonem twórcy.
- README deklaruje deterministyczne bramki jakości oraz testy i skrypt audytowy.
- Projekt jawnie nie przypisuje systemowi literalnej świadomości.

## Ryzyka
1. Trwała pamięć i kanon wymagają ścisłej integralności oraz kontroli migracji.
2. API/MCP zwiększa powierzchnię narzędziową i wymaga autoryzacji oraz limitów.
3. Root-level legacy może powodować podwójną implementację.
4. Proces generowania powinien mieć deterministyczne ograniczenia kosztu i cykli.

## Kolejność prac
1. Zweryfikować zgodność `src/omega/` z API, MCP i modułami legacy.
2. Ustalić kontrakty domenowe i jedyny composition root.
3. Przeprowadzić audyt SQLite, migracji, integralności zdarzeń i idempotencji.
4. Przetestować bramki jakości, odrzucenie/rebuild oraz zachowanie kanonu.
5. Zabezpieczyć API/MCP, sekrety, limity i obserwowalność.
6. Uporządkować legacy i CI; zweryfikować Docker/Railway.
7. Polonizować dokumentację i nazewnictwo użytkowe bez naruszania identyfikatorów technicznych.

## Kryterium zakończenia
Jeden kanoniczny runtime, testowalna trwałość stanu, bezpieczne API/MCP, deterministyczne bramki jakości i powtarzalny build.
