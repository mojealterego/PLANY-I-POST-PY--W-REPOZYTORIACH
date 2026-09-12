# Plan pracy — Stable-Diffusion-KMP

## Status
AUDYT ZAKOŃCZONY — projekt Stable Diffusion dla Kotlin Multiplatform.

## Stan faktyczny
Repozytorium ma około 82 MB i branch `master`. Należy zweryfikować natywne backendy, modele, platformy i integrację KMP.

## Ryzyka
- native/GPU compatibility;
- model provenance/licensing;
- duże artefakty;
- bezpieczeństwo danych obrazowych.

## Priorytet
WYSOKI — REFERENCJA.

## Kolejność prac
1. Mapowanie targetów KMP/native.
2. Runtime i model loading.
3. Testy urządzeń.
4. Provenance wag.

## Kryterium zakończenia
Powtarzalny build platform oraz zweryfikowane modele i licencje.
