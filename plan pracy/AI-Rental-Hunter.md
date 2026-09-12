# Plan pracy — AI-Rental-Hunter

## Status audytu
AUDYT ZAKOŃCZONY — repozytorium #42 w bieżącym przebiegu.

## Stan faktyczny
Pythonowy serwis MCP ukierunkowany na wyszukiwanie i analizę ofert najmu. README deklaruje narzędzia wyszukiwania, analizy pojedynczej oferty, rankingu i kalkulacji całkowitego kosztu. Architektura rozdziela MCP, wyszukiwanie, scoring i sygnały ryzyka. Repo ma `README.md`, `requirements.txt`, `.env.example`; dokumentacja wspomina także Docker/Railway.

Zależności: MCP 1.x, httpx, Pydantic 2.x, python-dotenv, BeautifulSoup4.

## Mocne strony
- deterministyczny scoring;
- normalizacja kosztów;
- sygnały ryzyka/scam screening;
- ograniczenie integracji do zgodnych z regulaminami źródeł;
- brak deklarowanego obchodzenia anti-bot i stref uwierzytelnionych.

## Ryzyka
- scraping/adapters muszą respektować regulaminy, robots i rate limits;
- wymagane testy parserów na danych z brakującymi i sprzecznymi polami;
- scoring ryzyka nie może być prezentowany jako pewne wykrycie oszustwa;
- należy zweryfikować izolację HTTP transportu, SSRF, limity URL i timeouty;
- trzeba sprawdzić rzeczywiste pliki deploymentu i testów, zanim projekt zostanie uznany za gotowy produkcyjnie.

## Kolejność prac
1. Zmapować moduły MCP i adaptery źródeł.
2. Dodać walidację URL/SSRF, timeouty, limity rozmiaru odpowiedzi i kontrolę przekierowań.
3. Testy kontraktowe modelu oferty, scoringu i kalkulacji kosztów.
4. Testy adapterów z fixture'ami zamiast zależności od żywych stron.
5. Zweryfikować Docker/Railway i konfigurację sekretów.
6. Polonizacja README/docs oraz doprecyzowanie granic odpowiedzialności scoringu ryzyka.

## Kryterium zakończenia
Bezpieczny MCP z testami deterministycznymi, odporny na złośliwe/nieprzewidywalne URL-e, z udokumentowanym zachowaniem adapterów i reprodukowalnym wdrożeniem.
