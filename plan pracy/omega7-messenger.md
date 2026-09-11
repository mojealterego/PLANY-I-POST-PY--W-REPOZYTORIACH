# Plan pracy — omega7-messenger

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Androidowy pakiet źródłowy Ω7 Messenger 0.8.1.
- README deklaruje polski interfejs, AES-256-GCM, Android Keystore, biometrie, blokadę dostępu, szyfrowane pairing/trusted-device stores oraz limit 7 urządzeń.
- Transport fail-closed: brak wysyłania sieciowego do czasu skonfigurowania rzeczywistego E2EE.
- Dokumentacja jawnie zaznacza brak produkcyjnej certyfikacji E2EE i wymienia brakujący protokół, backend/relay, synchronizację multi-device, testy fizyczne, fuzzing i niezależny audyt bezpieczeństwa.
- CI obejmuje testy, lint i build APK, ale lokalny build nie został w README potwierdzony.

## Ryzyka
1. Najwyższy priorytet: projekt nie może być przedstawiany jako gotowy komunikator E2EE.
2. Protokół kryptograficzny i model kluczy wymagają niezależnego przeglądu.
3. Pairing i multi-device synchronization są krytycznymi granicami bezpieczeństwa.
4. Konieczne są testy recovery, concurrency, fuzzing i fizyczne urządzenia.

## Plan implementacji
1. Zmapować kryptografię, Keystore, pairing i storage.
2. Formalnie zdefiniować protokół E2EE i model zagrożeń.
3. Zaimplementować backend/relay zgodnie z modelem bezpieczeństwa.
4. Zaprojektować bezpieczną synchronizację wielu urządzeń.
5. Dodać fuzzing parserów i warstw transportowych.
6. Przeprowadzić testy konkurencyjności, recovery i utraty kluczy.
7. Wykonać testy na rzeczywistych urządzeniach Android.
8. Zweryfikować CI oraz reproducible APK builds.
9. Dopiero po niezależnym przeglądzie bezpieczeństwa zmienić status produkcyjny.
10. Utrzymać polską dokumentację bezpieczeństwa jako źródło prawdy.

## Kryterium zakończenia
Zweryfikowany protokół E2EE, bezpieczny pairing/synchronizacja, przechodzące testy bezpieczeństwa i urządzeń oraz niezależny audyt kryptograficzny.