# atrilabs-engine — plan pracy

## Status
AUDYT ZAKOŃCZONY — silnik no-code/low-code.

## Stan faktyczny
Repozytorium ok. 33 MB z kodem silnika Atrilabs. Należy traktować jako potencjalną bazę technologiczną dla budowania interfejsów/aplikacji, ale nie zakładać gotowości produkcyjnej bez walidacji aktualnego builda i zależności.

## Ryzyka
- duża powierzchnia pluginów/komponentów;
- generowanie lub ładowanie kodu wymaga kontroli granic;
- kompatybilność starego upstreamu może być ograniczona.

## Priorytet
ŚREDNI/WYSOKI

## Kolejność prac
1. Audyt manifestów, build systemu i entrypointów.
2. Zweryfikować model rozszerzeń/pluginów.
3. Testy build/runtime i bezpieczeństwa kodu generowanego.
4. Ocenić przydatność jako komponentu dla przyszłego buildera.
5. Polonizacja/rebranding tylko warstwy własnej.

## Kryterium zakończenia
Powtarzalny build, testy rozszerzeń i udokumentowana granica bezpieczeństwa pluginów.
