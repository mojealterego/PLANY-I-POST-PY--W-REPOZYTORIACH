# AUDYT 368 — Librechat-Mobile

## Status
Audyt wykonany. Natywny klient Android/iOS dla self-hosted LibreChat, niezależny od upstream.

## Ustalenia
Kotlin Multiplatform, Compose, Ktor, Room/DataStore, secure token storage, SSE, MCP/agents, multi-account, artifacts, voice i adaptacyjny UI.

## Ryzyka
Wiele kont/serwerów, tokeny, self-signed TLS, pliki i artifacts, deep links, streaming oraz kompatybilność wersji backendu.

## Plan prac
Zweryfikować storage per account, TLS, token lifecycle, import/export, deep links, MCP config i CI release signing. Następnie polonizacja.

## Kryterium zakończenia
Testy Android/iOS, bezpieczny storage i transport, zweryfikowana proweniencja APK oraz brak cross-account leakage.
