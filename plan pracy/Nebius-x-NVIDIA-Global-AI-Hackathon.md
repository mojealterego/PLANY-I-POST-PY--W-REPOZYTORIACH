# Plan pracy — Nebius-x-NVIDIA-Global-AI-Hackathon

## Stan audytu
- **Audyt:** zakończony
- **Klasyfikacja:** prototyp SRE/agentic AI z bezpieczną, ograniczoną remediacją
- **Priorytet:** KRYTYCZNY
- **Produkcja:** NIE

## Ustalenia
InfraSentinel-Agentic rozdziela rozumowanie modelu, pozyskiwanie dowodów, deterministyczną autoryzację, governance i wykonanie. Publiczny prototyp używa symulatora i nie udostępnia arbitralnego shell execution. Akcje posiadają m.in. zakres, poziom ryzyka, identyfikatory dowodów, preconditions, expected effect, postconditions, rollback i idempotency key.

`pyproject.toml` definiuje Python >=3.11, pakiet `infrasentinel-agentic` 0.1.0, CLI `infrasentinel` oraz zależności OpenAI, Tavily, NeMo Guardrails, Pydantic, dotenv i YAML. Testy i Ruff są zależnościami developerskimi. README opisuje CLI demo, benchmark bezpieczeństwa i weryfikację łańcucha audytowego.

## Ryzyka / luki
1. Integracje Nebius/Tavily i Guardrails wymagają niezależnej weryfikacji rzeczywistego runtime, a nie tylko zgodności konfiguracji.
2. Przejście z symulatora do realnego Kubernetes/GitOps będzie zmianą poziomu ryzyka i wymaga osobnych adapterów oraz uprawnień namespace-scoped.
3. Dowody pobierane z sieci są poprawnie traktowane jako dane nieufne, ale należy przetestować odporność na prompt injection w treści źródeł i wynikach narzędzi.
4. Należy potwierdzić, że executor nie posiada ukrytej ścieżki omijającej `PolicyEngine`/governance.
5. Hash-chain audit wymaga testów integralności, rotacji/retencji oraz zachowania przy współbieżności.

## Kolejność prac
1. Przejrzeć `app/`, `tests/`, konfiguracje Guardrails, adaptery providerów i CI.
2. Zweryfikować niezmiennik `model proposes → policy authorizes → executor executes` testami kontraktowymi.
3. Rozszerzyć adversarial benchmark o prompt injection, skażone evidence i konflikty dowodów.
4. Zweryfikować idempotencję, rollback i post-condition verification.
5. Ustabilizować wersje zależności i reprodukowalność środowiska.
6. Wykonać testy integracyjne providerów wyłącznie w bezpiecznym zakresie.
7. Dopiero w osobnym etapie projektować namespace-scoped Kubernetes/GitOps adaptery.
8. Polonizować własną dokumentację i interfejs CLI po ustabilizowaniu kontraktów.

## Kryterium zakończenia
Benchmark bezpieczeństwa, testy policy/executor i integralność audytu muszą być powtarzalne. Realna infrastruktura nie może otrzymać większego blast radius tylko dlatego, że model jest bardziej kompetentny. Audyt nie oznacza produkcji.
