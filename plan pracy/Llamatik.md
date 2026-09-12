# AUDYT 360 — Llamatik

## Status
Audyt wykonany. Kotlin Multiplatform AI library z natywnym llama.cpp, whisper.cpp i stable-diffusion.cpp.

## Ustalenia
Android/iOS/Desktop/WASM, lokalne inference, opcjonalny backend HTTP, GGUF/BIN, embeddings, RAG, streaming, JSON schema, KV cache i równoległe sesje.

## Ryzyka
Native C++/JNI/Kotlin Native, pamięć i zasoby GPU, pobieranie modeli, bezpieczeństwo zdalnego trybu, pliki sesji/KV cache oraz kompatybilność wersji native.

## Plan prac
Zweryfikować wszystkie actual/expect implementacje, natywny bridge, lifecycle zasobów, concurrency i testy na każdej platformie. Dodać provenance modeli i polską dokumentację.

## Kryterium zakończenia
Powtarzalne buildy wszystkich wspieranych targetów, testy native bridge i bezpieczne zarządzanie modelami/sesjami.
