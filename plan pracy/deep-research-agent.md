# Audyt 164 — deep-research-agent

## Status
AUDYT ZAKOŃCZONY — TypeScriptowy wieloagentowy system researchowy z human-in-the-loop.

## Ustalenia
Pipeline dzieli pytanie na podproblemy, czeka na potwierdzenie, wyszukuje web/źródła akademickie, scrapuje URL-e, tworzy raport z cytowaniami, wersjonuje projekty i obsługuje follow-up chat. README opisuje Next.js frontend, EdgeOne functions i timeout 300 s.

## Ryzyka
Jakość źródeł i cytowań, scraping zewnętrznych URL, SSRF, limity/cost, przechowywanie raportów, sesje conversation_id i integralność wersji.

## Priorytet
WYSOKI.

## Kolejność prac
Źródła → izolacja fetch/scrapingu → auth → storage/versioning → citation validation → limity kosztów → testy end-to-end.

## Kryterium zakończenia
Reprodukowalny raport ze sprawdzalnym pochodzeniem źródeł i bezpiecznym pobieraniem treści.
