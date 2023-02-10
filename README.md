# Football-Analysis - opis (PL)

Projekt analizy piłkarzy zakładał pobranie danych wybranych zawodników z ostatnich 3 sezonów i ustrukturyzowanie ich w odpowiedni sposób. Dane zostały przeniesione do Excela (załączony plik w formacie .xls) oraz przekonwertowane do formatu .csv, tak aby wczytać je w Pythonie poprzez Jupyter Notebook.
Projekt skupiał się na odpowiednim przetworzeniu danych, począwszy od wczytania ich w odpowiedniej formie (za pomocą biblioteki NumPy) oraz wczytanie pliku .csv jako tabeli głównej (za pomocą biblioteki Pandas).
Dane następnie odpowiednio przekonwertowane, tak aby wyciągnąć interesujące statystyki oraz zrobić porównania stylu gry zawodników. Projekt skupia się na takich umiejętnościach jak:
- wczytywanie i odpowiednia implementacja danych (tworzenie arrays, dataframes, tabel czy odpowiednich kolumn)
- manipulacja danymi z pomocą biblioteki Pandas (grupowanie danych, wyciąganie średnich, maksymalnych oraz minimalnych wyników z danych kolumn, wyciąganie z tabeli konkretnych, interesujących nas danych - np. danego wiersza)
- tworzenie dodatkowych kolumn do gotowej tabeli z nowymi obliczeniami
- tworzenie różnych form wykresów za pomocą bibliotek Matplotlib oraz Seaborn oraz dostosowywanie tych wykresów do potrzeb analizy
- tworzenie funkcji upraszczających tworzenie wielu wykresów
- wyciąganie wniosków z tworzonej analizy (opis poniżej)

# Football-Analysis - description (ENG)

The football Analysis project involved taking the data of selected players from the last 3 seasons and structuring it. The data was transferred to Excel (attached file in .xls format) and converted to .csv format to upload it to Python via Jupyter Notebook.
The project focused on processing the data properly, starting with loading it in the wanted form (using the NumPy library) and loading the .csv file as a main table (using the Pandas library).
The data then was converted accordingly, so as to pull out interesting statistics and make comparisons of players' playing styles. The project focuses on skills such as:
- loading and appropriate implementation of data (arrays, dataframe, tables creation)
- data manipulation with the help of the Pandas library (grouping the data, extracting average, maximum and minimum scores from given columns, extracting specific data of interest from the table)
- creation of additional columns to our main table with new calculations
- creation of various forms of charts using Matplotlib and Seaborn libraries
- customization of these charts for analysis purposes
- creating functions to simplify the creation of multiple charts
- drawing conclusions from the created analysis (description below)

# Analiza zawodników

Poniższa analiza podzielona jest na 4 części i dokonując jej, chce uzyskać odpowiedzi na poniższe pytania:
- jaka jest pozycja każdego analizowanego piłkarza (obrońca, rozgrywający, skrzydłowy, napastnik)?
- jaki jest najlepszy zawodnik na danej pozycji?
- najlepszy indywidualny sezon, czy da się określić największą gwiazdę ligi?
- kto miał najrówniejszą formę przez te 3 sezony?

<b> CZĘŚĆ 1 </b>

