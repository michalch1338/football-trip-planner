# football-trip-planner

1. Dlaczego nie pracujemy bezpośrednio na main?
Używamy maina aby uniknąć sytuacji, że strona przestanie działać przez wprowadzone zmiany lub błędy w kodzie, chcemy mieć jedną stabilną wersję projektu, do której wprowadzamy dane po przeanalizowaniu ich kiedy są na gałęzi develop. Nie pracując wyłącznie na main można lepiej kontrolować zmiany, kto co robi i dzięki temu też nie będzie chaosu w zespole.

2. Co by się stało, gdyby każdy commitował na main?
Wtedy strona mogłaby bardzo często nie działać przez niesprawdzone zmiany i błędy w kodzie oraz chaos w zespole, gdzie każdy nie do końca by wiedział co robi inna osoba, więc też nie będzie wiadomo kto wprowadził dany błąd.
