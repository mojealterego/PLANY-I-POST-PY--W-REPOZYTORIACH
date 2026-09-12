# Plan pracy — eSIM-Tools

## Status
AUDYT ZAKOŃCZONY — webowe narzędzie do zarządzania eSIM Giffgaff/Simyo.

## Stan faktyczny
README opisuje konwersję SIM→eSIM, transfer urządzenia i generowanie QR, logowanie oraz weryfikację kodami. Repo zawiera wersję chińską i angielską, `src/assets`, dokumentację i Netlify deployment. Część instrukcji odwołuje się do metod nieoficjalnych dla nowych użytkowników.

## Ryzyka
poświadczenia operatorów; OTP; profile eSIM/QR; scraping/nieoficjalne API; sekrety frontendowe; dane telekomunikacyjne; aktualność procedur operatorów.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zmapować źródła API i proces generowania/otrzymywania QR.
2. Zweryfikować, że sekrety nie trafiają do klienta.
3. Ograniczyć logi i retencję danych.
4. Usunąć lub wyraźnie oznaczyć nieoficjalne ścieżki aktywacji.
5. Dodać testy mock i polską lokalizację.

## Kryterium zakończenia
Bezpieczny model auth/OTP, brak ujawniania danych eSIM i jasno udokumentowana zgodność z operatorami.