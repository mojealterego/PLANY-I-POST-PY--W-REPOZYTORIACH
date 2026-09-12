# Audyt 332 — mailtm_client

## Stan
AUDYT ZAKOŃCZONY — pakiet Dart/Flutter dla mail.tm.

## Ustalenia
README opisuje wrapper API do tworzenia/logowania kont tymczasowej poczty, pobierania domen, wiadomości, źródeł i załączników oraz usuwania/aktualizacji kont. Stan uwierzytelnienia obejmuje hasło i JWT.

## Ryzyka
Przechowywanie credentials/JWT; dane i załączniki wiadomości; nadużycia usług temp-mail; zgodność API.

## Priorytet
ŚREDNI/WYSOKI.

## Kolejność prac
1. Zweryfikować modele auth i storage.
2. Dodać testy błędów API i wygasania tokenów.
3. Ograniczyć logowanie treści poczty.
4. Udokumentować bezpieczne zastosowanie.

## Kryterium zakończenia
Brak wycieku credentials/treści, poprawna obsługa tokenów i testy API.