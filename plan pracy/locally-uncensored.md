# Plan pracy — locally-uncensored

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: desktopowe lokalne studio AI / Tauri
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIE POTWIERDZONO DLA WŁASNEJ DYSTRYBUCJI

## Ustalenia
README opisuje aplikację Windows/Linux łączącą lokalny chat, coding agent, generowanie obrazów i wideo. Deklaruje obsługę wielu lokalnych backendów, ComfyUI, modeli diffusion, RAG, głosu oraz opcjonalnych usług chmurowych. README podaje release v2.6.7 z sierpnia 2026 oraz szczegółowe zmiany funkcjonalne. Projekt używa AGPL-3.0 i ma silną zależność od zewnętrznych komponentów/modeli. Jest to duży kandydat do analizy integracyjnej, ale nie należy automatycznie przejmować jego brandingów ani traktować deklarowanych benchmarków jako własnych.

## Ryzyka
1. Bardzo szeroka powierzchnia integracji: lokalne backendy, ComfyUI, modele, cloud APIs i coding agent.
2. Coding agent oraz zewnętrzne MCP mogą wykonywać operacje na lokalnym systemie — wymagają osobnej polityki uprawnień i izolacji.
3. Instalator pobierający komponenty wymaga weryfikacji podpisów, integralności i provenance.
4. Prywatność deklarowana jako local/offline wymaga potwierdzenia na poziomie kodu i wszystkich opcjonalnych telemetry/provider paths.
5. Licencje modeli i komponentów muszą być analizowane osobno od licencji aplikacji.
6. Deklaracje wydajności i kompatybilności GPU wymagają reprodukcji.

## Kolejność prac
1. Zmapować Tauri, frontend, backendy lokalne i zarządzanie procesami.
2. Zidentyfikować wszystkie operacje filesystem/network/subprocess.
3. Zbudować threat model dla coding agenta, MCP i instalatora.
4. Zweryfikować model manager, pobieranie, cache, integralność i licencje.
5. Przetestować offline mode oraz granice cloud/local.
6. Zweryfikować ComfyUI lifecycle, VRAM/RAM i recovery.
7. Przeprowadzić testy Windows/Linux i release reproducibility.
8. Dopiero potem ocenić możliwość wykorzystania architektury w projektach własnych.

## Kryterium zakończenia
Udokumentowane granice bezpieczeństwa desktopa i agenta, reprodukowalny build, zweryfikowany tryb lokalny/offline, testy procesów/model managera oraz kompletna mapa zależności i licencji.
