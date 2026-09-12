# Plan pracy — hermes-mobile

## Status audytu
- Klasyfikacja: dojrzała aplikacja Android/Jetpack Compose będąca klientem dla Hermes Agent.
- Audyt: wykonany na podstawie README, konfiguracji Gradle i katalogu technologicznego.
- Produkcja: NIE — wymaga niezależnej weryfikacji bezpieczeństwa, transportu i procesu release.

## Ustalenia
- Aplikacja używa Kotlin 2.4.10, Jetpack Compose, Material 3, Navigation 3, Retrofit/OkHttp, Room 3 + SQLCipher, DataStore i szyfrowanego magazynu.
- Projekt ma testy JUnit/MockK/Turbine/Espresso/Compose oraz własne guardy jakości, w tym kontrolę hardcoded colors.
- `release` ma minifikację i shrink resources, ale konfiguracja jawnie dopuszcza `usesCleartextTraffic=true`; README również opisuje komunikację HTTP jako przeznaczoną dla zaufanych sieci lokalnych.
- README zawiera instrukcję LAN z przykładowymi domyślnymi danymi `admin/hermes`; należy traktować to jako ryzyko dokumentacyjne i wymusić własne silne dane.
- Repo jest forkowanym/kopiowanym projektem powiązanym z zewnętrznym upstreamem; przed rebrandingiem trzeba rozdzielić upstream od własnych zmian i ustalić provenance/licencję.

## Priorytety
1. Zmapować model zaufania LAN, endpointy gatewaya, WebSocket i mechanizmy sesji.
2. W release wyłączyć cleartext albo dopuścić je wyłącznie przez jawny allowlist lokalnych adresów z kontrolą środowiska.
3. Zweryfikować bezpieczne przechowywanie tokenów, haseł, profili połączeń i kluczy szyfrujących.
4. Sprawdzić logowanie OkHttp i wykluczyć wyciek Authorization/cookies do logów produkcyjnych.
5. Zweryfikować WebSocket ticket/session lifecycle, timeouty, reconnect i walidację certyfikatów, jeśli HTTPS/WSS jest używany.
6. Uruchomić pełny zestaw `check`, testy jednostkowe i instrumentacyjne oraz release build w czystym środowisku.
7. Zweryfikować deterministyczność artefaktów i podpisywania; usunąć dummy keystore z realnej ścieżki release.
8. Przejrzeć zależności i zgodność licencji po zmianach upstreamu.
9. Dopiero potem wykonać pełną polonizację/rebranding.

## Kryterium zakończenia
Kolejny etap wymaga przechodzącego release builda, potwierdzonego modelu bezpieczeństwa połączenia z gatewayem, testów auth/WS/Room oraz zweryfikowanego procesu podpisywania i dystrybucji.
