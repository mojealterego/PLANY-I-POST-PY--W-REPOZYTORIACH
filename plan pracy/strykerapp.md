# Plan pracy — strykerapp

## Stan audytu
**AUDYT ZAKOŃCZONY — Android security/pentest suite; bardzo wysoki poziom ryzyka operacyjnego.**

## Ustalenia
README opisuje StrykerOSS 6.x jako rootowaną aplikację Android z Debian chroot, terminalem, Nmap, Nuclei, Metasploit, Hydra, HID/USB gadgetami, Wi-Fi attack tooling oraz modułem BLE WhisperPair. `app/build.gradle` potwierdza arm64-v8a, minSdk 24, targetSdk 28, compileSdk 33, ndk-build, R8 release i opcjonalne podpisywanie z sekretów Gradle/env.

## Ryzyka i braki
- krytyczne: root, chroot i wykonywanie poleceń jako uprzywilejowany proces;
- krytyczne: moduły Wi-Fi deauthentication, WPS, handshake capture, exploit dispatch i Metasploit mogą mieć bezpośrednie skutki poza urządzeniem;
- krytyczne: USB HID/gadget i RNDIS/ECM/ACM mają potencjał oddziaływania na podłączone hosty;
- krytyczne: BLE exploit chain wymaga niezależnej walidacji zakresu i bezpiecznego trybu testowego;
- targetSdk 28 jest znacząco niższy od compileSdk i powinien zostać potraktowany jako główny problem modernizacji;
- lint ma `abortOnError false` i `checkReleaseBuilds false`, więc sam release build nie jest dowodem jakości;
- zależności są częściowo stare względem obecnego ekosystemu Android;
- chroot/core jest pobierany i rozpakowywany — wymagane są integralność, provenance i weryfikacja artefaktów;
- wymagane są ścisłe granice między trybem edukacyjnym/laboratoryjnym a funkcjami oddziałującymi na sieci/urządzenia zewnętrzne.

## Priorytet
**KRYTYCZNY**

## Kolejność prac
1. Zmapować wszystkie ścieżki root/su/chroot/process execution.
2. Wprowadzić formalny model trybu laboratoryjnego i ochrony przed przypadkowym działaniem poza zakresem.
3. Zweryfikować integralność pobieranego rootfs i komponentów.
4. Zmapować permissions, USB/BLE/Wi-Fi i lifecycle procesu.
5. Dodać testy jednostkowe parserów i managerów oraz testy instrumentacyjne na emulatorze/urządzeniu laboratoryjnym.
6. Zmodernizować SDK/build i włączyć fail-closed lint/quality gates.
7. Przeprowadzić audyt licencji i THIRD-PARTY-NOTICES.
8. Rebranding/polonizacja dopiero po ustabilizowaniu bezpieczeństwa i buildów.

## Kryterium zakończenia
Powtarzalny build, zweryfikowane artefakty, kontrolowane wykonanie uprzywilejowane, testy urządzeniowe oraz jednoznaczne ograniczenie zastosowania do autoryzowanych laboratoriów. Audyt nie oznacza produkcji.
