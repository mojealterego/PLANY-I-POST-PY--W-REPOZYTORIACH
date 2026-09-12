# Plan pracy — 500-AI-Agents-Projects

## Status audytu
AUDYT ZAKOŃCZONY — repozytorium #40 w bieżącym przebiegu.

## Stan faktyczny
Repozytorium jest katalogiem 500+ projektów i przypadków użycia agentów AI, z przykładami frameworków takich jak LangGraph, CrewAI, AutoGen, Agno i LlamaIndex. README wskazuje osobne, samodzielne przykłady agentów, własne `requirements.txt` i `.env.example`.

## Klasyfikacja
Katalog wiedzy / repozytorium referencyjne, nie pojedyncza aplikacja do bezpośredniego refaktoru. Największa wartość dla ekosystemu to indeksowanie, deduplikacja, ocena aktualności i selekcja przykładów.

## Ryzyka
- część linków i projektów zewnętrznych może być nieaktualna;
- deklaracje typu „production examples” wymagają weryfikacji per wpis;
- przykłady z obszarów wysokiego ryzyka (medycyna, finanse, cyberbezpieczeństwo) wymagają oznaczeń kontekstu i ograniczeń;
- wiele niezależnych zależności utrudnia jednolity build całego katalogu.

## Kolejność prac
1. Zbudować maszynowy indeks agentów: nazwa, framework, domena, repozytorium, status utrzymania, licencja, ostatnia weryfikacja.
2. Walidować linki i deduplikować wpisy.
3. Rozdzielić działające implementacje, tutoriale, projekty archiwalne i same koncepcje.
4. Dodać datę oraz źródło każdej oceny aktualności.
5. Polonizować indeks i metodologię, nie tłumacząc bezrefleksyjnie nazw własnych frameworków.
6. Nie wykonywać zbiorczej modernizacji obcych projektów; modernizować wyłącznie własne artefakty po selekcji.

## Kryterium zakończenia
Powtarzalny indeks, sprawdzone linki, jasne oznaczenie statusu każdego wpisu i możliwość wykorzystania katalogu jako bazy wiedzy bez sugerowania, że wszystkie zewnętrzne projekty są produkcyjne.
