# artemis — plan pracy

## Stan audytu
**AUDYT ZAKOŃCZONY — zaawansowany system AI do automatyzacji i testowania urządzeń Android.**

## Ustalenia
- Python >=3.12; projekt posiada CLI, SDK, serwer MCP i konsolę webową.
- Integruje LangGraph/LangChain, MCP, wielu dostawców modeli, ADB/uiautomator2, FastAPI oraz przetwarzanie obrazu/wideo.
- Pytest ma rozdzielone testy jednostkowe/narzędziowe oraz domyślnie wyklucza integration/e2e/cloud/manual/android.
- Coverage ma próg 60%.
- README deklaruje automatyzację realnych telefonów, instalowanie helpera accessibility i benchmark AndroidWorld 99%+; te twierdzenia wymagają odtworzenia na aktualnym środowisku przed traktowaniem ich jako potwierdzone.
- Telemetria PostHog jest obecna jako zależność i wymaga osobnego audytu prywatności/zgód.

## Ryzyka
1. System może wykonywać realne działania na urządzeniu — konieczne są silne granice uprawnień i tryby bezpieczne.
2. MCP udostępnia narzędzia sterujące urządzeniem; należy zweryfikować autoryzację, izolację i ekspozycję sieciową.
3. Wielu dostawców modeli zwiększa liczbę ścieżek błędów i różnic zachowania.
4. Deklaracje benchmarkowe wymagają niezależnej reprodukcji.

## Plan
1. Zmapować moduły: CLI, agent, MCP, API, device subsystem, SDK, UI.
2. Zbudować threat model dla sterowania urządzeniem i MCP.
3. Zweryfikować auth, bind address, CORS, sekrety i polityki narzędzi.
4. Wymusić allowlisty działań, limity czasu, limity kroków i kill switch.
5. Rozszerzyć testy kontraktowe MCP i testy na emulatorze.
6. Odtworzyć benchmark AndroidWorld z wersją środowiska, seedami i artefaktami.
7. Zweryfikować telemetry/privacy i możliwość pełnego wyłączenia telemetrii.
8. Zbudować CI dla unit + integration + emulator smoke.
9. Przygotować polską dokumentację i dopiero po stabilizacji przeprowadzić rebranding.

## Kryterium zakończenia
Bezpieczna, powtarzalna ścieżka MCP→urządzenie, udokumentowane uprawnienia, testy emulatorowe i reprodukowalne benchmarki. Samo posiadanie działającego demo nie jest gotowością produkcyjną.
