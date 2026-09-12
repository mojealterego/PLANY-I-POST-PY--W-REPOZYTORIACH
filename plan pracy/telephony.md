# Plan pracy — telephony

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: platforma telekomunikacyjna oparta o VoxImplant
- Priorytet: WYSOKI
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
Projekt implementuje firmową platformę obsługi połączeń: strefy, książkę adresową, harmonogramy, przekierowania, konferencje i voicemail. README opisuje JavaScript, konfigurację JSON/ERB, Ruby/Bundler oraz CI/CD z CircleCI. System operuje na danych osobowych i numerach telefonów oraz zewnętrznych kluczach VoxImplant/Mandrill.

## Ryzyka
1. Dane numerów telefonicznych i adresów e-mail wymagają kontroli dostępu oraz retencji.
2. Klucze API usług telekomunikacyjnych i pocztowych muszą być wyłącznie sekretami środowiskowymi.
3. Deployment konfiguracji bezpośrednio z CI wymaga walidacji, review i ochrony gałęzi.
4. Logika routingu połączeń wymaga testów stref, stref czasowych, awarii i fallbacków.
5. Należy zweryfikować aktualność zależności Ruby/JS i usług zewnętrznych.

## Kolejność prac
1. Zmapować konfigurację, taski deploymentu i skrypty CI.
2. Wprowadzić schematy JSON/ERB oraz walidację przed wdrożeniem.
3. Dodać testy routingu, harmonogramów i stref czasowych.
4. Wymusić bezpieczne zarządzanie sekretami i minimalne uprawnienia.
5. Dodać kontrolę zmian konfiguracji i audyt deploymentów.
6. Zweryfikować dostawców, retencję nagrań i wymagania prywatności.
7. Następnie polonizacja/rebranding własnych elementów.

## Kryterium zakończenia
Walidowane konfiguracje, bezpieczny CI/CD, testy routingu i fallbacków, kontrola sekretów/danych oraz zweryfikowany deployment.
