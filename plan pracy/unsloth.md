# Audyt: unsloth

## Status
AUDYT ZAKOŃCZONY — aktywny ekosystem lokalnego AI i desktop.

## Stan faktyczny
README opisuje natywną aplikację desktopową Windows/macOS/Linux, Studio i Core; obsługę LLM, GGUF, diffusion, audio, RAG, MCP, agentów, fine-tuningu i API OpenAI-compatible. Wspiera CPU/GPU i wiele backendów.

## Ryzyka
Model supply chain, wykonywanie narzędzi serwerowych, zdalny/LAN dostęp, hasła, GPU/sterowniki, duże modele i koszty/storage. README ostrzega, że server-side tools są domyślnie włączone przy ekspozycji Studio.

## Priorytet
KRYTYCZNY/WYSOKI.

## Kolejność prac
1. izolacja narzędzi i workspace;
2. secure defaults dla LAN/remote;
3. provenance modeli i checksumy;
4. kontrola zasobów GPU/storage;
5. testy desktop + API;
6. integracja wybranych wzorców z ekosystemem.

## Kryterium zakończenia
Brak niekontrolowanego dostępu zdalnego, sprawdzone modele/artefakty i powtarzalne testy kluczowych ścieżek.
