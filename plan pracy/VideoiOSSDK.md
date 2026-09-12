# VideoiOSSDK

## Status
AUDYT ZAKOŃCZONY — starszy SDK iOS do wideokomunikacji.

## Stan faktyczny
README opisuje Kaleyra Video SDK dla iOS: audio/wideo, czat, udostępnianie ekranu, nagrywanie, pliki, PIP i funkcje administracyjne. Obsługiwane są SPM i CocoaPods; minimalna platforma w przykładzie to iOS 15.

## Ryzyka
Projekt wymaga weryfikacji aktualności API, zależności WebRTC/Socket.IO/Starscream oraz zgodności z aktualnymi wersjami iOS/Xcode. Funkcje nagrywania i zdalnego sterowania wymagają przeglądu prywatności i uprawnień.

## Priorytet
WYSOKI.

## Kolejność prac
1. Ustalić aktualny stan branchy/release.
2. Zweryfikować build SPM/CocoaPods i sample.
3. Audyt sieci, kryptografii, storage i uprawnień.
4. Aktualizacja dokumentacji i polonizacja.
5. Testy na wspieranych wersjach iOS.

## Kryterium zakończenia
Odtwarzalny build, aktualne zależności i dokumentacja, testy funkcji komunikacyjnych oraz jawne wymagania prywatności.