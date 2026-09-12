# Audyt 88 — layla-sdk

## Stan
AUDYT ZAKOŃCZONY — publiczny TypeScript SDK dla mini-aplikacji Layla.

## Ustalenia
Repo ma `src`, `examples`, dokumentację skills/references, `.github`, package-lock i tsconfig. README opisuje WebView bridge przez `@layla-network/sdk`, chat/multimodal, streaming, pamięć, TTS/STT, audio, generowanie obrazu/muzyki, prywatny SQLite per mini-app i lokalne mocki. Wydania generują również bundle Agent Skill.

## Ryzyka
- WebView bridge jako granica zaufania;
- prywatność pamięci, plików i SQLite;
- uprawnienia generowania audio/obrazu/muzyki;
- bezpieczeństwo skill bundle używanego przez inne agenty;
- zgodność wersji SDK ↔ host Layla.

## Priorytet
WYSOKI.

## Kolejność prac
API contracts → bridge permissions → SQLite/file sandbox → skill bundle provenance → example tests → release automation → compatibility matrix → Polish docs.

## Kryterium zakończenia
Każda funkcja host bridge ma jawne uprawnienie, test i wersję kontraktu, a mini-app nie może wyjść poza przydzielone zasoby.