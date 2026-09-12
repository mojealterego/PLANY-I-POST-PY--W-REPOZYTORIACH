# Plan pracy — tauri

## Status
AUDYT ZAKOŃCZONY — 2026-09-12.

## Ustalenia
Upstream framework Tauri, stabilny, Rust + frontend HTML/JS/CSS, WebView przez tao/WRY, desktop/mobile, bundling, updater, tray i native notifications. README wskazuje CI oraz architekturę wieloplatformową.

## Ryzyka
- granica Rust/WebView i API komend;
- uprawnienia systemowe i capability model;
- aktualizacje, podpisywanie i integralność artefaktów;
- różnice platformowe.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Mapowanie workspace, crates, JS/CLI i CI.
2. Audyt capability/IPC/updater.
3. Testy platformowe i supply-chain.
4. Uporządkowanie polskich materiałów integracyjnych w repozytoriach zależnych.

## Kryterium zakończenia
Audyt implementacyjny potwierdzony testami; repozytorium traktowane jako upstream/reference, nie jako kandydat do bezpośredniego rebrandingu.
