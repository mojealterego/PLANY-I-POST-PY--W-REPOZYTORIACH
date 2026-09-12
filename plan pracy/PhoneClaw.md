# Audyt 339 — PhoneClaw

## Stan
AUDYT ZAKOŃCZONY — natywny iOS local AI agent.

## Ustalenia
Swift 5.10/iOS 17+, Gemma 4 i MiniCPM-V on-device, Skills dla kalendarza, przypomnień, kontaktów, schowka, HealthKit, głosu i obrazu. Opcjonalnie Web Search i sparowany Mac Gateway. Repo opisuje confirmation dla niejasnych/czułych operacji.

## Ryzyka
Dane osobowe; HealthKit; Contacts/Calendar; clipboard; tool execution; LAN gateway; model downloads/signing.

## Priorytet
KRYTYCZNY.

## Kolejność prac
Permissions → approval gates → local storage → LAN pairing → model provenance → testy urządzeniowe.

## Kryterium zakończenia
Żadna operacja wrażliwa bez właściwej autoryzacji/confirmacji; bezpieczny kanał Mac Gateway.