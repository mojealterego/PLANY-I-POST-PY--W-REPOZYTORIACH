# Plan pracy — USB-Uncensored-LLM

## Status
AUDYT ZAKOŃCZONY — przenośne środowisko lokalnego AI.

## Stan faktyczny
README opisuje przenośne środowisko Windows/macOS/Linux/Android z izolowanym Pythonem, silnikiem Ollama, katalogiem modeli GGUF i lokalnym HTTP UI. Modele są pobierane na urządzenie, a część projektu deklaruje dostęp z sieci LAN.

## Ryzyka
wykonywalne binaria na USB; skrypty instalacyjne; pobieranie modeli; integralność plików; HTTP w LAN; trwała historia rozmów; błędna interpretacja „zero dependency”/„secure”; provenance modeli.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować skrypty start/install i binaria per OS.
2. Zweryfikować checksum/signing artefaktów i źródła modeli.
3. Zamknąć serwer UI do localhost domyślnie; jawne włączenie LAN.
4. Zabezpieczyć dane rozmów i uprawnienia filesystemu.
5. Polonizacja i testy na czystych hostach.

## Kryterium zakończenia
Reprodukowalna dystrybucja, zweryfikowane artefakty, bezpieczne domyślne bindy i testy wieloplatformowe.