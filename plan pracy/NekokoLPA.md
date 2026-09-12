# Audyt 168 — NekokoLPA

## Status
AUDYT ZAKOŃCZONY — aplikacja LPA/eSIM Android/iOS z obsługą czytników kart.

## Ustalenia
README opisuje OMAPI, USB CCID, CryptoTokenKit, React Native/Yarn, Mac Catalyst, Redux, WASM/native modules oraz warianty aplikacji. NekokoLPA 2 rozszerza zakres o Telephony API i platformy desktopowe, ale zapowiadana otwartość kodu jest przyszła.

## Ryzyka
Uprawnienia smartcard/USB, eSIM profile data, native bridges/WASM, różnice Android/iOS/Catalyst, build variants i prywatność danych operatora.

## Priorytet
WYSOKI.

## Kolejność prac
Native boundaries → entitlements → profile handling → device matrix → reproducible builds → tests → polonizacja.

## Kryterium zakończenia
Obsługa profili i czytników jest izolowana, testowalna i zgodna z uprawnieniami każdej platformy.
