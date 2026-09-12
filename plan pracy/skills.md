# Audyt 81 — skills

## Stan
AUDYT ZAKOŃCZONY — biblioteka ElevenLabs Agent Skills.

## Ustalenia
README deklaruje zestaw skills zgodnych ze specyfikacją Agent Skills: TTS, STT, agents, sound effects, music, voice changer, isolation, dubbing i konfiguracja API. Repo zawiera również trigger/functional evals uruchamiane przez `evals/run_all.py`, z izolowanym workspace dla testów funkcjonalnych. Licencja MIT.

## Ryzyka
- każda umiejętność może wykonywać działania kosztowne lub przetwarzać dane audio;
- klucz API nie może trafiać do treści/logów;
- zgodność z Agent Skills specification musi być testowana maszynowo;
- należy rozdzielić dokumentację od kodu wykonywalnego.

## Priorytet
WYSOKI.

## Kolejność prac
Walidacja schematów skills → testy trigger/functional → sekrety → sandbox narzędzi → wersjonowanie → CI/eval reports → polonizacja.

## Kryterium zakończenia
Każdy skill ma test kontraktowy, ograniczenia uprawnień i deterministyczny sposób raportowania błędów.