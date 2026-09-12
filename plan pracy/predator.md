# predator

## Status
AUDYT ZAKOŃCZONY — platforma do testów obciążeniowych API.

## Stan faktyczny
Rozbudowany projekt z UI, REST API, rozproszonymi generatorami obciążenia, bazami danych, harmonogramami, webhookami, Prometheus/Influx i integracją Chaos Mesh. README deklaruje testy lint/unit/integration oraz deployment Docker/Kubernetes.

## Ryzyka
Sam system może generować znaczny ruch sieciowy; musi być ograniczony do systemów autoryzowanych. Dodatkowe ryzyko stanowią Docker socket, Kubernetes i zewnętrzne webhooki.

## Priorytet
WYSOKI.

## Kolejność prac
1. Audyt runnerów i uprawnień kontenerów.
2. Limity ruchu i bezpieczne domyślne cele.
3. Walidacja webhooków i auth API.
4. Build/test CI i aktualizacja zależności.
5. Dokumentacja po polsku z wyraźną granicą autoryzacji.

## Kryterium zakończenia
Powtarzalne testy, kontrolowane generowanie ruchu, minimalne uprawnienia i brak możliwości przypadkowego skierowania testu na nieautoryzowany cel.