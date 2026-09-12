# Audyt 390 — agentic-ai-hack

## Status
AUDYT ZAKOŃCZONY — materiał hackathonowy dotyczący wieloagentowego przetwarzania roszczeń ubezpieczeniowych na Azure AI.

## Stan faktyczny
README opisuje sześć etapów: wdrożenie środowiska Azure, przetwarzanie dokumentów i wyszukiwanie wektorowe, budowę agenta, obserwowalność i ewaluację, wyspecjalizowane agenty oraz orkiestrację. Architektura obejmuje Azure AI Foundry/GPT-4.1-mini, Document Intelligence, Storage Accounts, Cosmos DB, Azure AI Search, Semantic Kernel, Azure Container Apps, Application Insights i Log Analytics. Przepływ kończy się wygenerowaniem podsumowania roszczenia do przeglądu człowieka.

Challenge 0 przewiduje automatyczne wdrożenie zasobów Azure, Codespaces, skrypt `get-keys.sh` oraz populowanie `.env` wartościami pobranymi z zasobów. To wymaga szczególnej kontroli sekretów i uprawnień Azure.

## Klasyfikacja
MATERIAŁ HACKATHONOWY / REFERENCYJNY, z potencjałem do wykorzystania jako prototyp systemu agentowego w domenie wysokiej odpowiedzialności. Nie traktować jako zweryfikowanego systemu produkcyjnego do automatycznego rozstrzygania roszczeń.

## Ryzyka
- decyzje dotyczące ubezpieczeń i ryzyka nie mogą być bezwarunkowo delegowane modelom;
- dokumenty roszczeń mogą zawierać dane osobowe, finansowe i zdrowotne;
- szerokie uprawnienia Azure Owner/Contributor oraz sekrety w `.env`;
- prompt injection i złośliwe dane wejściowe w dokumentach;
- błędy OCR, ekstrakcji, klasyfikacji i detekcji fraudów;
- wieloagentowa orkiestracja może propagować błędne ustalenia między agentami;
- brak dowodu, że metryki hackathonowe oznaczają gotowość produkcyjną;
- konieczność audytowalności, human-in-the-loop i kontroli wersji modeli/promptów.

## Priorytet
KRYTYCZNY dla bezpieczeństwa i governance; WYSOKI dla wartości referencyjnej.

## Kolejność prac
1. Zdefiniować granice odpowiedzialności człowieka i modelu.
2. Wprowadzić minimalne uprawnienia Azure i izolację środowisk.
3. Zabezpieczyć `.env`, klucze, logi i dane dokumentów.
4. Dodać testy odporności na prompt injection, błędny OCR i niejednoznaczne roszczenia.
5. Oddzielić ekstrakcję faktów od rekomendacji oraz każdą rekomendację oznaczać źródłem i poziomem pewności.
6. Wymusić human review przed jakąkolwiek decyzją mającą skutek finansowy lub prawny.
7. Zbudować ewaluację regresyjną, obserwowalność i ślad audytowy dla każdego agenta.
8. Dopiero po spełnieniu kontroli bezpieczeństwa rozważać refaktoryzację i polonizację.

## Kryterium zakończenia
Każdy wynik systemu jest weryfikowalny, przypisany do źródeł i podlega obowiązkowej kontroli człowieka przed działaniem o skutkach finansowych lub prawnych; sekrety są zarządzane poza kodem, a środowisko Azure działa według zasady najmniejszych uprawnień.

**Audyt ≠ produkcja.**
