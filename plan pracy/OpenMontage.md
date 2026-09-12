# Audyt: OpenMontage

## Status
AUDYT ZAKOŃCZONY — agentic system produkcji wideo.

## Stan faktyczny
README opisuje pipeline od researchu i scenariusza przez generowanie assetów, montaż, narrację i render. Obecne elementy obejmują Backlot, approval gates, registry providerów, Remotion, FFmpeg, Blender i wiele dostawców modeli. Instalacja wymaga Python 3.10+, Node 18+ i FFmpeg. Licencja AGPLv3.

## Ryzyka
Koszty wielu providerów, generowanie treści, pobieranie materiałów z sieci, provenance/licencje assetów, wykonywanie pipeline'u przez agenta i lokalne pliki.

## Priorytet
KRYTYCZNY/WYSOKI.

## Kolejność prac
1. audyt tool registry i granic wykonania;
2. approval gates i koszt budget;
3. provenance assetów i licencje;
4. sandbox dla FFmpeg/Blender/Remotion;
5. testy reprodukowalności renderów;
6. polonizacja/rebranding.

## Kryterium zakończenia
Każda operacja kosztowna lub destrukcyjna ma jawne uprawnienie, limit i log; pipeline przechodzi testy end-to-end.
