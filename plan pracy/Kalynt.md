# Plan pracy — Kalynt

## Stan audytu
**AUDYT WSTĘPNY ZAKOŃCZONY — 2026-09-11**

## Ustalenia
- Repozytorium ma rozbudowaną strukturę monorepo: `apps`, `packages`, `examples`.
- Posiada osobne `ARCHITECTURE.md`, `CHANGELOG.md`, `CONTRIBUTING.md`, `SECURITY.md`, `Current_Changes.md` i README.MD.
- Jest obecne `package.json` oraz bardzo duży `package-lock.json`, co wskazuje na ekosystem Node.
- Istnieje `.env.example` oraz konfiguracja GitHub Actions.
- README występuje jako `README.MD`, co wymaga ujednolicenia nazewnictwa.

## Ryzyka
1. Monorepo wymaga jednoznacznych granic pakietów i zależności.
2. Należy zweryfikować architekturę opisaną w ARCHITECTURE.md względem kodu.
3. `.env.example` wymaga audytu pod kątem sekretów i niebezpiecznych wartości domyślnych.
4. Duży lockfile wymaga analizy zależności, duplikatów i podatności.
5. Równoległe dokumenty zmian mogą powodować rozjazd stanu rzeczywistego.

## Plan implementacji
1. Przeanalizować `ARCHITECTURE.md` i porównać z grafem pakietów.
2. Zmapować `apps` i `packages` wraz z zależnościami kierunkowymi.
3. Zidentyfikować wspólne biblioteki i punkty sprzężenia.
4. Zweryfikować skrypty package managera i pipeline CI.
5. Wykonać audyt zależności i bezpieczeństwa.
6. Ujednolicić dokumentację do `README.md` i zdefiniować źródło prawdy dla zmian.
7. Uporządkować konfigurację środowisk.
8. Dodać testy kontraktowe między pakietami.
9. Przygotować polską dokumentację architektury i wdrożenia.
10. Wykonać pełny build monorepo i walidację wszystkich aplikacji.

## Kryterium zakończenia
Spójny graf zależności, przechodzące CI, brak krytycznych podatności, zgodność dokumentacji z kodem i jednoznaczny proces wydawniczy.