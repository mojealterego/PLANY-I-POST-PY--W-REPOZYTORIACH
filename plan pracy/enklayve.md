# Plan pracy — enklayve

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Desktopowa aplikacja local-first oparta o Tauri 2, React 19/TypeScript/Vite i Rust.
- Funkcje obejmują analizę PDF/DOCX/TXT/Markdown/Excel/CSV, RAG, embeddingi, lokalne LLM oraz GPU acceleration.
- Backend Rust deklaruje szyfrowanie AES-256-GCM, biometrię, backup/restore, eksport i cache modeli.
- llama.cpp jest używane przez `llama-cpp-2`, embeddingi przez fastembed.
- Deklarowane wsparcie macOS, Windows i Linux oraz Metal/CUDA.

## Ryzyka
1. Kryptografia i biometria wymagają audytu implementacji, nie tylko deklaracji README.
2. Wieloplatformowość zwiększa liczbę ścieżek bezpieczeństwa i buildów.
3. Obsługa dużych modeli może powodować presję na pamięć i błędy OOM.
4. Lokalność danych musi zostać potwierdzona przez analizę połączeń sieciowych.
5. Dokumentacja zawiera placeholderowe adresy `user/...` w linkach GitHub, które wymagają korekty.

## Plan implementacji
1. Zmapować frontend Tauri oraz komendy Rust.
2. Zweryfikować granice IPC i walidację argumentów komend.
3. Przeprowadzić audyt szyfrowania, keychainów i biometrii per platforma.
4. Przeanalizować pipeline dokumentów, OCR, chunking, embeddingi i retrieval.
5. Zweryfikować model cache i bezpieczne pobieranie modeli.
6. Zmierzyć pamięć, czas ładowania i throughput CPU/GPU.
7. Zbudować macOS/Windows/Linux w CI.
8. Dodać testy integracyjne dla dokumentów i RAG.
9. Zweryfikować brak niezamierzonych połączeń zewnętrznych.
10. Wykonać pełną polonizację UI i dokumentacji oraz poprawić linki.

## Kryterium zakończenia
Przejście testów bezpieczeństwa i funkcjonalnych, działające buildy trzech platform, zweryfikowana lokalność danych oraz kompletna polska dokumentacja.