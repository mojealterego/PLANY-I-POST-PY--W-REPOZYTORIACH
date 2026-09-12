# Audyt 335 — maid

## Stan
AUDYT ZAKOŃCZONY — Android React Native, lokalne i zdalne LLM.

## Ustalenia
README opisuje lokalne GGUF przez llama.cpp, zdalnych providerów, pobieranie modeli z Hugging Face, własne pliki GGUF, rozmowy, parametry, Supabase sync i Maise TTS. Projekt ma CI build/test/CodeQL i podaje fingerprinty kluczy podpisujących APK.

## Ryzyka
Model download/supply chain; API keys; lokalne pliki; opcjonalny sync chatu; podpisy APK; zdalne providery.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zweryfikować credentials i storage.
2. Zweryfikować provenance modeli i integralność downloadów.
3. Audytować signing/release.
4. Przetestować izolację lokalnych danych i sync.

## Kryterium zakończenia
Brak wycieku kluczy/danych, zweryfikowane modele i podpisy oraz testy krytycznych ścieżek.