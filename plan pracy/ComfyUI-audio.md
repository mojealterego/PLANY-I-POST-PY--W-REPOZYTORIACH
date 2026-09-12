# Plan pracy — ComfyUI-audio

## Status
AUDYT ZAKOŃCZONY — eksperymentalne rozszerzenie audio dla ComfyUI; rozwój wstrzymany przez autora.

## Stan faktyczny
README wymienia Tacotron2, MusicGen/AudioGen, Tortoise, VALL-E X, VoiceFixer oraz utility nodes. Instalacja korzysta z PyTorch CUDA i osobnych wymagań Windows/Linux. Projekt deklaruje eksperymentalność i brak dalszego utrzymania.

## Ryzyka
nieaktualne zależności/model API; CUDA/OS compatibility; provenance modeli i forków; przetwarzanie audio; brak aktywnego maintenance.

## Priorytet
NISKI/ŚREDNI — REFERENCYJNY.

## Kolejność prac
1. Zamrozić snapshot i zmapować wymagania.
2. Oznaczyć status projektu jako eksperymentalny.
3. Zweryfikować licencje wszystkich modeli/forków.
4. Jeśli używany dalej: odseparować zależności i dodać smoke tests.
5. Dodać polski opis integracji z ComfyUI.

## Kryterium zakończenia
Reprodukowalny snapshot albo świadomie utrzymywany fork z testem generacji audio.