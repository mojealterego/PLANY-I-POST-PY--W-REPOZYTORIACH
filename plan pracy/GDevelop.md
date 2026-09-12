# Plan pracy — GDevelop

## Status
AUDYT ZAKOŃCZONY — duży upstreamowy silnik/IDE no-code do gier.

## Stan faktyczny
README opisuje pełne środowisko 2D/3D/multiplayer, edytor, silnik, rozszerzenia i usługi. Architektura obejmuje `Core`, `GDJS`, `GDevelop.js`, `newIDE` oraz `Extensions`; stack obejmuje TypeScript, PixiJS, Three.js, React, Electron i WebAssembly. Repo ma CI dla wielu platform i testy.

## Ryzyka
ogromny zakres kodu; rozszerzenia i WASM; Electron; build wieloplatformowy; supply chain; AI-assisted authoring; kompatybilność projektów.

## Priorytet
WYSOKI / REFERENCYJNY.

## Kolejność prac
1. Mapa modułów i granic procesu build.
2. Audyt rozszerzeń/WASM/Electron.
3. CI/test matrix i provenance artefaktów.
4. Bezpieczne ograniczenia dla AI-generated changes.
5. Polski indeks architektury i dokumentacji.

## Kryterium zakończenia
Zweryfikowana architektura i build/test matrix; brak niekontrolowanego wykonania rozszerzeń.