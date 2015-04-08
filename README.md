# AwesomeLabsManual

if you want install a clean Rails:

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
1. instalacja: 
  1. ```sudo apt-get install postgresql```
  2. ``sudo apt-get install libpq-dev postgresql```
2. Aby dodać użytkownika do bazy:
  1. przełaczanie usera postgresql: ```sudo su - postgres```
  2. tworzymy usera dla naszego projektu: ```createuser -d -P <name_user>```


Start SupportHub Project
---------------------------------
1. Go To https://help.github.com/articles/generating-ssh-keys/#platform-linux and do step 2 & 4 
  wygenerowanie certyfikatu i wgranie go na GitHub pozwala na połączenie komputera z kontem na GitHub
2. Install Git: ```sudo apt-get install git```
3. pobieramy kod: ```git clone git@github.com:AntiTyping/SupportHub.git```
4. ```cd SupportHub```
5. Install Gems: ```bundle install```
6. jeżeli mamy Postgresql dodajemu usera:
  1. ```sudo su - postgres```
  2. ```createuser -d -P supporthub```
7. Create user with password and change config/database.yml to contain this password. !Two places: development and test section)
8. Create databases: ```rake db:setup```
9. Seed the databases: ```rake db:seed```
10. Run the tests: ```rake```
11. all should be green
12. Start server: ```rails s```
13. Open browser: http://localhost:3000

AwesomeLabsManual
