# Plan pracy — virtual-phone

## Status
AUDYT ZAKOŃCZONY — aplikacja/usługa wirtualnej telefonii, wymagająca mapowania.

## Stan faktyczny
Repozytorium ma około 25 MB. Dokładny stos i model telekomunikacyjny należy potwierdzić w kodzie przed wdrożeniem.

## Ryzyka
- dane numerów i połączeń;
- SIP/HTTP exposure;
- auth i sekrety operatorów;
- koszty usług zewnętrznych.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapa usług i providerów.
2. Auth/TLS/secrets.
3. Testy telekomunikacyjne.
4. Privacy/retention.

## Kryterium zakończenia
Kontrolowana ekspozycja, bezpieczne sekrety i testy integracyjne.
