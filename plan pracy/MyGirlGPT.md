# Plan pracy — MyGirlGPT

## Status
AUDYT ZAKOŃCZONY — wielokomponentowy AI companion.

## Stan faktyczny
Projekt składa się z TelegramBota, serwera LLM, serwera TTS i serwera generowania obrazów. Dokumentacja wskazuje text-generation-webui, Bark, Stable Diffusion WebUI, lokalny model oraz uruchamianie na własnym serwerze/RunPod.

## Ryzyka
Tokeny Telegram/API, prywatne rozmowy, generowanie obrazów i głosu, sieciowa komunikacja między usługami, ekspozycja portów, stare zależności/model stack oraz brak jednoznacznej granicy danych prywatnych.

## Priorytet
WYSOKI.

## Kolejność prac
1. Zmapować wszystkie usługi i porty.
2. Przenieść sekrety do bezpiecznej konfiguracji.
3. Wprowadzić TLS/auth i ograniczenie sieci.
4. Zdefiniować retencję oraz usuwanie rozmów.
5. Zweryfikować modele, licencje i provenance.
6. Dodać testy integracyjne i health checks.
7. Polonizacja i rebranding.

## Kryterium zakończenia
Komponenty komunikują się przez jawnie zabezpieczone kontrakty, sekrety nie są przechowywane w kodzie, a dane użytkownika mają kontrolowaną retencję.