# Audyt 325 — openinterpreter

## Stan
AUDYT ZAKOŃCZONY — agent wykonujący polecenia/kod, krytyczny.

## Ustalenia
Projekt Open Interpreter umożliwia modelowi wykonywanie kodu i działań przez interfejs agenta. Powierzchnia obejmuje LLM, interpreter, system plików i potencjalnie procesy systemowe.

## Ryzyka
Arbitrary code execution; filesystem/network access; sekrety; prompt injection; niejawne działania narzędziowe.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Zweryfikować sandbox i allowlisty.
2. Oddzielić planowanie od wykonania.
3. Dodać approval gates i limity zasobów.
4. Zweryfikować testy bezpieczeństwa.

## Kryterium zakończenia
Żadne działanie systemowe bez jawnej polityki i kontrolowanej granicy wykonania.