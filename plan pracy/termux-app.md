# Audyt 318 — termux-app

## Stan
AUDYT ZAKOŃCZONY — repozytorium referencyjne/upstream.

## Ustalenia
Termux to Androidowa aplikacja terminalowa i środowisko Linux; README rozdziela aplikację od pakietów. Występują pluginy, współdzielony `com.termux`, wiele kanałów dystrybucji, GitHub Actions dla build/test oraz jawnie opisane ryzyka podpisywania APK. GitHub buildy używają publicznie znanego klucza testowego.

## Ryzyka
Supply chain i podpisy APK; uprawnienia Android; procesy i pluginy; zgodność źródeł dystrybucji.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Zweryfikować manifesty/Gradle i moduły.
2. Zweryfikować pipeline release/signing.
3. Zweryfikować testy na wspieranych Androidach.
4. Zachować jako wzorzec infrastruktury, nie jako bezpośredni kandydat do przepisywania.

## Kryterium zakończenia
Mapa modułów, buildów, testów i łańcucha podpisywania bez niezweryfikowanych deklaracji bezpieczeństwa.