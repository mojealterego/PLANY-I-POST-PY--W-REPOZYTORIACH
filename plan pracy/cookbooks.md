# Plan pracy — cookbooks

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: katalog przykładów i warsztatów AI/RAG/agentów
- Priorytet: ŚREDNI
- Status produkcyjny: NIE DOTYCZY JAKO JEDNEJ APLIKACJI

## Ustalenia
README opisuje wiele niezależnych przykładów: computer use, e-commerce agent, Google Drive/RAG, generowanie i wyszukiwanie fontów, analizę wywiadów, multi-agent, RAG oraz warsztat Qdrant dotyczący degradacji jakości retrievalu. Repozytorium jest zbiorem cookbooków, a nie pojedynczym produktem. Największą wartością jest referencja implementacyjna i porównawcza.

## Ryzyka
1. Przykłady mogą mieć różne cykle życia i różne wymagania.
2. Integracje z usługami zewnętrznymi wymagają osobnych kontroli sekretów i kosztów.
3. Wyniki benchmarków z README należy traktować jako artefakty przykładowe do czasu reprodukcji.
4. Nie należy modernizować wszystkich przykładów jednym mechanizmem — każdy powinien mieć własny kontrakt.

## Kolejność prac
1. Zindeksować każdy cookbook wraz z runtime i zależnościami.
2. Oznaczyć przykłady: aktywny, demonstracyjny, historyczny.
3. Dodać wspólny standard `.env.example`, testów i instrukcji uruchomienia.
4. Zweryfikować benchmarki warsztatowe i dane wejściowe.
5. Oddzielić przykłady wymagające płatnych usług od lokalnych.
6. Przygotować polski indeks i opisy bez zmiany oryginalnych licencji.

## Kryterium zakończenia
Każdy przykład ma znany status, instrukcję uruchomienia, źródła danych/dependency contract i podstawowy smoke test albo jawne oznaczenie materiału referencyjnego.
