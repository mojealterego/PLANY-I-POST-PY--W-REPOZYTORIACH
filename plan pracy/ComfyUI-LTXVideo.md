# Audyt 332 — ComfyUI-LTXVideo

## Stan
AUDYT ZAKOŃCZONY — custom nodes/workflows dla LTX-2.

## Ustalenia
README opisuje rozszerzenia ComfyUI dla LTX-2.3: T2V/I2V, IC-LoRA, HDR, dubbing, upscaling oraz text-to-audio. Wymagania obejmują ComfyUI, CUDA GPU z 32 GB+ VRAM i 100 GB+ dysku; modele są pobierane osobno.

## Ryzyka
Duże modele i koszty zasobów; provenance checkpointów/LoRA; generowanie obrazu/głosu; kompatybilność wersji ComfyUI.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Zweryfikować node API i wersję ComfyUI.
2. Zmapować wymagane modele i checksum/provenance.
3. Przetestować workflows 2.3 i regresje.
4. Oddzielić dane referencyjne od produkcyjnych assetów.

## Kryterium zakończenia
Powtarzalne workflow, jawne wersje modeli i zweryfikowana kompatybilność.