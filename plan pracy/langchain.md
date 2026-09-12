# Plan pracy — langchain

## Status
AUDYT ZAKOŃCZONY — duży framework agentowy/LLM, repo referencyjne wysokiej wartości.

## Stan faktyczny
README określa LangChain jako platformę inżynierii agentów i aplikacji LLM. Wspiera modele, embeddingi, vector stores, retrievery, narzędzia i integracje oraz kieruje do LangGraph, Deep Agents i LangSmith. Repo jest upstreamowym, rozbudowanym projektem bibliotecznym, więc lokalizacja ma dotyczyć warstwy dokumentacyjnej/wybranych artefaktów, a nie niszczyć API.

## Ryzyka
szybkie zmiany API; ogromna macierz integracji; supply chain; wykonywanie narzędzi przez agentów; prompt/data leakage; kompatybilność wersji.

## Priorytet
WYSOKI / REFERENCYJNY.

## Kolejność prac
1. Ustalić snapshot wersji i główne pakiety.
2. Przeanalizować integracje, tool execution i granice zaufania.
3. Zweryfikować testy i CI.
4. Oznaczyć materiały upstreamowe zamiast tworzyć lokalny fork funkcjonalny.
5. Przygotować polskie dokumenty indeksujące wiedzę.

## Kryterium zakończenia
Mapa architektury, provenance upstreamu, testy krytycznych ścieżek i polski indeks bez naruszania kompatybilności.