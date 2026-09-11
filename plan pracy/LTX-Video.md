# Plan pracy — LTX-Video

## Stan audytu
**AUDYT ZAKOŃCZONY — 2026-09-12**

## Klasyfikacja
Repozytorium źródłowe modelu generowania wideo LTX-Video. Jest to duży projekt Python/ML, a README wskazuje, że bieżący rozwój został przeniesiony do LTX-2. Repozytorium należy traktować jako bazę badawczo-technologiczną i komponent referencyjny, nie jako zwykłą aplikację użytkową.

## Ustalenia
- Python `>=3.10`.
- Pakiet `ltx_video*` budowany przez setuptools.
- Główne zależności: PyTorch, Diffusers, Transformers, SentencePiece, Hugging Face Hub, einops, timm.
- Opcjonalna ścieżka inferencji obejmuje `imageio[ffmpeg]`, `av` i `torchvision`.
- Opcjonalne testy używają pytest.
- Główne elementy repozytorium: `ltx_video/`, `configs/`, `docs/`, `tests/`, `inference.py`.
- README deklaruje text-to-video, image-to-video, keyframes, video extension, video-to-video oraz integracje z ComfyUI i Diffusers.
- README wskazuje LTX-2 jako następcę i główne miejsce dalszego rozwoju.
- Repozytorium zawiera konfiguracje modeli oraz artefakty dokumentacyjne związane z wieloma wersjami modeli.

## Ryzyka
1. Ryzyko dezaktualizacji względem LTX-2 i rozdzielenia właściwego kierunku rozwoju.
2. Wysoka wrażliwość na zgodność wersji PyTorch/Transformers/Diffusers/CUDA/MPS.
3. Kosztowna i sprzętowo zależna walidacja inferencji.
4. Duża powierzchnia modeli, konfiguracji i workflowów zwiększająca ryzyko niespójności.
5. Brak potwierdzenia kompletności automatycznej walidacji CI na podstawie znalezionego pliku workflow pod oczekiwaną ścieżką.
6. Licencjonowanie modeli/weightów musi być analizowane osobno od licencji kodu.

## Plan refaktoryzacji
1. Ustalić relację repozytorium LTX-Video do LTX-2 i oznaczyć kanoniczne źródło dalszego rozwoju.
2. Zmapować publiczne API pakietu `ltx_video` oraz oddzielić API stabilne od wewnętrznego.
3. Ustalić macierz kompatybilności Python/PyTorch/CUDA/MPS/Transformers/Diffusers.
4. Uporządkować konfiguracje modeli i nazewnictwo wersji bez usuwania artefaktów wymaganych do reprodukcji.
5. Rozbudować testy kontraktowe dla konfiguracji, ładowania modeli, pipeline'ów i kształtów tensorów.
6. Dodać deterministyczne testy smoke dla inferencji na minimalnym modelu/fixture, bez wymagania pełnego modelu produkcyjnego w każdym CI.
7. Zweryfikować integracje ComfyUI i Diffusers oraz granice odpowiedzialności między repozytoriami.
8. Zweryfikować licencje kodu, modeli, checkpointów i materiałów referencyjnych.
9. Ujednolicić dokumentację operacyjną po polsku, zachowując oryginalne nazwy techniczne i cytowania źródeł.
10. Zbudować reprodukowalny proces instalacji, testów i inferencji.

## Kryterium zakończenia
Repozytorium zostanie uznane za zrefaktoryzowane dopiero po przejściu testów kontraktowych i smoke, potwierdzeniu kompatybilności środowiska, uporządkowaniu konfiguracji oraz potwierdzeniu, że dokumentacja jednoznacznie wskazuje status LTX-Video względem LTX-2.
