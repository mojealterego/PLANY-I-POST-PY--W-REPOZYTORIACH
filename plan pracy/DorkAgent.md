# Plan pracy — DorkAgent

## Status
AUDYT ZAKOŃCZONY — mały agent wyszukiwania/informacji OSINT.

## Stan faktyczny
Repozytorium ma około 800 KB i `main`. Przed użyciem produkcyjnym trzeba potwierdzić źródła wyszukiwania, parsery, zakres zapytań i sposób zapisu wyników.

## Ryzyka
- jakość i provenance wyników;
- scraping i limity usług;
- potencjalne zastosowania dual-use;
- brak gwarancji świeżości danych.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapa źródeł i parserów.
2. Ograniczenia zapytań/rate limits.
3. Provenance i cytowanie wyników.
4. Testy fixture offline.

## Kryterium zakończenia
Powtarzalny agent z kontrolowanym zakresem wyszukiwania i wiarygodnym śladem źródeł.
