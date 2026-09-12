# Plan pracy — mcp-server-phone

## Status
AUDYT ZAKOŃCZONY — MCP związany z funkcjami telefonu.

## Stan faktyczny
Repozytorium ma około 600 KB. Dokładny zakres narzędzi należy potwierdzić w kodzie i manifestach.

## Ryzyka
- telefon/SMS i dane użytkownika;
- narzędzia wykonujące działania zewnętrzne;
- auth i sekrety;
- błędne lub nieautoryzowane wywołania.

## Priorytet
WYSOKI.

## Kolejność prac
1. Mapa tool contracts.
2. Permission matrix.
3. Approval/confirmation gates.
4. Testy negatywne.

## Kryterium zakończenia
Jawne uprawnienia, walidacja parametrów i bezpieczne wykonanie narzędzi.
