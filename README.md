# Zadanie

Należy napisać program pomagający w robieniu wykresów na laboratoria fizyczne.

Program powinien odczytywać plik, który zawiera dane obliczeniowe i jakieś metadate.
Na przykład może to być plik o postaci:

    Podpis osi $x$ [jednostka]
    Podpis osi $y$ [jednostka]
    0.0 0.1
    0.1 0.9
    0.2 2.2
    0.3 2.9
    0.4 4.0

Forma ta nie jest wymagana! Może to być np. plik JSON, YAML, CSV, albo arkusz Excela.

Należy napisać program, który:

1. Policzy współczynniki regresji liniowej *y* = *ax* + *b* wraz z **błędem współczynnika nachylenia**.
2. Zrobi elegancki wykres danych pomiarowych (punktowy) oraz dopasowania liniowego (liniowy), nadający się
   do bezpośredniego wstawienia do sprawozdania.
3. Wypisze wartość współczynnika nachylenia wraz z błędem.
4. BONUS: Program opcjonalnie na rykresie narysuje znaczniki błędów jeżeli są one podane w pliku
   (np. jako trzecia kolumna) albo jako metadane.
5. BONUS 2: Program potrafi dokonać przeszkrałcenia wprowadzonych wartości według zadanego wzoru
   (lub użyje dane bezpośrednio w przypadku braku takiego wzoru).
6. BONUS 3: Program ma prosty interfejs ułatwiający jego używanie.

Do regresji liniowej można użyć funkcji [`linreges` z pakietu `scipy`](https://docs.scipy.org/doc/scipy-0.14.0/reference/generated/scipy.stats.linregress.html). Zwraca ona współczynniki *a* i *b* jako `slope` i `intercept` oraz odchylenie standardowe współczynnika *a* jako `stderr`.
