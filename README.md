# football-trip-planner

1. Dlaczego nie pracujemy bezpośrednio na main?
Używamy maina aby uniknąć sytuacji, że strona przestanie działać przez wprowadzone zmiany lub błędy w kodzie, chcemy mieć jedną stabilną wersję projektu, do której wprowadzamy dane po przeanalizowaniu ich kiedy są na gałęzi develop. Nie pracując wyłącznie na main można lepiej kontrolować zmiany, kto co robi i dzięki temu też nie będzie chaosu w zespole.

2. Co by się stało, gdyby każdy commitował na main?
Wtedy strona mogłaby bardzo często nie działać przez niesprawdzone zmiany i błędy w kodzie oraz chaos w zespole, gdzie każdy nie do końca by wiedział co robi inna osoba, więc też nie będzie wiadomo kto wprowadził dany błąd.

3. Czym jest projekt?
Projekt jest planerem wycieczek, który wspiera decyzje biznesowe. Aplikacja ma znaleźć wszystkie mecze w danym mieście w określonym czasie, sprawdzić pełny sezon wybranego klubu, wygenerować plan wyjazdu (mecz + miasto + atrakcja) i oceniać które wyjazdy mają potencjał produktowy.

4. Jak go uruchomić?
Trzeba włączyć cmd i za pomocą change directory zmienić folder na ten, w którym znajduje się projekt. Następie, kiedy jesteśmy w dobrym folderze trzeba napisać komendę "dotnet run", aby ruchomić program.

5. Główne sekcje seed.json
   *cities:
     - id
     - name (nazwa miasta)
     - country (nazwa kraju, w którym znajduje się miasto)
   *matches:
     - id
     - homeTeam (nazwa klubu gospodarzy spotkania)
     - awayTeam (nazwa klubu gości spotkania)
     - kickoffUtc (data i godzina rozpoczęcia meczu)
     - cityId (miasto klubu gospodarzy zdefiniowane przez cityId)
   *attractions: 
     - id
     - cityId (miasto zdefiniowane przez cityId)
     - name (nazwa atrakcji)
     - description (opis atrakcji)

6. Jak są ze sobą powiązane?
Matches i attractions są powiązane do cities przez pole cityId. Dzięki temu możemy zobaczyć gdzie znajduje się dany mecz i jakie atrakcje bedą w tym mieście. 
