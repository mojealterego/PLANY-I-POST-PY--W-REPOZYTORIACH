# Audyt 161 — gonnect

## Status
AUDYT ZAKOŃCZONY — desktopowy klient UC/VoIP Qt/C++ dla Linux/Flatpak i Windows.

## Ustalenia
README opisuje SIP, przekierowania, konferencje do trzech osób, RTT, LDAP/CardDAV/CSV/Microsoft 365, Jitsi, chat, kalendarze, zestawy słuchawkowe, busylights, Flatpak oraz CMake/Conan. Projekt jest konfigurowany plikiem zamiast kreatora.

## Ryzyka
SIP/RTP i urządzenia audio, prywatność rozmów, konfiguracja Flatpak, uprawnienia sprzętowe, integracje kontaktów/kalendarzy oraz kompatybilność Windows/Linux.

## Priorytet
WYSOKI.

## Kolejność prac
Build matrix → bezpieczeństwo konfiguracji → audio/SIP → integracje → Flatpak sandbox → testy urządzeń → polonizacja.

## Kryterium zakończenia
Powtarzalny build, testy protokołów i integracji, ograniczone uprawnienia oraz udokumentowana konfiguracja.
