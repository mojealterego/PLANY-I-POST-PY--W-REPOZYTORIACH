# Plan pracy — dcache

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: rozproszony system storage / projekt infrastrukturalny
- Priorytet: KRYTYCZNY
- Status produkcyjny: NIEPOTWIERDZONY

## Ustalenia
dCache jest dużym systemem rozproszonego przechowywania danych z wirtualnym systemem plików, replikacją, zarządzaniem przestrzenią, recovery i wieloma protokołami dostępu. README odsyła do książki, User Guide i BUILDING.md oraz deklaruje AGPLv3 z częściami BSD/LGPL. Manifest Maven wskazuje Java 21, Jenkins CI i bardzo rozbudowane dependency management. fileciteturn235file0 fileciteturn236file0

## Ryzyka
1. System ma bardzo szeroki zakres funkcjonalny i wysoką złożoność rozproszoną.
2. Wiele protokołów storage/network wymaga testów interoperacyjności i bezpieczeństwa.
3. Należy kontrolować zgodność Java/dependencies oraz transitive dependencies.
4. Dane mogą być krytyczne operacyjnie; backup, recovery i failure semantics muszą być jawnie testowane.

## Kolejność prac
1. Zmapować moduły, usługi i protokoły.
2. Przeanalizować testy jednostkowe/systemowe i Jenkins.
3. Zbudować macierz Java/dependency/protocol compatibility.
4. Zweryfikować auth, TLS, ACL, izolację storage i konfigurację usług.
5. Przetestować failure/recovery/replication semantics.
6. Zachować upstream provenance; rebranding tylko własnych warstw.

## Kryterium zakończenia
Reprodukowalny build, zweryfikowane testy systemowe i recovery, audyt bezpieczeństwa interfejsów oraz aktualna dokumentacja operacyjna.
