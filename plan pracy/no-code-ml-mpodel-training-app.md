# Plan pracy — no-code-ml-mpodel-training-app

## Status audytu
AUDYT ZAKOŃCZONY — repozytorium #41 w bieżącym przebiegu.

## Stan faktyczny
Minimalna aplikacja Streamlit do treningu modeli ML bez kodowania. README jest jednozdaniowe. Repozytorium zawiera `src/`, `data/`, `trained_model/` oraz `requirements.txt`.

Zależności są przypięte: Streamlit 1.32.2, streamlit-option-menu 0.3.12, openpyxl 3.1.2, scikit-learn 1.4.1.post1 i XGBoost 2.0.3.

## Ocena
Projekt ma realną strukturę aplikacji, ale dokumentacja i automatyzacja są bardzo słabe. Bez inspekcji zawartości `src/` nie należy zakładać, jakie algorytmy, formaty danych ani ścieżki inferencji są faktycznie obsługiwane.

## Kolejność prac
1. Zmapować `src/` i ustalić entrypoint Streamlit.
2. Zweryfikować formaty wejściowe, pipeline preprocessingu, trening, zapis i ładowanie modeli.
3. Dodać testy jednostkowe dla transformacji i treningu oraz test smoke UI.
4. Dodać walidację danych, limity zasobów i bezpieczne ścieżki plikowe.
5. Uporządkować wersjonowanie modeli i artefaktów `trained_model/`.
6. Dodać CI: lint, testy i minimalny smoke build.
7. Rozbudować README i wykonać polonizację.

## Kryterium zakończenia
Udokumentowany entrypoint, reprodukowalny trening na danych testowych, testy pipeline oraz jednoznaczny format artefaktu modelu.
