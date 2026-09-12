# Plan pracy — hack-skills

## Status
AUDYT ZAKOŃCZONY — baza Agent Skills dla autoryzowanych prac bezpieczeństwa.

## Stan faktyczny
Repozytorium organizuje 101 skills w standardzie `skills/{id}/SKILL.md`, z master entry, kategoriami i tematami głębokimi. Obejmuje web/API/auth, mobile, reverse engineering, forensics, AI/ML i inne domeny bezpieczeństwa. Publikowane są także statyczny interfejs oraz zaszyfrowany ZIP.

## Ryzyka
Treści ofensywne, możliwość użycia poza autoryzowanym zakresem, provenance materiałów, aktualność porad, integralność paczek i ryzyko instrukcji nadmiernie operacyjnych.

## Priorytet
KRYTYCZNY — LAB/EDUKACJA.

## Kolejność prac
1. Provenance każdego skillu.
2. Klasyfikacja: edukacja/CTF/autoryzowany test.
3. Walidacja loadera i struktury SKILL.md.
4. Testy treści i linków.
5. Integralność publikowanych artefaktów.
6. Jasne granice użycia i polonizacja dokumentacji.

## Kryterium zakończenia
Każdy skill ma źródło, zakres zastosowania i wersję; katalog nie sugeruje nieautoryzowanego użycia, a artefakty publikacyjne są weryfikowalne.