# Audyt 299 — agent-learning-kit

## Stan
AUDYT ZAKOŃCZONY — SDK ewaluacji agentów/LLM.

## Ustalenia
README opisuje AI-Evaluation SDK z 72 metrykami lokalnymi, LLM-as-Judge, skanerami jailbreak/code injection/PII/secrets, oceną strumieniową, AutoEval, pętlą feedbackową, OpenTelemetry i backendami rozproszonymi. Dostępne są interfejsy Python i TypeScript. Licencja Apache 2.0.

## Ryzyka
- fałszywie dodatnie/ujemne wyniki ewaluacji;
- dane w feedback store i telemetry;
- integracje z zewnętrznymi modelami;
- koszt i retencja scoringu cloud;
- bezpieczeństwo automatycznych guardrails.

## Priorytet
WYSOKI

## Plan prac
Zweryfikować metryki i benchmarki → testy deterministyczności → izolacja danych → polityki retencji → CI/eval gates → pinowanie zależności → polonizacja dokumentacji.

## Kryterium
Każda metryka ma znaną definicję, testy i ograniczenia; wyniki nie są traktowane jako absolutna prawda produkcyjna.
