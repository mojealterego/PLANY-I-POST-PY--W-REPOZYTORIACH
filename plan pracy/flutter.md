# Plan pracy — flutter

## Status
AUDYT ZAKOŃCZONY — duże repozytorium frameworka Flutter; referencja upstream.

## Stan faktyczny
Projekt ma bardzo duży rozmiar i branch `master`. Ze względu na charakter frameworka należy traktować go jako zależność referencyjną, nie kandydat do mechanicznej polonizacji kodu.

## Ryzyka
- ogromny toolchain Dart/Flutter;
- kompatybilność platform;
- supply chain i release artifacts;
- czasochłonne testy wieloplatformowe.

## Priorytet
WYSOKI — REFERENCJA.

## Kolejność prac
1. Identyfikacja używanych komponentów.
2. Pinowanie wersji w projektach zależnych.
3. Weryfikacja buildów tylko tam, gdzie framework jest używany.
4. Dokumentacja referencyjna.

## Kryterium zakończenia
Udokumentowana wersja źródłowa i kompatybilność zależnych projektów.
