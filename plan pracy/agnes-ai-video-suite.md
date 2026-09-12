# Plan pracy — agnes-ai-video-suite

## Status
AUDYT ZAKOŃCZONY — self-hosted prototyper wideo EchoSync.

## Stan faktyczny
README opisuje generowanie wieloscenowych prototypów z narracją TTS, napisami, muzyką i opcjonalnym cyfrowym prezenterem. Deklarowana architektura jest self-hosted/offline-first, z Web UI i Dockerem. Projekt rozróżnia prezentera od deepfake.

## Ryzyka
realna zgodność deklaracji „offline” z kodem; modele i pobierane artefakty; dane głosowe/wideo; GPU; bezpieczeństwo uploadów; avatar/lip-sync i zgoda na wizerunek.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować rzeczywisty pipeline i zależności.
2. Zweryfikować brak niejawnych połączeń sieciowych.
3. Izolować uploady i generację.
4. Dodać provenance modeli oraz politykę zgody dla avatara.
5. Testy Docker/smoke generation i polonizacja UI.

## Kryterium zakończenia
Zweryfikowana prywatność self-hosted, reprodukowalny kontener i testy generacji.