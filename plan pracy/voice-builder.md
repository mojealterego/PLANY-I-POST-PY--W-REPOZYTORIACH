# voice-builder

## Status
AUDYT ZAKOŃCZONY — eksperymentalny system budowania głosów TTS na GCP/Firebase.

## Stan faktyczny
README opisuje Docker, GCP/App Engine, Firebase, Cloud Functions, GCS oraz silniki Festival/Merlin. System przetwarza dane głosowe, buduje modele i udostępnia syntezę; istnieje mechanizm custom data exporter.

## Ryzyka
Wysokie koszty i uprawnienia chmurowe, dostęp do bucketów GCS, API keys oraz dane głosowe. Dokumentacja zawiera historyczne ACL i bezpośrednie IP/HTTP.

## Priorytet
WYSOKI.

## Kolejność prac
1. Audyt IAM/GCS/sekretów.
2. Izolacja pipeline'ów treningowych.
3. Walidacja danych wejściowych i exporterów.
4. Testy end-to-end i kosztowe.
5. Aktualizacja deploymentu i polonizacja.

## Kryterium zakończenia
Minimalne uprawnienia, bezpieczne sekrety, kontrola danych głosowych i reprodukowalny pipeline.