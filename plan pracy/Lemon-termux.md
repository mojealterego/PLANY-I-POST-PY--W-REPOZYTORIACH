# Lemon-termux

## Status
AUDYT ZAKOŃCZONY — projekt badawczo-referencyjny o wysokim ryzyku.

## Stan faktyczny
Bash/Termux/Linux; README opisuje narzędzie powiązane z L3MON/AhMyth, z funkcjami GPS, mikrofonu, kontaktów, SMS, logów połączeń, schowka/powiadomień, plików, kolejki poleceń i budowania APK.

## Ryzyka
Zakres obejmuje zdalne monitorowanie i pozyskiwanie danych z urządzeń. Wysokie ryzyko nadużycia, prywatności i nieautoryzowanego dostępu; zależności i instrukcje są historyczne.

## Priorytet
KRYTYCZNY — wyłącznie analiza defensywna/laboratoryjna.

## Kolejność prac
1. Inwentaryzacja kodu i przepływów uprawnień.
2. Klasyfikacja komponentów i danych wrażliwych.
3. Usunięcie niepotrzebnych sekretów/instrukcji operacyjnych.
4. Testy wyłącznie na kontrolowanych urządzeniach.
5. Dokumentacja po polsku i granice użycia.

## Kryterium zakończenia
Audyt reprodukowalny, jasna granica laboratoryjna, brak niekontrolowanego rozszerzania funkcji monitorujących; dopiero potem ewentualna modernizacja.