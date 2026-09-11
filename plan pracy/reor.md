# Plan pracy — reor

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Lokalna aplikacja desktopowa do zarządzania wiedzą osobistą.
- Główne funkcje: automatyczne linkowanie notatek, semantic search i RAG Q&A.
- Modele lokalne przez Ollama i Transformers.js; LanceDB jako warstwa wektorowa.
- Dane użytkownika są deklarowane jako lokalne.
- Projekt buduje się przez Node/npm i posiada wersję desktopową dla macOS, Linux i Windows.
- Licencja: AGPL-3.0.

## Ryzyka
1. Należy zweryfikować, czy wszystkie ścieżki danych faktycznie pozostają lokalne.
2. Integracje z API zgodnymi z OpenAI muszą być jednoznacznie oznaczone.
3. Należy zbadać odporność indeksowania na duże zbiory notatek.
4. Trzeba zweryfikować aktualność zależności oraz proces pakowania desktopowego.

## Plan implementacji
1. Zmapować frontend, warstwę indeksowania, RAG i storage.
2. Zidentyfikować granice domenowe i odpowiedzialności modułów.
3. Zweryfikować wszystkie połączenia sieciowe i przepływy danych.
4. Zweryfikować lifecycle indeksów LanceDB i synchronizacji notatek.
5. Dodać testy importu, indeksowania, wyszukiwania i RAG.
6. Usprawnić obsługę dużych korpusów i odbudowy indeksu.
7. Zweryfikować buildy macOS/Windows/Linux.
8. Przeprowadzić audyt bezpieczeństwa danych lokalnych.
9. Wprowadzić pełną polską dokumentację i interfejs językowy.

## Kryterium zakończenia
Powtarzalne buildy desktopowe, testy przepływu notatka → indeks → retrieval → odpowiedź, potwierdzona lokalność danych i kompletna dokumentacja.