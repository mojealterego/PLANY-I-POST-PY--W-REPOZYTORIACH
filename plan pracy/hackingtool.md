# hackingtool

## Status
AUDYT ZAKOŃCZONY — rozbudowany konsolowy toolkit bezpieczeństwa z warstwą AI.

## Stan faktyczny
Python 3.10+, 215 kuratorowanych narzędzi w 21 kategoriach, katalog, wyszukiwanie, planowanie celów i warstwa rekomendacji AI. README deklaruje bezpieczne instalacje, pinowanie pobrań, SHA-256, SBOM i podpisane wydania.

## Ryzyka
Zakres obejmuje narzędzia ofensywne, w tym phishing, DDoS, RAT i cracking. Najważniejsze jest utrzymanie autoryzowanego zakresu oraz niedopuszczenie do automatycznego wykonania. Supply chain i instalacja zewnętrznych narzędzi wymagają ciągłej kontroli.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Audyt mechanizmu AI→narzędzie→polecenie.
2. Weryfikacja zasady „nic nie wykonuje się automatycznie”.
3. Kontrola katalogu, źródeł, hashy i SBOM.
4. Testy sandbox/allowlist i CI.
5. Polonizacja dokumentacji przy zachowaniu granic laboratoryjnych.

## Kryterium zakończenia
Brak nieautoryzowanego wykonania, wymuszona kontrola celu, integralność artefaktów i pełna ścieżka audytowa.