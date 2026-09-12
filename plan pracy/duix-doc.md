# AUDYT 354 — duix-doc

## Status
Audyt wykonany na podstawie README i metadanych repozytorium. Repozytorium jest projektem dokumentacji Mintlify.

## Ustalenia
- Mintlify CLI (`mint`) do lokalnego podglądu i publikacji.
- Dokumentacja jest powiązana z organizacją duixcom i GitHub App.
- README wskazuje, że push do `main` nie uruchamia samoczynnie aktualizacji online; wymagane jest zsynchronizowanie dostępu GitHub App w panelu Mintlify.
- Brak podstaw do traktowania repo jako aplikacji produkcyjnej.

## Ryzyka
- ręczny krok synchronizacji może powodować rozjazd źródła i publikacji;
- należy zweryfikować konfigurację CI/CD, zależności i wersję Mintlify;
- trzeba sprawdzić, czy w repo nie ma danych lub sekretów publikacyjnych.

## Plan prac
1. Zmapować pełne drzewo dokumentacji i konfigurację Mintlify.
2. Zweryfikować build dokumentacji lokalnie i w CI.
3. Usunąć ręczne punkty synchronizacji, jeśli można je zastąpić kontrolowanym deploymentem.
4. Ujednolicić język dokumentacji do polskiego, zachowując terminologię techniczną.
5. Dodać walidację linków, obrazów i wersjonowania.

## Kryterium zakończenia
Powtarzalny build dokumentacji, zweryfikowany deployment i brak sekretów w repozytorium. Audyt nie oznacza gotowości produkcyjnej.
