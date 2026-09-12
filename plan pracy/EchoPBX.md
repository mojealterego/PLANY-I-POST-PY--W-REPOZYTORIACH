# Plan pracy — EchoPBX

## Status
AUDYT ZAKOŃCZONY — projekt PBX/telekomunikacyjny wymagający dalszego mapowania.

## Stan faktyczny
Repozytorium jest średniej wielkości i ma osobny branch główny. Dokładny zakres komponentów PBX należy potwierdzić w źródłach przed implementacją zmian.

## Ryzyka
- ekspozycja usług SIP/PBX;
- auth, TLS i sekrety;
- dane połączeń i prywatność;
- konfiguracja sieciowa oraz persistence.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapa usług i portów.
2. Auth/TLS/secrets.
3. Testy SIP i konfiguracji.
4. Dokumentacja i polonizacja.

## Kryterium zakończenia
Zweryfikowana topologia, bezpieczne sekrety, testy usług i kontrolowana ekspozycja sieciowa.
