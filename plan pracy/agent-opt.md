# agent-opt — plan pracy

## Status
AUDYT ZAKOŃCZONY — SDK optymalizacji promptów.

## Stan faktyczny
Python SDK Future AGI z sześcioma strategiami: Random Search, Bayesian/Optuna, ProTeGi, Meta-Prompt, PromptWizard i GEPA. Integruje LiteLLM oraz ewaluację metrykami. README opisuje generatory, evaluatory, data mappers, strukturę `src/fi/opt/` i roadmapę obejmującą async, multi-objective, trace ingestion, wersjonowanie promptów i budżety kosztowe.

## Ryzyka
- optymalizacja promptów może zwiększać koszty i liczbę wywołań modeli;
- LLM-as-judge jest podatny na drift i bias;
- integracja z traceAI może przenosić dane produkcyjne do procesu optymalizacji;
- brak dowodu reprodukowalności wyników benchmarków w samym audycie.

## Priorytet
WYSOKI

## Kolejność prac
1. Zweryfikować package metadata, testy i CI.
2. Ustalić limity kosztu/tokenów i deterministyczne seedowanie tam, gdzie możliwe.
3. Testy regresji dla każdego algorytmu i evaluatorów.
4. Kontrola prywatności danych treningowych/trace.
5. Polonizacja i rebranding po stabilizacji API.

## Kryterium zakończenia
Powtarzalne testy wszystkich optimizerów, jawne limity kosztowe i udokumentowane zachowanie evaluatorów.
