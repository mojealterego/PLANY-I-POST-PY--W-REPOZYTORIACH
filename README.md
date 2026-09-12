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
| Audyt szczegółowy | W TOKU — **353/376** |
| Plany pracy | UTWORZONE — **353/376** |
| Refaktoryzacja | OCZEKUJE NA AUDYT DANEGO REPOZYTORIUM |
| Rebranding | OCZEKUJE |
| Pełna polonizacja | OCZEKUJE |
| Projekty z bazy wiedzy | OCZEKUJĄ NA ZAKOŃCZENIE ETAPU ISTNIEJĄCEGO PORTFELA |

## Ostatnia tura — 20 repozytoriów zweryfikowanych

W tej turze przeanalizowano rzeczywistą zawartość **20 repozytoriów**: README, a tam gdzie było to istotne również manifest/dependency file lub główny punkt wejścia. Następnie sprawdzono istnienie planu w centralnym repozytorium przed utworzeniem nowego.

Nowe, unikalne plany utworzone w tej turze:

| Nr | Repozytorium | Wynik audytu | Priorytet |
|---:|---|---|---|
| 342 | Temp-SMS-Receive | Python CLI; zewnętrzne API SMS, autoryzacja, AES, automatyczne instalowanie zależności i aktualizacje Git | KRYTYCZNY |
| 343 | Uncensored-Local-Studio | Tauri/React; lokalne Stable Diffusion, LLM, Whisper, Kokoro, pobieranie modeli i subprocessy | KRYTYCZNY |
| 344 | Rivo-Agent-Application | React Native Android; `llama.rn`, GGUF, Firebase Auth, AsyncStorage, downloader, moduły Kotlin | KRYTYCZNY |
| 345 | sanna | Governance agentów; konstytucje YAML, Ed25519, receipts, gateway/interceptor i policy enforcement | KRYTYCZNY |
| 346 | sim | Workspace agentów/workflow; Next.js/Bun/Postgres/Drizzle, Better Auth, jobs, webhooks, E2B/isolated-vm | KRYTYCZNY |
| 347 | FastGPT | Agent/RAG/workflow/MCP; wizualna orkiestracja, pluginy, knowledge base i API | KRYTYCZNY |
| 348 | dify | Platforma LLM/Agent/RAG/LLMOps; workflow, providerzy modeli, narzędzia, API i self-hosting | KRYTYCZNY |
| 349 | pageplug | Fork Appsmith; React + Java/Spring WebFlux + Taro, MongoDB/Redis, data-source proxy | KRYTYCZNY |
| 350 | claude-code-android | Android/Termux; trzy ścieżki instalacji, patchowane binarium, AVF VM, ADB i security model | KRYTYCZNY |
| 351 | construct-3-games | Monorepo historycznych gier Construct 3; wiele prototypów i jamów, asset provenance | ŚREDNI/REFERENCYJNY |
| 352 | saltcorn | No-code database builder; Node/Express/PostgreSQL, multi-tenant, dynamic plugins i CLI | KRYTYCZNY |
| 353 | MaxKB | Enterprise Agent/RAG; Vue/Django/LangChain/PostgreSQL+pgvector, MCP, workflow i multimodalność | KRYTYCZNY |

Repozytoria sprawdzone i już posiadające plan lub wymagające dalszej rekonsyliacji nie zostały ponownie doliczone. W tej grupie potwierdzono m.in. istniejące plany dla `plasmic`, `OpenHands` i `ShipinKit`.

## Dowody z audytu

`Temp-SMS-Receive` rzeczywiście zawiera Pythonowy CLI z `requests`, `pycryptodome`, `pyperclip` oraz funkcjami pobierania krajów, numerów i wiadomości; kod zawiera także stały klucz AES i mechanizm `git pull`. fileciteturn810file0 fileciteturn814file0

`Uncensored-Local-Studio` deklaruje lokalne image generation, LLM, Whisper i Kokoro na Windows/Linux/macOS; frontend używa Tauri 2, React 19 i Vite 8. fileciteturn812file0 fileciteturn815file0

`Rivo-Agent-Application` potwierdza React Native 0.85.3, `llama.rn`, Firebase Auth, AsyncStorage, downloader i natywne moduły Android; README wskazuje także konieczność zastąpienia debug signing przed produkcją. fileciteturn818file0 fileciteturn820file0

`MaxKB`, `FastGPT` i `Dify` potwierdzają duże platformy Agent/RAG/workflow, natomiast `sim` łączy workspace danych z agentami, harmonogramami i izolowanym wykonywaniem kodu. fileciteturn817file0 fileciteturn827file0 fileciteturn837file0 fileciteturn826file0

`claude-code-android` posiada osobny security model, SSRF guard, permission rules i testy claimów; Path A wykorzystuje patchowanie binarium Linux dla Termux. fileciteturn842file0

`GDevelop` oraz `construct-3-games` są projektami/game-development reference o zupełnie innym charakterze niż backendy agentowe: GDevelop jest pełnym no-code IDE/engine, a construct-3-games jest zbiorem historycznych gier i prototypów. fileciteturn841file0 fileciteturn843file0

## Postęp

**353 / 376 repozytoriów — 93,88% audytu szczegółowego.**  
**23 repozytoria pozostają do jednoznacznego rozliczenia/audytu.**

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
