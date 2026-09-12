# AUDYT 366 — AI_Offensive_MCP_Using_KaliLinux

## Status
Audyt wykonany. MCP bridge do Kali z 30 narzędziami i opcjonalnym persistent Metasploit layer.

## Ustalenia
Host bridge komunikuje się MCP/stdio i HTTP z Kali; repo zawiera patch serwera, launcher Waitress oraz integrację Metasploit RPC. README jawnie ostrzega, że API może wykonywać dowolne polecenia na hoście Kali.

## Klasyfikacja bezpieczeństwa
Tylko autoryzowane środowiska laboratoryjne/testowe. Nie rozszerzać funkcji ofensywnych.

## Plan prac
Zweryfikować auth, TLS, ACL/firewall, bind adresów, walidację poleceń, izolację procesu i ekspozycję Metasploit. Dodać deny-by-default, audyt zdarzeń i testy bezpieczeństwa.

## Kryterium zakończenia
Ścisła granica autoryzacji i sieci, brak niekontrolowanej ekspozycji API oraz kompletne logowanie/audyt działań.
