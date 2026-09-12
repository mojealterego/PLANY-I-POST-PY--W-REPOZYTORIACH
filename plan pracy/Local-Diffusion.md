# Plan pracy — Local-Diffusion

## Stan audytu
- Audyt: ZAKOŃCZONY
- Klasyfikacja: mobilna aplikacja Flutter/Android do lokalnej generacji obrazów
- Priorytet: WYSOKI
- Status produkcyjny: NIE POTWIERDZONO

## Ustalenia
README opisuje lokalną inferencję diffusion na Androidzie przez stable-diffusion.cpp, obsługę wielu architektur modeli, kwantyzację, ControlNet, PhotoMaker, img2img, inpainting/outpainting, LoRA oraz eksperymentalne GPU. Projekt deklaruje build Flutter i release APK. `pubspec.yaml` wskazuje Flutter/Dart, FFI, picker plików, permission_handler, galerie, shadcn_ui, animacje i inne biblioteki; wersja aplikacji 1.0.0+1, SDK Dart >=3.2.3 <4.0.0.

## Ryzyka
1. Należy niezależnie zweryfikować kompatybilność deklarowanych formatów/modeli z aktualnym silnikiem.
2. Pobieranie modeli z Hugging Face/Civitai wymaga kontroli źródła, integralności, licencji i rozmiaru.
3. FFI/native engine oraz uprawnienia Androida wymagają audytu pamięci, lifecycle i bezpieczeństwa.
4. Benchmarki pamięci i wydajności wymagają reprodukcji na reprezentatywnych urządzeniach.
5. Trzeba rozdzielić możliwości lokalne od ewentualnych funkcji sieciowych i potwierdzić prywatność.
6. Zależności Dart są częściowo zakresowe (`^`), więc reprodukowalność release wymaga lockfile i procesu aktualizacji.

## Kolejność prac
1. Zmapować Flutter UI, warstwę FFI i native engine.
2. Zweryfikować pipeline model → kwantyzacja → inferencja → zapis obrazu.
3. Przetestować import modeli, duże pliki i błędy pamięci.
4. Audyt uprawnień, storage, sieci i pobierania modeli.
5. Dodać testy integracyjne oraz testy urządzeniowe Android.
6. Powtórzyć benchmarki RAM/VRAM/czasu generacji.
7. Ustabilizować wersje zależności i release APK.
8. Następnie polonizacja i rebranding.

## Kryterium zakończenia
Powtarzalny release Android, zweryfikowany pipeline lokalnej inferencji, bezpieczny import/pobieranie modeli oraz reprodukowalne benchmarki.
