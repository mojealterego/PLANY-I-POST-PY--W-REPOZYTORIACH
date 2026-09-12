# Audyt: n8n

## Stan
AUDYT — duża platforma workflow automation z szerokim ekosystemem integracji.

## Ryzyka
Credential management, webhooki, connector execution, arbitrary HTTP/code nodes, multi-user isolation i secret leakage są kluczowe.

## Priorytet
KRYTYCZNY.

## Kolejność
Auth/tenancy → credentials → node permissions → network/code execution → webhook security → tests → deployment.

## Kryterium zakończenia
Ścisłe granice connectorów i kodu, bezpieczne sekrety, audit trail oraz testy wielodostępności.
