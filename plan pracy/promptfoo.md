# Audyt: promptfoo

## Status
AUDYT ZAKOŃCZONY — dojrzałe narzędzie eval/red-team LLM.

## Stan faktyczny
README opisuje CLI i bibliotekę do automatycznych ewaluacji, porównywania modeli, CI/CD, code scanning i testów bezpieczeństwa. Wymaga Node >=22.22, rekomenduje 24 LTS. Projekt deklaruje lokalne evals i licencję MIT; README wskazuje obecne powiązanie z OpenAI.

## Ryzyka
Duża powierzchnia integracji providerów, dane promptów/evaluations, konfiguracje red-team oraz możliwość uruchamiania testów przeciw usługom bez właściwego zakresu.

## Priorytet
WYSOKI.

## Kolejność prac
1. mapowanie providerów i sekretów;
2. kontrola zakresu testów red-team;
3. reprodukowalność evals i benchmarków;
4. CI policy i raportowanie;
5. polonizacja tylko warstwy własnej, zachowując upstream provenance.

## Kryterium zakończenia
Evals są powtarzalne, sekrety nie trafiają do artefaktów, a testy bezpieczeństwa mają jawny scope.
