# OmniMAS Advanced — plan pracy

## Status
AUDYT ZAKOŃCZONY — baza architektoniczna, nie produkcja.

## Stan faktyczny
Androidowy agent automatyzacji oparty o lokalny Ollama LLM i AccessibilityService. Architektura rozdziela Planner, Grounding, Decision Agent, Executor, Memory, Security Gate i Supervisor. README wskazuje akcje CLICK/TYPE/SCROLL/BACK/HOME/DONE oraz potwierdzenie dla operacji wysokiego ryzyka. CI buduje debug APK.

## Ryzyka
- AccessibilityService może oddziaływać na inne aplikacje;
- endpoint Ollama i transport zdalny wymagają twardego uwierzytelniania/TLS;
- trwała pamięć, timeouty i kolejka misji są jeszcze elementami backlogu;
- brak potwierdzenia testów instrumentacyjnych.

## Priorytet
KRYTYCZNY

## Kolejność prac
1. Audyt modułów Gradle, manifestu, uprawnień i workflow.
2. Zabezpieczenie granicy LLM → decyzja → wykonanie.
3. Testy deterministyczne i instrumentacyjne na emulatorze.
4. Timeouty, retry, anulowanie misji i trwała pamięć.
5. Polonizacja/rebranding dopiero po stabilizacji.

## Kryterium zakończenia
Brak nieautoryzowanych akcji, pełne testy UI/agent loop, bezpieczny transport LLM i reproducible build.
