# Audyt: youpac-ai

## Status
AUDYT ZAKOŃCZONY — aktywny prototyp produktu.

## Stan faktyczny
README opisuje platformę AI dla twórców YouTube: upload wideo do 1 GB, transkrypcję ElevenLabs, generowanie tytułów/opisów/miniatur/postów, wizualny canvas, współpracę i podglądy. Stos: React Router 7, React 19, TypeScript, Convex, Clerk, OpenAI, ElevenLabs, FFmpeg, Tailwind/shadcn, Vercel. `package.json` potwierdza m.in. React Router 7.5.3, React 19.1, Convex 1.24.3, OpenAI 5.6.0, FFmpeg WASM i Zod.

## Ryzyka
- przetwarzanie dużych plików wideo i koszty storage/transferu;
- sekrety OpenAI/ElevenLabs/Clerk oraz granice klient-serwer;
- izolacja projektów i udostępnianych canvasów;
- generowany kod i treści AI wymagają walidacji;
- deklarowana gotowość produkcyjna wymaga reprodukcji build/testów.

## Priorytet
KRYTYCZNY/WYSOKI — strategiczny kandydat na produkt komercyjny.

## Kolejność prac
1. testy end-to-end upload→transkrypcja→generacja→eksport;
2. audyt autoryzacji Convex/Clerk i share links;
3. limity, kolejki i kontrola kosztów modeli;
4. walidacja FFmpeg i bezpieczeństwo plików;
5. observability, billing i hardening deploymentu;
6. pełna polonizacja i rebranding.

## Kryterium zakończenia
Powtarzalny build, testy krytycznych ścieżek, potwierdzona izolacja danych i kontrola kosztów. Audyt nie oznacza produkcji.
