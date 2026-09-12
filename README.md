# ARCH-ENG-CORE-999 — Centralny rejestr audytu repozytoriów

**Data rozpoczęcia:** 2026-09-11  
**Zakres:** wszystkie repozytoria właściciela `mojealterego` wykryte przez połączone konto GitHub  
**Liczba repozytoriów wykryta w aktualnej inwentaryzacji:** **376**  
**Repozytorium monitorujące:** `mojealterego/PLANY-I-POST-PY--W-REPOZYTORIACH`

## Zasada procesu

Każde repozytorium przechodzi osobny audyt. Dla każdego powstaje osobny plik w `plan pracy/` zawierający stan, ustalenia audytowe, ryzyka, priorytety oraz kolejność prac. Audyt nie jest utożsamiany z refaktoryzacją: najpierw ustalamy stan faktyczny, następnie wykonujemy modernizację.

## Stan globalny

| Zakres | Stan |
|---|---|
| Inwentaryzacja portfela | ZAKTUALIZOWANA — **376 repozytoriów** |
| Audyt szczegółowy | W TOKU — **341/376** |
| Plany pracy | UTWORZONE — **341/376** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnia tura — rekonsyliacja i nowe audyty

Ponownie sprawdzono aktualną inwentaryzację oraz katalog `plan pracy/`. Wśród 20 kolejnych kandydatów **16 posiadało już plany audytowe**, więc nie zostały ponownie doliczone. Cztery repozytoria nie miały planów i otrzymały nowe, zweryfikowane plany:

| Nr | Repozytorium | Wynik audytu | Priorytet |
|---:|---|---|---|
| 338 | local-llms-on-android | Android on-device LLM; ONNX/LiteRT, Qwen/Gemma, obraz, OCR, kamera i lokalne dane | KRYTYCZNY |
| 339 | PhoneClaw | iOS local AI agent; Gemma/MiniCPM-V, Skills, dane systemowe i opcjonalny Mac Gateway | KRYTYCZNY |
| 340 | Omni-mobile | Android Compose; WebSocket do runtime AI, obecnie domyślny endpoint developerski `ws://10.0.2.2:8000/ws` | WYSOKI |
| 341 | aider | Agent pair-programming; lokalne/chmurowe LLM, mapowanie codebase i Git | WYSOKI/REFERENCYJNY |

## Ważna korekta procesu

W tej turze celowo **nie wymuszono sztucznego zwiększenia licznika o 20**. Próby utworzenia planów dla kolejnych kandydatów zwracały konflikt istniejącego pliku (`sha wasn't supplied`), co potwierdziło, że te repozytoria były już objęte katalogiem `plan pracy/`. Dzięki temu centralny licznik nie podwaja audytów.

Dla nowych pozycji sprawdzono rzeczywistą zawartość README. `local-llms-on-android` potwierdza lokalne modele Qwen/Gemma przez ONNX/LiteRT, multimodalne wejście i brak telemetryki; `PhoneClaw` potwierdza lokalnego agenta iOS z natywnymi Skills oraz kontrolowanymi operacjami; `Omni-mobile` ma jawnie developerski WebSocket `ws://10.0.2.2:8000/ws`; `aider` jest terminalowym agentem pair-programming z integracją Git. fileciteturn799file0 fileciteturn800file0 fileciteturn801file0 fileciteturn802file0

## Poprzednie audyty

Audyty 1–337 pozostają zapisane w tym rejestrze oraz w odpowiednich plikach `plan pracy/`. Numery 338–341 odpowiadają czterem nowym, unikalnym planom zapisanym w tej turze. Licznik ma być zwiększany wyłącznie o nowe, unikalne repozytoria.

## Postęp

**341 / 376 repozytoriów — 90,69% audytu szczegółowego.**  
**35 repozytoriów pozostaje do jednoznacznego rozliczenia/audytu.**

## Aktualizacja inwentaryzacji

Portfel wynosi obecnie **376 repozytoriów**. Licznik jest dynamiczny i będzie ponownie weryfikowany przy każdym kolejnym przebiegu. Nowe repozytoria nie są automatycznie uznawane za zbadane; muszą przejść rzeczywisty audyt zawartości i otrzymać własny plan.

## Reguła kolejnych audytów

Kolejny wpis może otrzymać status **AUDYT ZAKOŃCZONY** dopiero po przeanalizowaniu rzeczywistej zawartości repozytorium, a nie tylko jego nazwy i metadanych. W przypadku repozytoriów dużych analiza obejmuje co najmniej README, strukturę katalogów, manifesty zależności, konfigurację budowania, CI/CD, testy oraz główne punkty wejścia. W projektach archiwalnych i dokumentacyjnych oceniana jest również aktualność, pochodzenie danych oraz przydatność referencyjna.

## Klasy priorytetów

- **KRYTYCZNY** — puste repozytorium, projekt bazowy dla innych prac, duże ryzyko architektoniczne/bezpieczeństwa albo bezpośrednia wartość strategiczna.
- **WYSOKI** — aktywny projekt wymagający uporządkowania, polonizacji, zabezpieczenia lub modernizacji.
- **ŚREDNI** — projekt użyteczny, lecz bez natychmiastowej blokady ekosystemu.
- **NISKI** — materiały referencyjne, archiwa, katalogi lub projekty o ograniczonym zakresie wykonawczym.

## Zasada produkcyjna

Żaden projekt nie zostanie uznany za zakończony po samym audycie. Po audycie następuje implementacja zgodnie z planem, kompilacja/testy i dopiero wtedy zmiana statusu na produkcyjny.
