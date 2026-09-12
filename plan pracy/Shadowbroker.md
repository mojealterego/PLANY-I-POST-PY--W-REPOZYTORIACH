# Plan pracy — Shadowbroker

## Status
AUDYT ZAKOŃCZONY — platforma OSINT/geospatial, wysokie ryzyko operacyjne.

## Stan faktyczny
README opisuje Next.js + MapLibre GL + FastAPI/Python, ponad 40 warstw danych, backendowe OSINT/recon, Shodan, kanał agentowy HMAC, mesh/InfoNet i wiele zewnętrznych feedów. Repo zawiera m.in. `.env.example`, Docker, CI GitLab, `backend/`, Makefile i rozbudowaną dokumentację.

## Ryzyka
SSRF i dostęp do usług zewnętrznych; bardzo szeroki zakres danych lokalizacyjnych; API keys; kanał agenta z akcjami read/write; źródła OSINT i retencja; obciążenie feedów; zgodność z ToS/licencjami.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zmapować wszystkie endpointy `/api`, narzędzia i uprawnienia.
2. Zweryfikować SSRF guards, HMAC, rate limits i trust boundary.
3. Ograniczyć operacje agenta do jawnie autoryzowanych akcji.
4. Dodać testy bezpieczeństwa, provenance feedów i retencji.
5. Spolonizować UI/dokumentację bez zmiany nazw protokołów/API.

## Kryterium zakończenia
Udokumentowany model zaufania, testy security, kontrola wyjścia danych i brak nieautoryzowanych operacji.