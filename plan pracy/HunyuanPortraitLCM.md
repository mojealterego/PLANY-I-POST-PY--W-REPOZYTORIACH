# HunyuanPortraitLCM

## Status
AUDYT ZAKOŃCZONY — badawczy model animacji portretów.

## Stan faktyczny
Projekt opisuje HunyuanPortrait, dyfuzyjny system animacji portretu sterowany materiałem wideo, z rozdzieleniem tożsamości i ruchu. README wskazuje PyTorch, Gradio, LCM/LoRA, wymaganie NVIDIA 3090 24 GB i Linux. Zawiera instrukcje pobierania wag z Hugging Face oraz kod inferencji.

## Ryzyka
Wysokie wymagania sprzętowe, duże modele, provenance wag i licencje komponentów. Animacja wizerunku może mieć zastosowania deepfake; należy zachować zgodę na materiał referencyjny i jasne oznaczenie treści syntetycznych.

## Priorytet
WYSOKI — badania/eksperymenty.

## Kolejność prac
1. Zweryfikować requirements, checkpointy i wersje CUDA/PyTorch.
2. Udokumentować provenance i licencje wszystkich wag.
3. Dodać walidację wejścia i ograniczenia zasobów.
4. Testy jakości/reprodukowalności inference.
5. Polonizacja dokumentacji z zasadami zgody i oznaczania materiałów.

## Kryterium zakończenia
Reprodukowalna konfiguracja badawcza, poprawne licencje/provenance i bezpieczne zasady używania wizerunku.