# gpt_mobile — plan pracy

## Status
AUDYT ZAKOŃCZONY — aplikacja mobilna.

## Stan faktyczny
Repozytorium ok. 10 MB z kodem mobilnym związanym z GPT. Dokładny framework, API i model przechowywania danych wymagają potwierdzenia w manifestach i entrypointach.

## Ryzyka
- klucze API w aplikacji mobilnej;
- WebView/network security;
- przechowywanie historii rozmów;
- zależności mobilne i zgodność SDK.

## Priorytet
WYSOKI

## Kolejność prac
1. Audyt manifestów i dependency graph.
2. Usunąć wszelkie sekrety klienta.
3. Zweryfikować storage/network i błędy.
4. Testy emulator/device.
5. Polonizacja/rebranding.

## Kryterium zakończenia
Bezpieczny model konfiguracji API, testowany build i kontrolowane przechowywanie danych.