Na sam początek warto przyjrzeć się zawodnikiem, którzy regularnie zdobywają mniej niż 10 goli w sezonie.
![def_fwd](https://user-images.githubusercontent.com/111128309/218095610-6a6241b0-4b13-4445-911b-88efe4da244c.jpg)

Cancelo i Alexander-Arnold nie przekroczyli bariery 10 bramek w żadnym sezonie. Są to więc ewidentnie obrońcy. Następnie sprawdzamy kto regularnie strzela powyżej 17 bramek na sezon. Na tej podstawie możemy z całą pewnością stwierdzić, że Salah i Kane to napastnicy. Na liście po jednym razie przewinęli się też Mane, Son i Vardy, więc należy ich zbadać pod tym kątem. Najłatwiej sprawdzić statystykę wszystkich oddanych strzałów, w ten sposób widać jak blisko bramki przeciwnika gra dany piłkarz. 
-	Sadio Mane:
![Mane](https://user-images.githubusercontent.com/111128309/218096741-b4f735fa-3076-4521-9c07-4eac136d98f9.jpg)
![Mane2](https://user-images.githubusercontent.com/111128309/218096757-ac3cb211-4434-472f-a45b-4bebb0eefec5.jpg)

Mane dużo strzela, ale widzimy też, że bardzo dużo drybluje. Widzimy też, że z czasem zmniejsza się liczba jego dryblingów, a zwiększa liczba strzałów. Oznacza to, że jego styl prawdopodobnie lekko ewoluował. Z bycia początkowo typowym skzrydłowym, stał się zawodnikiem grającym bliżej środka. Jest on więc czymś pomiędzy skrzydłowym, a napastnikiem. Widać jednak, iż drybluje on, obok Zahy, najczęściej w lidze. Dlatego na potrzeby analizy przypiszemy mu pozycję skrzydłowego, ale sprawdzimy jak wypada też w porównaniu z typowymi napastnikami.
-	Jamie Vardy:
![Vardy](https://user-images.githubusercontent.com/111128309/218096773-f5a3a244-f955-4bf5-b0ab-da2c84203682.jpg)

Wdać, że Vardy potrafi strzelić dużo goli oddając mało strzałów. Oznacza to, że prawdopodobnie strzela z bardzo bliska, więc jego pozycja boiskowa to napastnik. Ponadto Vardy kreuje mało sytuacji, co umacnia nas w przekonaniu, że jest typem napastnika czekającego na podanie od kolegów z zespołu.
-	Son:
![Son](https://user-images.githubusercontent.com/111128309/218096842-f965925d-23ef-40e2-b625-bb51d9f992f4.jpg)
![Son2](https://user-images.githubusercontent.com/111128309/218096857-ef8ee21c-0cf2-451a-ab43-4f59395e11db.jpg)

Jest to bardzo ciekawy zawodnik, prawdopodobnie najcięższy do scharakteryzowania. Z całą pewnością nie oddaje on zbyt wielu strzałów, jednak potrafi strzelić sporo goli. Drybluje mniej od Mane, ale potrafi stowrzyć sporo sytuacji innym zawodnikom i ma dużo kluczowych podań. Prawdopodobnie jest on czymś między rozgrywającym, skrzydłowym, a napastnikiem. Na potrzeby analizy przypiszemy go do pozycji rozgrywającego, ale sprawdzimy też jak wypada w porównaniu ze skrzydłowymi.
-	Wilfried Zaha - jest to typowy skrzydłowy. Najwięcej dryblingów w całej lidze. Stała liczba tworzonych sytuacji oraz strzałów na sezon.
![Zaha](https://user-images.githubusercontent.com/111128309/218096906-da28f041-23e1-4665-bf3b-05a20489a591.jpg)

-	Kevin de Bruyne - jest to typowy rozgrywający. Najwięcej asyst, stworzony szans, kluczowych podań. Bezkonkurencyjny w tym względzie, mimo mniejszej liczby minut niż konkurencja.
![KdB](https://user-images.githubusercontent.com/111128309/218096876-d856e09e-ea0a-4d0d-9e81-26822a443379.jpg)

<b> CZĘŚĆ 2 </b>

Mamy więc pogrupowanych zawodników. Następnie spróbujemy scharakteryzować każdego piłkarza w większych szczegółach i wybrać najlepszego zawodnika na danej pozycji.
Obrońcy w zestawieniu to boczni obrońcy. Mają oni więcej statystyk ofensywnych od stoperów i to na tych statystykach skupiamy się w poniższej analizie. Po ilości asyst, tworzonych szans (dośrodkowania lub długie podania) i kluczowych podaniach, widać że Trent Alexander-Arnold jest bezkonkurencyjny dla Cancelo na przestrzeni 3 sezonów. Ciekawiej robi się porównując inne pozycje (analizowane statystyki ofensywne poniekąd to wymuszają), dlatego też zdecydowałem się dodać TAA do analizy rozgrywających (statystykami kreowania szans najbardziej przypomina taki profil gracza).

<i><b> de Bruyne vs Son (vs TAA) </i></b>

W tej części analizy pomijamy zdobycze bramkowe. W tej statystyce Alexander-Arnold jako obrońca nie ma szans z pozostałymi zawodnikami. Wyjątkowe są jednak jego umiejętności dokładnych podań i warto im się przyjrzeć.
![Playmakers](https://user-images.githubusercontent.com/111128309/218097429-c144dd2a-1c51-471d-b89c-b95efb0e2ce0.jpg)

<i><b> Zaha vs Sadio Mane (vs Son) </i></b>
![Wingers](https://user-images.githubusercontent.com/111128309/218105030-f32f35c9-3d24-4e53-80e7-491452c39880.jpg)


<i><b> Salah vs Kane vs Vardy (vs Mane) </i></b>
![Forwards](https://user-images.githubusercontent.com/111128309/218105069-c5e94b9b-e29b-46ff-95a7-0e882944dc23.jpg)

<b> CZĘŚĆ 3 </b>

.

Źródła danych/data source:

https://www.kickest.it/en/premier-league/stats
, transfermakt.pl
