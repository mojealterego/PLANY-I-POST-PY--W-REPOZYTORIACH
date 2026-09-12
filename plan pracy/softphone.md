# Audyt 84 — softphone

## Stan
AUDYT ZAKOŃCZONY — eksperymentalny web softphone SIP/RTP.

## Ustalenia
README opisuje PHP 8.1+ + Swoole, SIP UDP 4000, WSS/HTTPS, RTP↔PCM bridge, DTMF, wiadomości SIP i storage wiadomości. Główne punkty to `server.php`, `audio.php`, `trunkController` i `CallMediaBridge`. Repo używa zewnętrznych submodułów `libspech` oraz komponentu pcg729. Dokumentacja wskazuje aktywną gałąź inbound i brak pełnego production hardening.

## Ryzyka
- SIP/RTP/WSS to krytyczna powierzchnia sieciowa;
- auth, replay/dedup i state machine SIP;
- storage `messages.json` i sekrety vault;
- NAT, codec negotiation i niezawodność UDP;
- supply chain statycznego PHP/G729.

## Priorytet
KRYTYCZNY.

## Kolejność prac
SIP state machine → auth/session binding → TLS/WSS → RTP validation → secret vault → persistent store → concurrency/load tests → release.

## Kryterium zakończenia
Połączenia i media przechodzą deterministyczne testy, nieautoryzowane sesje są odrzucane, a transport i sekrety są zweryfikowane end-to-end.