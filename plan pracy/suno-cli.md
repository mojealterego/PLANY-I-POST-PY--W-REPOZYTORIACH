# Audyt 159 — suno-cli

## Status
AUDYT ZAKOŃCZONY — Rust CLI integrujący się z nieoficjalnym API Suno.

## Ustalenia
README opisuje Rust 2024, CLI do generowania muzyki, autoryzację przez cookies przeglądarki, generowanie/pobieranie utworów, persony głosu, CAPTCHA, JSON oraz integrację z agentami. Projekt wyraźnie wskazuje brak oficjalnego API Suno.

## Ryzyka
- automatyczne pozyskiwanie sesji przeglądarki i przechowywanie poświadczeń;
- zależność od niepublicznych kontraktów usług;
- CAPTCHA i mechanizmy antynadużyciowe;
- self-update bez pełnej weryfikacji podpisu/attestacji artefaktu;
- koszty i prawa do wygenerowanych treści.

## Priorytet
WYSOKI.

## Kolejność prac
Audyt zależności i auth → bezpieczeństwo sekretów → stabilność API → weryfikacja artefaktów aktualizacji → testy offline → zgodność/licencje.

## Kryterium zakończenia
Bezpieczny model auth, deterministyczne testy, kontrolowane aktualizacje i udokumentowana zgodność z usługą.
