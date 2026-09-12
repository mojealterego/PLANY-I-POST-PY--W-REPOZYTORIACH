# Plan pracy — getbelmo

## Status
AUDYT ZAKOŃCZONY — MCP CLI do zarządzania hostingiem/deploymentami Belmo.

## Stan faktyczny
README opisuje Node CLI MCP z logowaniem lokalnym, OAuth tokenem, workspace/project/deployment lifecycle, logami, env vars, domenami, GTM i GitHub. Ruch API idzie po HTTPS. Lokalny helper nasłuchuje na 127.0.0.1, używa jednorazowego nonce, a credentials są szyfrowane AES-256-GCM.

## Ryzyka
bardzo szeroki zestaw operacji deploymentowych; token OAuth kopiowany ręcznie; klucze szyfrowania zależne od host/user/home; env vars i sekrety; rollback/stop/start; GitHub integration.

## Priorytet
KRYTYCZNY.

## Kolejność prac
1. Audyt tool-by-tool i authorization model.
2. Zweryfikować nonce, CSRF, cookie/token handling i crypto key derivation.
3. Approval gates dla deploy/rollback/env/domain.
4. Audit log i minimalne scopes GitHub.
5. Testy negatywne i polska dokumentacja.

## Kryterium zakończenia
Żadna operacja skutkująca zmianą infrastruktury bez jawnej autoryzacji i testu bezpieczeństwa.