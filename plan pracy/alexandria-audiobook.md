# Plan pracy — alexandria-audiobook

## Status
AUDYT ZAKOŃCZONY — aktywny lokalny generator audiobooków.

## Stan faktyczny
README opisuje pipeline LLM → adnotowany skrypt → obsada głosowa → TTS → edycja → eksport. Repozytorium zawiera `Dockerfile`, `docker-compose.yml`, notebook Colab, `app/`, `builtin_lora/`, prompty i dokumentację głosową. Obsługuje lokalne/kompatybilne z OpenAI API LLM, Qwen3-TTS, voice cloning, LoRA oraz eksport MP3/M4B/Audacity. Model i środowisko GPU są istotne dla reprodukowalności.

## Ryzyka
Prywatność tekstów i nagrań; provenance/licencje modeli i głosów; duże wagi; GPU/RAM/dysk; nieuprawnione klonowanie głosu.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować `app/`, Docker/Colab i zależności.
2. Przypiąć wersje i dodać testy CPU/GPU.
3. Izolować uploady i dane projektów.
4. Wprowadzić politykę zgody/proweniencji dla voice cloning.
5. Spolonizować UI i dokumentację.
6. Dodać CI/lint/testy oraz smoke generation na fixture.

## Kryterium zakończenia
Powtarzalny build, testy bez realnych danych, zweryfikowane licencje/model provenance i pełna polonizacja.