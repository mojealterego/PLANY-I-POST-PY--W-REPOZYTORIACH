# Audyt 322 — datadog-agent

## Stan
AUDYT ZAKOŃCZONY — duży agent obserwowalności/infrastruktury, referencyjny.

## Ustalenia
Repozytorium obejmuje agenta systemowego integrującego zbieranie metryk, logów i zdarzeń oraz liczne integracje. Duży rozmiar wymaga analizy modułowej zamiast ręcznego przepisywania całości.

## Ryzyka
Uprawnienia systemowe; dostęp do hosta; dane telemetryczne; integracje i konfiguracja; supply chain.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Zmapować moduły i konfigurację.
2. Przeanalizować permissions i collectors.
3. Zweryfikować CI/testy i wersje zależności.
4. Wykorzystać wzorce obserwowalności jako referencję.

## Kryterium zakończenia
Pełna mapa powierzchni systemowej i danych telemetrycznych.