# Plan pracy — unity-mcp

## Status
AUDYT ZAKOŃCZONY — aktywny MCP dla Unity, wysoka powierzchnia uprawnień.

## Stan faktyczny
README opisuje 47 entrypointów MCP do zarządzania scenami, GameObjects, assetami, skryptami C#, testami, profilowaniem i buildami. Wspiera Unity 2021.3 LTS–6.x, Python 3.10+, wiele klientów MCP, routing wielu instancji, grupy narzędzi i zdalny serwer z auth. Repo ma wersjonowane wydania i dokumentację security.

## Ryzyka
agent może wykonywać zmiany w projekcie; edycja i uruchamianie kodu; remote server; konfiguracja wielu instancji; MCP tool exposure; supply chain pluginów Unity.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Mapa wszystkich narzędzi i poziomów uprawnień.
2. Default-deny dla operacji destrukcyjnych i buildów.
3. Walidacja ścieżek, projektów i instancji.
4. Testy auth/remote transport/tool isolation.
5. Polska dokumentacja i macierz uprawnień.

## Kryterium zakończenia
Każda operacja ma określoną autoryzację, walidację i test regresji; brak niejawnego dostępu do hosta.