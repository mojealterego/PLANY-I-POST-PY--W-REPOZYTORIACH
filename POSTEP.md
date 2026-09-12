# Rejestr postępu — ARCH-ENG-CORE-999

## Stan bieżący

- Data aktualizacji: 2026-09-12
- Faza: **2 — ranking priorytetów**
- Inwentaryzacja portfela: **414 repozytoriów**
- Rekonsyliacja inwentarza: **414/414 — zakończona**
- Audyt szczegółowy: **414/414 — zakończony**
- Konsolidacja wyników: **zakończona**
- Ranking priorytetów: **utworzony**
- Refaktoryzacja: oczekuje na wybór pierwszego P0
- Rebranding: oczekuje
- Polonizacja: oczekuje
- Nowe projekty: oczekują na kwalifikację

## Ranking priorytetów

Utworzono `RANKING_PRIORYTETOW_414.md`. Ranking rozdziela potencjał biznesowy od gotowości produkcyjnej i uwzględnia: problem biznesowy, gotowość kodu, MRR/ARPU, B2B, aktywa technologiczne, skalowalność, bezpieczeństwo/regulacje oraz time-to-market.

### P0 — strategiczny rdzeń

1. B2B AI Agent / AI Employee
2. Agent automatyzacji procesów przedsiębiorstwa
3. Agent programistyczny z izolowanym execution sandbox
4. Agent mobilny Android
5. Agent dokumentów + RAG / Knowledge Agent
6. AI Customer Support / Voice Agent
7. AI Sales / CRM Agent

### P1 — bardzo wysoki

8. Private / Offline AI Assistant
9. Agent Research / Knowledge Management
10. Platforma budowy agentów i workflowów
11. AI Developer Tools
12. Platforma AI dla twórców — obraz/wideo/audio

### P2 — średni/wysoki

13. Telecom / PBX / Voice automation
14. Mobile productivity agents
15. Lokalne generowanie obrazu/wideo
16. AI app/workflow builder
17. Gry z AI

### P3–P5

Upstream/reference, research/lab oraz repozytoria minimalne są kierowane do odpowiednio zachowania, wykorzystania jako źródła wiedzy lub archiwizacji. Nie są bezpośrednimi kandydatami do ślepego rebrandingu.

## Decyzja strategiczna

Pierwszym celem po rankingu jest budowa **jednego bezpiecznego, modułowego rdzenia B2B AI Agent / AI Employee**, z którego będą wyprowadzane wyspecjalizowane produkty. Nie rozpoczynamy równoległej produkcji wielu niezależnych aplikacji.

## Następny etap

**Etap 3 — wybór konkretnego produktu P0 i rozpoczęcie refaktoryzacji.** Przed wdrożeniem obowiązują bramki: deny-by-default, sandbox, approval dla działań konsekwencyjnych, izolacja tenantów, testy bezpieczeństwa, obserwowalność, recovery, SBOM/provenance oraz weryfikacja licencji.
