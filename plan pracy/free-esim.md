# Plan pracy — free-esim

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: projekt/web/landing + dokumentacja
- Priorytet: WYSOKI
- Domyślna gałąź: `main`
- Stan źródłowy: repozytorium zawiera obecnie tylko `README.md`; deklarowana architektura nie jest odzwierciedlona w zawartości repozytorium.

## Ustalenia
- README opisuje eSIMFree.org jako platformę z darmowym pakietem 5 GB, globalnym zasięgiem i aktywacją przez QR.
- README deklaruje Next.js/Tailwind, Node/Express/Cloudflare Workers, Firebase/Supabase, Vercel/Cloudflare/DigitalOcean oraz integracje Mailgun/Telegram, ale brak kodu implementacyjnego potwierdzającego te warstwy.
- Występują deklaracje biznesowe i techniczne wymagające niezależnej weryfikacji przed publikacją produkcyjną.
- Kontakt zawiera instrukcję zastępczą, co wskazuje na niedomkniętą dokumentację.

## Ryzyka
1. Rozbieżność między deklarowanym stosem a faktyczną zawartością repozytorium.
2. Brak testów, CI/CD, konfiguracji wdrożenia i infrastruktury jako kodu.
3. Brak widocznej implementacji procesu provisioning/aktywacji eSIM.
4. Ryzyko publikacji nieweryfikowanych twierdzeń o zasięgu, darmowości i parametrach usługi.

## Kolejność prac
1. Ustalić kanoniczny zakres produktu i właściciela danych biznesowych.
2. Odtworzyć rzeczywisty kod aplikacji albo jednoznacznie sklasyfikować repo jako dokumentacyjne.
3. Zaprojektować Clean Architecture dla frontendu, API, integracji operatorskich i warstwy danych.
4. Dodać walidację konfiguracji, sekrety poza repozytorium, testy i CI.
5. Zweryfikować przepływ aktywacji, obsługę błędów, prywatność i bezpieczeństwo danych telekomunikacyjnych.
6. Przeprowadzić pełną polonizację dokumentacji i interfejsu oraz uporządkować branding.
7. Potwierdzić build i wdrożenie dopiero po uzyskaniu rzeczywistego kodu.

## Kryterium zakończenia
Repozytorium ma zawierać kompletną, testowalną implementację albo jawnie zostać utrzymane jako repozytorium dokumentacyjne; wszystkie deklaracje README muszą mieć źródło lub status niezweryfikowane.
