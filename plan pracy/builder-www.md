# Audyt 77 — builder-www

## Stan
AUDYT ZAKOŃCZONY — aktywny fork/repozytorium Frappe Builder.

## Ustalenia
README opisuje low-code website builder oparty o Frappe Framework/Frappe UI, z AI page generation, CMS, skryptami, publikacją i analityką. Repo ma workspace `frontend` i `frappe-ui`; `package.json` wymaga Node >=18, AGPL-3.0-only, a skrypty obejmują instalację, dev i build.

## Ryzyka
- fork/upstream ownership i zakres własnych zmian wymagają rozdzielenia;
- konfiguracja developerska zawiera `ignore_csrf 1` — tylko lokalnie;
- skrypty instalacyjne pobierane z zewnętrznego źródła wymagają pinowania i weryfikacji integralności;
- brak w tym przebiegu pełnej weryfikacji testów frontend/backend.

## Priorytet
WYSOKI — duża wartość jako baza wizualnego buildera, ale wymagane zarządzanie upstream i bezpieczeństwo konfiguracji.

## Kolejność prac
1. Zidentyfikować własne commity względem upstream.
2. Zmapować frontend/Frappe/backend i CI.
3. Zweryfikować auth, CSRF, publikowanie i wykonywanie skryptów użytkownika.
4. Dodać kontrakty testowe, build/release i testy bezpieczeństwa.
5. Dopiero potem polonizacja i rebranding.

## Kryterium zakończenia
Reprodukowalny build, testy przechodzą, granice skryptów/CMS są udokumentowane, a własne zmiany są oddzielone od upstream.