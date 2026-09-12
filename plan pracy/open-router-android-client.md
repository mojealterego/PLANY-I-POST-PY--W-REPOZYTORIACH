# AUDYT 356 — open-router-android-client

## Status
Audyt wykonany na podstawie README. Edukacyjna aplikacja Android korzystająca z OpenRouter.

## Ustalenia
Kotlin/Android, Clean Architecture, MVVM, Hilt, Coroutines/Flow, Room, Retrofit2, ViewBinding i Markwon. Funkcje obejmują czat, historię, ulubione modele i własny klucz API.

## Ryzyka
Sekret API przechowywany po stronie urządzenia, bezpieczeństwo logów/cache, TLS, walidacja odpowiedzi i kompatybilność API OpenRouter.

## Plan prac
Zweryfikować manifest, storage, interceptor Retrofit, obsługę błędów i sekretów, testy oraz wersje zależności. Następnie lokalizacja polska i hardening.

## Kryterium zakończenia
Build/testy Android przechodzą, sekret nie trafia do logów ani repo, a storage i transport są bezpieczne.
