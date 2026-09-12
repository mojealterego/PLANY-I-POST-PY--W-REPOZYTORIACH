# Plan pracy — claude-code-android

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: Android/Termux uruchamianie agenta kodującego
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Repo dokumentuje trzy ścieżki uruchomienia Claude Code na Androidzie: natywny Termux z patchowanym binarium linux-arm64, Ubuntu przez proot-distro oraz eksperymentalny Android Virtualization Framework. README zawiera osobny model bezpieczeństwa, ograniczenia SSRF/permissions, testy claimów i instrukcje ADB. fileciteturn842file0

## Ryzyka
1. Agent kodujący może czytać/zapisywać pliki i wykonywać polecenia.
2. Path A patchuje binarium Linux i posiada auto-update wrapper — supply chain jest krytyczny.
3. Wymuszanie DNS Google może zmieniać model prywatności i zachowanie VPN/split DNS.
4. ADB wireless i Termux:API mogą rozszerzać zasięg agenta.
5. Ścieżka AVF ma ograniczoną, niejednoznacznie zweryfikowaną kompatybilność urządzeń.

## Kolejność prac
1. Formalnie zweryfikować capability matrix dla każdej ścieżki.
2. Audytować instalatory, checksumy i aktualizacje.
3. Zweryfikować permission model agenta i separację web-read/file-write.
4. Przetestować SSRF guard i ADB boundary.
5. Zweryfikować DNS behavior oraz wpływ na prywatność.
6. Testy fizycznych urządzeń i release reproducibility.

## Kryterium zakończenia
Każda ścieżka ma zweryfikowany zakres uprawnień, integralność instalowanych artefaktów, testy bezpieczeństwa i powtarzalną procedurę aktualizacji.
