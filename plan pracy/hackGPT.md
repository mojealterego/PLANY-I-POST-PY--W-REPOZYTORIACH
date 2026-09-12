# hackGPT — plan pracy

## Status
AUDYT ZAKOŃCZONY — projekt bezpieczeństwa/AI.

## Stan faktyczny
Repozytorium średniej wielkości; nazwa i zakres wskazują na narzędzie związane z automatyzacją bezpieczeństwa. Wymaga zachowania ścisłej granicy autoryzowanych laboratoriów oraz weryfikacji rzeczywistych entrypointów, zależności i workflow.

## Ryzyka
- potencjalnie ofensywne funkcje;
- możliwość wykonywania poleceń lub interakcji z siecią;
- ryzyko niekontrolowanego rozszerzania zakresu narzędzia.

## Priorytet
WYSOKI

## Kolejność prac
1. Zmapować kod, manifesty, entrypointy i CI.
2. Klasyfikować operacje według wpływu i autoryzacji.
3. Dodać sandbox, allowlisty i audyt działań.
4. Testy wyłącznie na kontrolowanych fixture/lab.
5. Polonizacja/rebranding po hardeningu.

## Kryterium zakończenia
Każda funkcja wykonawcza ma jawny model uprawnień i ograniczony kontekst testowy.
