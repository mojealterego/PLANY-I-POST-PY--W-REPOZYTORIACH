# Audyt 389 — PornHub

## Status
AUDYT ZAKOŃCZONY — archiwalny bot Telegram do pobierania treści z serwisu dla dorosłych.

## Stan faktyczny
README opisuje bota Telegram, wdrażanie z użyciem Pythona, FFmpeg i zmiennych środowiskowych oraz komendy `start`, `repo` i `help`. Projekt przewiduje pobieranie materiałów i udostępnianie ich przez bota. Dokumentacja odwołuje się do zewnętrznego repozytorium źródłowego i historycznego wdrożenia Heroku/VPS.

## Klasyfikacja
MATERIAŁ ARCHIWALNY / EDUKACYJNY. Nie rozwijać jako usługi dystrybucji treści ani narzędzia do masowego pobierania.

## Ryzyka
- prawa autorskie, regulaminy usług źródłowych i dystrybucja treści;
- treści przeznaczone dla dorosłych oraz konieczność skutecznych ograniczeń dostępu;
- Telegram bot token, zmienne środowiskowe i konfiguracja wdrożeniowa;
- pobieranie, buforowanie i przesyłanie materiałów przez serwer;
- zależności systemowe FFmpeg/Python i brak potwierdzonej współczesnej macierzy testów;
- ekspozycja komend i danych użytkowników przez bota.

## Priorytet
WYSOKI dla klasyfikacji i bezpieczeństwa; NISKI dla rozwoju produktu.

## Kolejność prac
1. Zamrozić zakres jako projekt referencyjny.
2. Przejrzeć zależności, konfigurację i sposób przechowywania sekretów.
3. Usunąć z dokumentacji instrukcje masowej dystrybucji oraz dane/konfiguracje demonstracyjne, które mogłyby ujawniać sekrety.
4. Jeżeli materiał ma pozostać dydaktyczny, ograniczyć testy do syntetycznych fixture'ów i lokalnego mocka Telegram/API.
5. Udokumentować kontrolę wieku, zgody, prawa do materiałów i politykę retencji danych.

## Kryterium zakończenia
Repozytorium pozostaje jednoznacznie oznaczone jako archiwalne, nie prowadzi nieautoryzowanej dystrybucji treści, nie zawiera sekretów i posiada bezpieczny, lokalny zakres demonstracyjny.

**Audyt ≠ produkcja.**
