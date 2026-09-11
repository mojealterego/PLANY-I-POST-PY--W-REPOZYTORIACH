# Plan pracy — ai-game-builder

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Repozytorium ma strukturę projektu Unity: `Assets/`, `Packages/`, `.github/`.
- README zawiera wyłącznie tytuł projektu, więc dokumentacja projektowa jest praktycznie nieobecna.
- `Packages/manifest.json` deklaruje Unity Ads 4.4.2 oraz Unity Purchasing 4.9.4, a także moduły audio, IMGUI, JSON i UnityWebRequest.
- Projekt wymaga pełnego rozpoznania scen, skryptów, konfiguracji Build Settings, wersji Unity, pipeline'u CI i zależności Asset Store.

## Ryzyka
1. Brak dokumentacji utrudnia odtworzenie środowiska.
2. Ads/IAP wymagają audytu konfiguracji produkcyjnej i sekretów.
3. Nieznany jest stan testów i kompilacji.
4. Nieznana jest architektura kodu domenowego i warstwy prezentacji.

## Plan implementacji
1. Zidentyfikować wersję Unity i platformy docelowe.
2. Zmapować `Assets` według domen: gameplay, UI, dane, infrastruktura.
3. Zmapować wszystkie skrypty i zależności.
4. Zweryfikować Ads/IAP oraz konfigurację usług zewnętrznych.
5. Zbudować testowalną architekturę domenową, aplikacyjną i infrastrukturalną.
6. Dodać testy EditMode/PlayMode oraz CI.
7. Uporządkować konfigurację środowisk.
8. Przygotować polską dokumentację i README produkcyjne.
9. Wykonać kompilację wszystkich wspieranych platform.
10. Dopiero po przejściu testów wykonać rebranding i oznaczyć wersję produkcyjną.

## Kryterium zakończenia
Powtarzalny build, przechodzące testy, kompletna dokumentacja, brak niezaimplementowanych placeholderów oraz jawnie zdefiniowane konfiguracje produkcyjne.