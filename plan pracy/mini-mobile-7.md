# Plan pracy — mini-mobile-7

## Status audytu

**AUDYT ZAKOŃCZONY — 2026-09-12**

Repozytorium: `mojealterego/mini-mobile-7`  
Gałąź domyślna: `main`  
Język wykryty: Shell / konfiguracja infrastruktury  
Charakter: laboratorium prywatnej sieci LTE/5G dla maksymalnie 7 kontrolowanych urządzeń.

## Zakres rzeczywiście sprawdzony

Przeanalizowano:
- `README.md`
- strukturę katalogu głównego
- `.env.example`
- `.gitignore`
- `Makefile`
- `SECURITY.md`
- `scripts/validate-host.sh`
- `scripts/build-ueransim.sh`
- `core/open5gs/README.md`
- `core/open5gs/config/5gc-lab.yaml.example`
- katalogi `core/`, `ran/`, `ims/`, `network/`, `subscribers/`, `monitoring/`, `docs/`, `scripts/`
- metadane repozytorium i gałąź domyślną.

## Stan techniczny

Repozytorium jest przede wszystkim szkieletem wdrożeniowym i dokumentacyjnym, a nie kompletną, gotową siecią komórkową. Architektura deklaruje Open5GS + MongoDB, UERANSIM dla laboratorium bez RF, Kamailio IMS oraz srsRAN lub kompatybilny RAN dla testów fizycznych. Adresacja jest rozdzielona na segmenty Core `10.10.0.0/24`, UE `10.20.0.0/24`, Management `10.30.0.0/24` i IMS `10.40.0.0/24`.

`Makefile` udostępnia walidację hosta, bootstrap Ubuntu 22 oraz budowanie UERANSIM. Walidator sprawdza m.in. `ip`, `systemctl`, `curl`, `gpg`, `iptables`, usługę MongoDB, obecność Open5GS, interfejs `ogstun` i przekazywanie IPv4. Skrypt budowania UERANSIM przypina wersję `v3.3.0` i buduje ją lokalnie po instalacji zależności.

Konfiguracja środowiskowa jest przygotowana jako przykład bez sekretów. Open5GS jest przypięty do `v2.8.0`, a konfiguracja 5GC jest jawnie oznaczona jako referencyjna, a nie jako bezpośredni zamiennik plików `/etc/open5gs/*.yaml`.

## Mocne strony

1. Jasny podział na Core, RAN, IMS, sieć, subskrybentów i monitoring.
2. Jawna zasada laboratorium bez RF przed przejściem do infrastruktury fizycznej.
3. Dobra separacja sekretów od repozytorium.
4. Wydzielony segment administracyjny i zalecenie administracji przez VPN.
5. Przypinanie wersji Open5GS i UERANSIM zamiast ślepego używania `latest`.
6. README zawiera ograniczenia techniczne i prawne oraz nie udaje wdrożenia produkcyjnego.
7. `SECURITY.md` ustanawia podstawowe zasady ochrony poświadczeń i izolacji sieci.

## Ryzyka i braki

### KRYTYCZNE
- Nie ma jeszcze dowodu, że cały stos został uruchomiony end-to-end w środowisku laboratoryjnym.
- Brak widocznych testów automatycznych dla konfiguracji 5GC/EPC, routingu, subscriber provisioning i IMS.
- Brak potwierdzonego CI/CD w przeanalizowanym zakresie.
- Konfiguracja Open5GS pozostaje szkieletem opisowym; wymaga walidacji z faktycznymi szablonami konkretnej wersji.

### WYSOKIE
- `validate-host.sh` raportuje część braków jako `WARN`, więc sam sukces skryptu nie oznacza gotowości całej infrastruktury.
- Skrypt `build-ueransim.sh` używa `sudo apt` i zewnętrznego repozytorium; należy dodać kontrolę integralności źródeł i powtarzalność środowiska.
- Brak formalnego kontraktu wersji dla całego stosu: Open5GS, MongoDB, UERANSIM, Kamailio i RAN.
- Brak jawnego testu, który gwarantuje zgodność adresacji, PLMN, TAC, SST i DNN pomiędzy komponentami.
- Brak procedury automatycznego backupu i odtwarzania danych MongoDB.

### ŚREDNIE
- Brak licencji repozytorium.
- Brak jawnego modelu obserwowalności i kryteriów alarmowania mimo obecności katalogu `monitoring/`.
- Dokumentacja wymaga dalszego rozdzielenia procedur laboratoryjnych od przyszłych procedur fizycznego RAN.

## Plan implementacyjny

### Etap 1 — inwentaryzacja i kontrakty
- ustalić macierz wersji wszystkich komponentów;
- zdefiniować jeden kanoniczny model parametrów sieci;
- walidować spójność CIDR, PLMN, TAC, SST, DNN i interfejsów;
- określić wymagania hosta Linux i wspierane wersje Ubuntu.

### Etap 2 — laboratorium UERANSIM
- przygotować powtarzalne środowisko;
- uruchomić minimalny Open5GS + MongoDB;
- dodać jednego syntetycznego subskrybenta;
- zweryfikować rejestrację i PDU session;
- zweryfikować NAT i łączność UE;
- zapisać logi oraz wyniki testów jako artefakty.

### Etap 3 — siedmiu subskrybentów
- wprowadzić bezpieczny model provisioning;
- nie przechowywać Ki/OPc/SQN w Git;
- dodać testy izolacji i poprawności identyfikatorów;
- zweryfikować równoległe sesje dla siedmiu kontrolowanych urządzeń w laboratorium.

### Etap 4 — IMS i usługi dodatkowe
- uruchomić Kamailio za segmentacją i uwierzytelnionym dostępem;
- przetestować SIP/IMS wyłącznie w kontrolowanym środowisku;
- dodać testy regresji konfiguracji.

### Etap 5 — bezpieczeństwo operacyjne
- wdrożyć VPN-only management;
- zablokować ekspozycję MongoDB i interfejsów administracyjnych;
- dodać skanowanie sekretów i walidację `.gitignore`;
- przygotować backup/restore;
- dodać audyt zmian konfiguracji i retencję logów.

### Etap 6 — fizyczny RAN
- traktować jako osobny etap dopiero po spełnieniu wymagań prawnych, sprzętowych i bezpieczeństwa;
- nie uznawać konfiguracji programowej za dowód prawa do transmisji;
- dokumentować sprzęt, USIM, lokalizację, moc, anteny i wymagane uprawnienia przed aktywacją RF.

## Polonizacja i rebranding

- utrzymać komentarze i dokumentację operacyjną po polsku;
- ujednolicić nazewnictwo parametrów i procedur;
- dodać polski przewodnik uruchomienia laboratorium;
- rozdzielić dokumentację techniczną, bezpieczeństwa i wymagań prawnych;
- zachować nazwy techniczne upstreamów tam, gdzie są nazwami własnymi komponentów.

## Kryterium zakończenia

Repozytorium może przejść z etapu planowania do implementacji dopiero po uzyskaniu powtarzalnego testu laboratoryjnego end-to-end, automatycznej walidacji konfiguracji, kontroli sekretów, procedury backup/restore i kompletnej dokumentacji. Nie wolno oznaczać projektu jako produkcyjnego na podstawie samego audytu.
