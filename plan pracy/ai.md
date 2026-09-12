# Plan pracy — ai

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: lokalny generator obrazu/wideo AI o charakterze 18+
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
README deklaruje lokalny generator Wan 2.5 z generacją obrazu/wideo i dużą biblioteką LoRA. Repozytorium opisuje instalatory dla Windows/Linux i wymagania GPU. Dokumentacja zawiera treści seksualne oraz deklarowane zabezpieczenia dotyczące wieku, zgody i zakazu materiałów z udziałem małoletnich. fileciteturn237file0 Nie znaleziono `requirements.txt` na oczekiwanej ścieżce, więc rzeczywisty runtime/dependency graph wymaga dalszego mapowania.

## Ryzyka
1. Szczególnie istotna jest kontrola treści i ochrona przed generowaniem materiałów bez zgody lub z udziałem osób małoletnich.
2. Model/LoRA provenance, licencje i integralność artefaktów wymagają weryfikacji.
3. Instalatory i lokalne wykonywanie modeli wymagają audytu supply-chain.
4. Deklarowane parametry jakości/wydajności wymagają reprodukowalnego benchmarku.

## Kolejność prac
1. Zmapować rzeczywisty kod, runtime i installer.
2. Zweryfikować źródła modeli/LoRA i licencje.
3. Zdefiniować bezpieczne guardraile dotyczące treści, zgody i wieku.
4. Przetestować import modeli, generację i obsługę błędów.
5. Zweryfikować integralność instalatorów i aktualizacji.
6. Dopiero po tym przeprowadzić polonizację/rebranding własnych elementów.

## Kryterium zakończenia
Zweryfikowany runtime i supply chain, kontrola ryzyk treściowych, integralność modeli/instalatorów oraz reprodukowalne testy generacji.
