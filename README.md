# AwesomeLabsManual

if you wont a clean Rails install:

LINUX
----

Instalacja Ruby on Rails
---------------------------------

1. Install RVM, Ruby w wersji 2.1.5, Rails
  1.  ```gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3```
  2.  ```\curl -sSL https://get.rvm.io | bash -s stable --ruby=2.1.5 --rails```
  3.  możliwe że trzeba zainstalować wczesniej curl: ```sudo apt-get install curl```
2. Restart terminala!
3. Dodajemy patch do Ruby (by mieć możliwość wywołania komendy ‘ruby’ z lini poleceń: ```source $(rvm 2.1.5 do rvm env --path)```
4. sprawdzamy czy wszystko działa:
  1. ```ruby -v (wersja ruby)```
  2. ```rails -v (wersja rails)
5. tworzymy katalog roboczy: ```mkdir ~/workspace```
6. przechodzimy do katalogu: ```cd ~/workspace```
7. tworzymy nowy projekt: ```rails new nazwa_projektu```
8. przechodzimy do katalogu: ```cd ~/workspace/nazwa_projektu```
9. sprawdzamy czy wszystko ok: ```rake```
  1. jeżeli jest ok, nie otrzymamy żadnego komunikatu
  2. jeżeli jest problem: “Could not find a JavaScript runtime?” to instalujemy JS: ```sudo apt-get install nodejs```
10. uruchamiamy serwer: ```rails s```
11. sprawdzamy w przeglądarce: http://localhost:3000

Instalacja Bazy Danych Postgresql
------------------------------------------
1. instalacja: ```sudo apt-get install postgresql```
2. Aby dodać użytkownika do bazy:
  1. przełaczanie usera postgresql: ```sudo su - postgres```
  2. tworzymy usera dla naszego projektu: ```createuser -d -P <name_user>```


AwesomeLabsManual
