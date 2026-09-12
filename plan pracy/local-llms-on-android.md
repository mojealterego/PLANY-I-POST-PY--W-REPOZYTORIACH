# Audyt 338 — local-llms-on-android

## Stan
AUDYT ZAKOŃCZONY — Android on-device LLM.

## Ustalenia
Pocket LLM obsługuje lokalne Qwen/Gemma przez ONNX i LiteRT, chat, głos, obrazy, OCR, kamerę, historię lokalną oraz pobieranie modeli. README wymaga fizycznego urządzenia i rozdziela APK od modeli.

## Ryzyka
Model supply chain/downloads; prywatne obrazy i kamera; pamięć/RAM; uprawnienia Android; provenance licencji modeli.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Provenance modeli → storage/uprawnienia → integralność downloadów → testy urządzeniowe → wydajność.

## Kryterium zakończenia
Bezpieczny lifecycle modeli i danych oraz zweryfikowane buildy Android.