# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **293**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKOŃCZONA — **293 repozytoria** |
| Audyt szczegółowy | W TOKU — **51/293** |
| Plany pracy | UTWORZONE — **51/293** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnio wykonane audyty

| Nr | Repozytorium | Wynik audytu | Priorytet | Plan pracy |
|---:|---|---|---|---|
| 44 | JARVIS-2.0 | Android/Expo + Node backend; foundation działa, ale backend ma jeszcze plikowy stan, auth fail-open przy braku tokenu i CORS `*` | KRYTYCZNY | `plan pracy/JARVIS-2.0.md` |
| 45 | omega-x-neuromesh | Verification-first control plane dla Unreal; mocny default-deny prototyp, ale UE 5.8/MCP runtime nadal nieweryfikowane | KRYTYCZNY | `plan pracy/omega-x-neuromesh.md` |
| 46 | hermes-mobile | Dojrzały klient Android dla Hermes Agent; silne testy i szyfrowanie, ale release dopuszcza cleartext i wymaga pełnej weryfikacji transportu | WYSOKI | `plan pracy/hermes-mobile.md` |
| 47 | ESIM2 | Historyczna implementacja ESIM dla NLI/PyTorch; wartość referencyjna wysoka, lecz packaging i środowisko wymagają modernizacji | ŚREDNI | `plan pracy/ESIM2.md` |
| 48 | Text2Image-Generation | Projekt text-to-image bez dostępnego README; nieprzypięte zależności i szeroki stos ML/web | WYSOKI | `plan pracy/Text2Image-Generation.md` |
| 49 | artemis | Zaawansowana automatyzacja realnych urządzeń Android przez AI/MCP; silne testowanie, ale wymagane niezależne potwierdzenie benchmarków i security boundary | KRYTYCZNY | `plan pracy/artemis.md` |
| 50 | Kartografia | React/Vite/PWA + Capacitor Android; rozbudowany fundament gry, ale zależności `latest` osłabiają reprodukowalność | WYSOKI | `plan pracy/Kartografia.md` |
| 51 | MetaGPT | Duży framework wieloagentowy; wysoka wartość referencyjna, konieczna weryfikacja kompatybilności, granic narzędzi i aktualności dokumentacji | KRYTYCZNY | `plan pracy/MetaGPT.md` |

## Poprzednie audyty

Audyty 1–43 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Pozycje 44–51 są opisane powyżej.

## Postęp

**51 / 293 repozytoriów — 17,41% audytu szczegółowego.**  
**242 repozytoria pozostają do audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **293 repozytoria**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
