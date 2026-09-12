# Plan pracy — simplex-chat

## Stan audytu
**AUDYT ZAKOŃCZONY — bardzo duży projekt komunikatora; wartość strategiczna i bezpieczeństwa bardzo wysoka.**

## Ustalenia
README opisuje wieloplatformowy komunikator SimpleX z szyfrowaniem end-to-end, aplikacjami Android/iOS, CLI oraz rozbudowaną dokumentacją i tłumaczeniami. `cabal.project` pokazuje stos Haskell oraz kilka zależności pobieranych jako przypięte repozytoria Git. W repozytorium istnieją testy i CI upstreamu, ale ich pełna aktualność względem lokalnego forka wymaga osobnej weryfikacji.

## Ryzyka i braki
- bardzo duża powierzchnia kryptograficzna i wieloplatformowa;
- należy zweryfikować aktualność zależności kryptograficznych oraz reprodukowalność buildów;
- `cabal.project` zawiera historyczny `index-state` oraz wiele własnych forków zależności — wymaga audytu provenance i aktualności;
- konieczna jest analiza granic FFI/native/mobile oraz storage lokalnego;
- należy rozdzielić kod upstream od własnych modyfikacji `mojealterego` przed rebrandingiem;
- polonizacja powinna wykorzystać istniejącą strukturę tłumaczeń zamiast naruszać upstreamowy mechanizm lokalizacji;
- wymagane są testy regresyjne protokołów, synchronizacji, storage i kryptografii przed jakąkolwiek modernizacją funkcjonalną.

## Priorytet
**KRYTYCZNY**

## Kolejność prac
1. Ustalić dokładny fork/base commit i zakres własnych zmian.
2. Zmapować aplikacje, bibliotekę Haskell, komponenty native i zależności Git.
3. Przeprowadzić audyt kryptograficzny/protokółowy bez modyfikowania prymitywów bez dowodu poprawności.
4. Zweryfikować buildy Android/iOS/CLI oraz toolchainy.
5. Zbudować testy regresyjne i reprodukowalność.
6. Zbadać lokalne dane, backupy, migracje i synchronizację.
7. Dopiero potem rebranding i polonizacja własnych warstw.

## Kryterium zakończenia
Zweryfikowana genealogia kodu, powtarzalne buildy, przechodzące testy krytycznych ścieżek oraz brak regresji bezpieczeństwa. Nie uznawać za projekt produkcyjny wyłącznie na podstawie audytu.
