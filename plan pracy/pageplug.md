# Plan pracy — pageplug

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: fork/chińska dystrybucja Appsmith / low-code web + mini-program
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
PagePlug opisuje się jako chińska wersja Appsmith, z wizualnym builderem, API/data sources, JavaScript, React frontendem, Javą/Spring WebFlux po stronie serwera i Taro dla mobilnych mini-programów. README wskazuje MongoDB, Redis, Nginx, Docker oraz obsługę danych i formularzy. fileciteturn840file0

## Ryzyka
1. Jest to fork istniejącej platformy — provenance, upstream divergence i licencje są kluczowe.
2. Dane źródłowe przechodzą przez backend proxy; wymagana izolacja i kontrola credentialów.
3. Użytkownik może wykonywać JavaScript i konfigurować integracje API/DB.
4. Środowisko demo nie gwarantuje trwałości ani bezpieczeństwa danych.
5. Wielowarstwowy stack React/Java/Taro/Mongo/Redis zwiększa złożoność wdrożenia.

## Kolejność prac
1. Ustalić dokładny upstream commit i zakres własnych zmian.
2. Audytować auth/RBAC, data-source credentials i proxy.
3. Zabezpieczyć wykonywanie JavaScript oraz import/export DSL/JSON.
4. Zweryfikować Docker/Nginx/Redis/Mongo deployment i sekrety.
5. Dodać testy integracyjne i regression tests względem upstream.
6. Dopiero po audycie provenance rozważyć polonizację/rebranding własnych warstw.

## Kryterium zakończenia
Pełna mapa różnic względem upstream, bezpieczne data-source proxy i wykonanie kodu, zweryfikowany deployment oraz rozliczona licencja/provenance.
