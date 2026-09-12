# Audyt: SillyTavern

## Stan
AUDYT — duża aplikacja webowa interfejsu dla modeli konwersacyjnych, rozszerzeń i providerów.

## Ryzyka
Rozszerzenia, integracje z zewnętrznymi modelami, treści użytkownika i konfiguracja mogą zwiększać powierzchnię ataku. Należy kontrolować pluginy, sekrety i outbound network.

## Priorytet
WYSOKI/KRYTYCZNY.

## Kolejność
Extension model → auth/data → secrets → network → content safety → tests → deployment.

## Kryterium zakończenia
Kontrolowane rozszerzenia, bezpieczne sekrety i testy integracyjne providerów.
