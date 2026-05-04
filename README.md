*Aplikacja stylizowana jest pod biblioteke stramlit poniewaz na poczatku robilem w niej jednak wazy ona 500MB co zmusilo mnie na przepisanie jej do Flaska*

*Zgodnie z ustaleniem dla osob ktore chcicaly pokazac prace na zajeciach wstrzymalem sie od dodania komentarzy do pliku Dockerfile*

*w pliku zadanie1.md narazie znajduje sie kopia README zostanie to rozdzielone po zrobieniu zadania nieobowiazkowego*

### Krotki opis decyzji w dockerfile:

* Rozdzielone zostal etap instalacji od etapu uruchamiajacego by finalny obraz nie zawierał zbednych narzędzi takich jak np pip czy pliki tymczasowe zmniejszylo mi to obraz kocowy o ok 20 MB
* Dla optymalizacji cachu instrukcje znajduja sie przed kopiowaniem reszty kodu, co przyspiesza przebudowywanie obrazu przy zmianach w samym kodzie


### Należy podać polecenia niezbędne do:
a. zbudowania opracowanego obrazu kontenera,


`docker build -t zad1pogoda:1.6 .`

b. uruchomienia kontenera na podstawie zbudowanego obrazu,

API KEY ze wzgledow bezpieczenstwa podany zostal na moodlu

`docker run -d -p 8501:8501 -e API_KEY="" --name *nazwa* pejas/zad1pogoda:latest`

c. sposobu uzyskania informacji z logów, które wygenerowałą opracowana aplikacja podczas
uruchamiana kontenera (patrz: punkt 1a),

`docker logs *nazwa*`

d. sprawdzenia, ile warstw posiada zbudowany obraz oraz jaki jest rozmiar obrazu.

sprawdzanie liczby warstw

`docker history pejas/zad1pogoda`

Sprawdzenie całkowitego rozmiaru obrazu

`docker images pejas/zad1pogoda`
