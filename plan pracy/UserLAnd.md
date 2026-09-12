# Audyt 324 — UserLAnd

## Stan
AUDYT ZAKOŃCZONY — środowisko Linux na Androidzie, referencyjne.

## Ustalenia
Projekt zapewnia uruchamianie dystrybucji/środowisk Linux na Androidzie bez klasycznej maszyny wirtualnej. Kluczowe obszary to procesy, filesystem, sieć, storage i integracja z Androidem.

## Ryzyka
Uprawnienia Android; izolacja filesystemu; procesy; sieć; kompatybilność wersji systemu.

## Priorytet
WYSOKI/REFERENCYJNY.

## Kolejność prac
1. Zmapować manifest i warstwę native.
2. Zweryfikować granice procesu/filesystemu.
3. Zweryfikować testy na aktualnych Androidach.

## Kryterium zakończenia
Udokumentowana izolacja i powierzchnia uprzywilejowana.