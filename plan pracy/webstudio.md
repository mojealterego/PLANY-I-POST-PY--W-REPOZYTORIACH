# AUDYT 355 — webstudio

## Status
Audyt na podstawie README i metadanych. Webstudio to open-source visual development platform z możliwością self-hostingu.

## Ustalenia
- Platforma dla developerów, designerów i zespołów.
- Użytkownik kontroluje dane, komponenty i infrastrukturę.
- Core repozytorium jest AGPL-3.0-or-later.
- `sdk-components-animation` jest opcjonalnym komponentem proprietary z osobną EULA.
- Fork lokalny wskazuje na upstream Webstudio.

## Ryzyka
Licencjonowanie komponentów, synchronizacja z upstream, bezpieczeństwo edytora i generowanego artefaktu.

## Plan prac
1. Zmapować monorepo, pakiety i build.
2. Zweryfikować model publikacji i self-hostingu.
3. Zidentyfikować granice AGPL/EULA.
4. Zbadać sanitizację HTML/CSS/JS i izolację wykonywanego kodu.
5. Przygotować lokalizację polską bez zmiany licencji upstream.

## Kryterium zakończenia
Zweryfikowany build, granice licencyjne i model bezpiecznego publikowania. Audyt nie oznacza produkcyjności.
