# Audyt 388 — PornHubBot

## Status
AUDYT ZAKOŃCZONY — archiwalny Python 2.7/Scrapy crawler zapisujący metadane i adresy materiałów z serwisu dla dorosłych do MongoDB.

## Stan faktyczny
README deklaruje Scrapy, MongoDB, middleware z pulą Cookie/UA, równoległe żądania, paginację oraz pola takie jak tytuł, czas trwania, URL, okładka i adres MP4. Drzewo repozytorium zawiera projekt Scrapy `PornHub/`, `settings.py`, pipeline MongoDB, middleware, spider, listę user-agentów, `quickstart.py`, `scrapy.cfg` i obrazy dokumentacyjne. Konfiguracja ustawia `ROBOTSTXT_OBEY=True`, `DOWNLOAD_DELAY=1` i `CONCURRENT_REQUESTS=20`.

## Klasyfikacja
MATERIAŁ ARCHIWALNY / EDUKACYJNY. Repozytorium nie powinno być rozwijane jako wysokowydajny scraper ani narzędzie do masowego pobierania treści.

## Ryzyka
- zgodność z regulaminem źródła, prawami autorskimi i prawami do treści;
- prywatność i przechowywanie metadanych/adresów materiałów;
- stare środowisko Python 2.7 i nieaktualne zależności;
- mechanizmy Cookie/UA oraz współbieżność mogą zwiększać obciążenie usługi;
- brak potwierdzonego testu reprodukowalności i brak nowoczesnego zarządzania sekretami/konfiguracją;
- dane MongoDB mogą zawierać identyfikatory i adresy wymagające kontroli dostępu.

## Priorytet
WYSOKI dla klasyfikacji i bezpieczeństwa; NISKI dla dalszego rozwoju funkcjonalnego.

## Kolejność prac
1. Zachować repo jako materiał referencyjny i udokumentować jego wiek.
2. Zidentyfikować zależności i brakujące artefakty środowiska bez uruchamiania masowego crawlowania.
3. Usunąć z dokumentacji sugestie wysokowydajnego pobierania i wszelkie sekrety/dane testowe.
4. Dodać bezpieczne testy jednostkowe dla parsera/modelu danych na lokalnych fixture'ach.
5. Udokumentować zgodność, limity, robots.txt i politykę danych.
6. Dopiero w razie uzasadnionego celu edukacyjnego rozważać migrację do współczesnego Pythona na syntetycznych fixture'ach.

## Kryterium zakończenia
Repozytorium jest jednoznacznie sklasyfikowane jako archiwalny materiał edukacyjny, nie wykonuje masowego pobierania bez jawnego upoważnienia, nie przechowuje przypadkowych danych wrażliwych i posiada testowalny, lokalny zakres demonstracyjny.

**Audyt ≠ produkcja.**
