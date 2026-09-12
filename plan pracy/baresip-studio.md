# Plan pracy — baresip-studio

## Status
AUDYT ZAKOŃCZONY — Android SIP/VoIP user agent.

## Stan faktyczny
README opisuje Android Studio projekt oparty na baresip/libbaresip, z SIP, głosem, wiadomościami, konferencjami, transferami, TLS/WSS oraz ZRTP/DTLS-SRTP. Wspierany Android 9+, funkcje calling/messaging od Android 10. Dostępne są źródła, biblioteki natywne i dystrybucja F-Droid/Play/GitHub.

## Ryzyka
SIP/RTP security; certyfikaty; native libraries/FFI; uprawnienia audio; aktualność Android API; podpis APK; prywatność kontaktów i treści rozmów.

## Priorytet
WYSOKI.

## Kolejność prac
1. Ustalić wersje Gradle/SDK/NDK i libbaresip.
2. Zweryfikować TLS/SRTP i walidację certyfikatów.
3. Audyt uprawnień i storage/logów.
4. Reproducible build oraz weryfikacja podpisów.
5. Polska lokalizacja i testy urządzeniowe.

## Kryterium zakończenia
Powtarzalny signed build, testy SIP/media i udokumentowane granice prywatności.