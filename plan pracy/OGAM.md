# Audyt 329 — OGAM

## Stan
AUDYT ZAKOŃCZONY — wieloplatformowa aplikacja on-device AI, krytyczna.

## Ustalenia
README opisuje React Native dla Android/iOS/macOS, lokalne LLM/GGUF, GPU/NPU, Stable Diffusion, vision, Whisper, PDF, SQLite, tool calling, zdalne serwery OpenAI-compatible oraz MCP. Pro zawiera integracje Calendar/email/Linear/Notion/GitHub, ale działania są deklarowane jako draft → approval. Repo posiada testy Jest/RNTL, JUnit, XCTest i CI.

## Ryzyka
MCP/tool calling; lokalne uprawnienia; sekrety; pliki użytkownika; model download; NPU/GPU; pamięć; integracje wykonujące działania.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zweryfikować permission matrix i approval gates.
2. Zmapować storage, model manager i download provenance.
3. Zweryfikować MCP i zewnętrzne akcje.
4. Uruchomić testy na Android/iOS.

## Kryterium zakończenia
Żadna akcja zewnętrzna bez jawnej zgody, bezpieczne przechowywanie sekretów i zweryfikowany lifecycle modeli/danych.