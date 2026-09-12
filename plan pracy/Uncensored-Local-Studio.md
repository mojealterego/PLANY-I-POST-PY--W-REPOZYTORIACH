# Plan pracy — Uncensored-Local-Studio

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: wieloplatformowe lokalne studio AI / Tauri + React
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia z repozytorium
README opisuje lokalne studio dla Stable Diffusion, LLM, Whisper i Kokoro TTS na Windows, Linux i macOS. Architektura obejmuje frontend Vite/React, lokalne backendy `stable-diffusion.cpp`, `llama.cpp`, `whisper.cpp` i Kokoro, katalogi modeli oraz skrypty instalacyjne. Model Manager może pobierać wagi z Hugging Face, a system automatycznie dobiera backend GPU/NPU. fileciteturn812file0 Manifest frontendu używa React 19, Vite 8 i Tauri 2. fileciteturn815file0

## Ryzyka
1. Pobieranie i uruchamianie obcych wag modeli jest elementem łańcucha dostaw.
2. Lokalny runtime uruchamia procesy backendowe i wymaga ścisłej izolacji filesystem/network.
3. Automatyczna konfiguracja backendów może wykonywać operacje systemowe z podwyższonym wpływem.
4. Wieloplatformowość zwiększa liczbę kombinacji GPU/NPU/sterowników.
5. Należy zweryfikować provenance modeli, licencje oraz integralność binariów.
6. Deklaracja „100% offline” wymaga audytu wszystkich ścieżek instalacji, aktualizacji i pobierania modeli.

## Kolejność prac
1. Zmapować granice Tauri ↔ frontend ↔ procesy backendowe.
2. Zabezpieczyć uruchamianie subprocessów i ścieżki plików.
3. Dodać allowlisty źródeł modeli, checksumy i manifesty artefaktów.
4. Rozdzielić tryb instalacji/aktualizacji od trybu inference.
5. Zweryfikować brak niejawnej telemetrii i połączeń sieciowych.
6. Zbudować macierz testów Windows/Linux/macOS × GPU/NPU/CPU.

## Kryterium zakończenia
Powtarzalne buildy Tauri, bezpieczny lifecycle procesów i modeli, zweryfikowana izolacja lokalnych danych, kontrolowany supply chain modeli oraz testy na reprezentatywnych platformach.
