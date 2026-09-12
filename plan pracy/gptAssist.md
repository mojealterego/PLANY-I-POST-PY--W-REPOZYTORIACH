# Plan pracy — gptAssist

## Stan audytu
**AUDYT ZAKOŃCZONY — lekki klient Android/WebView, projekt referencyjny do dalszej modernizacji.**

## Ustalenia
README opisuje gptAssist jako prosty wrapper WebView dla ChatGPT z blokowaniem niepotrzebnych URL-i, trybem restricted/unrestricted, obsługą plików i głosu. Projekt jest licencjonowany GPLv3. Rootowy `build.gradle` używa Android Gradle Plugin 8.2.2.

## Ryzyka i braki
- brak potwierdzonej aktualnej macierzy SDK/build-tools/JDK;
- WebView i mechanizm allowlisty URL są krytyczną granicą bezpieczeństwa;
- należy zweryfikować obsługę uploadów, linków zewnętrznych, JavaScript, cookies, WebView storage i intentów;
- należy zweryfikować, czy tryb unrestricted nie może przypadkowo stać się domyślnym lub omijać zabezpieczeń;
- należy sprawdzić aktualność zależności Android oraz polityki certyfikatów/TLS;
- wymagane są testy na kilku wersjach Androida i urządzeniach fizycznych;
- README zawiera treści upstreamowe i informacje o wymaganiach Google, które należy traktować jako materiał do weryfikacji, nie jako własną specyfikację projektu.

## Priorytet
**WYSOKI**

## Kolejność prac
1. Zmapować Activity, WebView, URL filtering i obsługę intentów.
2. Zdefiniować formalny model dozwolonych domen i nawigacji.
3. Zweryfikować upload/download, storage, cookies, JS bridge i zewnętrzne schematy URI.
4. Zaktualizować i przypiąć zależności oraz SDK.
5. Dodać testy jednostkowe filtra URL i testy instrumentacyjne WebView.
6. Dodać CI dla debug/release/lint.
7. Uporządkować licencje/upstream attribution.
8. Następnie rebranding i pełna polonizacja własnego interfejsu/dokumentacji.

## Kryterium zakończenia
Powtarzalny build APK, przechodzący lint/testy, formalnie zweryfikowana polityka nawigacji WebView oraz brak niezamierzonych ścieżek opuszczających model prywatności. Audyt nie oznacza produkcji.
