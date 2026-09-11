# Plan pracy — PaulaAI

## Stan audytu
- Audyt: ZAKOŃCZONY
- Typ: aplikacja Streamlit / szablon demonstracyjny GDP
- Priorytet: NISKI
- Gałąź: `main`

## Ustalenia
- README opisuje prosty dashboard GDP oparty na Streamlit.
- Instrukcja uruchomienia zakłada `requirements.txt` i `streamlit_app.py`.
- Nazwa repozytorium PaulaAI nie odpowiada deklarowanej funkcji GDP dashboardu, co wskazuje na prawdopodobne repozytorium odziedziczone/szablonowe albo niedokończony projekt.
- Brak podstaw do uznania projektu za aplikację Paula AI.

## Ryzyka
1. Niespójność nazwy, celu i implementacji.
2. Brak informacji o testach, danych, źródłach i wdrożeniu.
3. Potencjalne użycie nieaktualnego szablonu Streamlit.

## Kolejność prac
1. Zweryfikować zawartość repozytorium i historię projektu.
2. Ustalić, czy repo ma zostać przemianowane, przeznaczone do dashboardu danych, czy wykorzystane ponownie dla PaulaAI.
3. Dla dashboardu: dodać źródła danych, walidację, testy i CI.
4. Dla PaulaAI: rozpocząć osobny projekt zgodny z rzeczywistą architekturą agenta.
5. Ujednolicić README i polską dokumentację po ustaleniu celu.

## Kryterium zakończenia
Repozytorium ma jeden jednoznaczny cel, zgodną nazwę, aktualny kod i instrukcję uruchomienia; nie pozostaje w stanie „szablon o innej nazwie”.
