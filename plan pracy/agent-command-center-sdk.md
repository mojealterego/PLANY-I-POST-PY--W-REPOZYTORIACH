# Plan pracy — agent-command-center-sdk

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: SDK Python + TypeScript dla bramy Agent Command Center
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIE POTWIERDZONO

## Ustalenia
Repozytorium zawiera dwa główne SDK oraz integracje TypeScript z LangChain, LlamaIndex, React i Vercel AI SDK. README deklaruje zgodność z OpenAI-compatible API, routing, guardrails, caching, streaming, tool calling i structured output. Manifest TypeScript publikuje ESM/CJS, deklaracje typów, build, test, lint i typecheck; Node >=18.0.0. README odwołuje się jednak do zewnętrznego gatewaya Future AGI, więc przed wykorzystaniem jako własnej warstwy należy rozdzielić kod SDK od zależności usługowej i zweryfikować kontrakt API.

## Ryzyka
1. Silna zależność dokumentacji od zewnętrznej platformy/gatewaya.
2. Należy zweryfikować rzeczywistą kompatybilność deklarowanego OpenAI API, szczególnie Responses, audio, files, batches i multimodalności.
3. Wymagana kontrola sekretów, endpointów, timeoutów, retry i obsługi błędów.
4. Konieczne testy kontraktowe niezależne od zewnętrznej usługi.
5. Pełna polonizacja dokumentacji i wydzielenie własnych adapterów dopiero po potwierdzeniu licencji oraz pochodzenia kodu.

## Kolejność prac
1. Zmapować SDK Python/TypeScript i wszystkie integracje.
2. Zbudować macierz zgodności endpointów OpenAI-compatible.
3. Dodać testy kontraktowe z lokalnym/mockowanym gatewayem.
4. Zweryfikować streaming, tool calling, structured output, błędy i retry.
5. Sprawdzić publikację npm/PyPI, wersjonowanie i reproducibility.
6. Zweryfikować security boundary dla kluczy i custom base URL.
7. Dopiero potem rebranding, pełna polonizacja i integracja z ekosystemem.

## Kryterium zakończenia
Build, typecheck, testy jednostkowe i kontraktowe oraz publikacyjne smoke-testy przechodzą bez zależności od produkcyjnego gatewaya.
