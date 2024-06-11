# Git ja Github ohjeet

## Git käyttöönotto

kun käytät Git:iä ensimmäistä kertaa tietokoneella, sinun täytyy asettaa käyttäjänimi ja sähköposti järjestelmään.
Git pitää kirjaa muutoksista, ja merkkaa näiden avulla kuka on tehnyt muutoksia milloinkin.
Käyttäjänimi asetetaan komennolla

Git config --global user.name "etunimi.sukunimi"

Sähköposti taas komennolla

Git config --global user.email "etunimi.sukunimi(at)esimerkki.com"

## Git:n kirjaston (repository) asettaminen

Kun haluat käyttää Git:iä, sinun tulee valita haluatko luoda kirjaston koneellesi vaiko suoraan GitHubiin.
Yleensä on helpompaa luoda ensin kirjasto GitHubissa, ja sitten kopioida se omalle tietokoneelle.

## kirjaston luominen Git:illä

Ensin avaa komentokehote (tai jokin muu terminaali) joko suoraan kohdekansiosta, tai liikkumalla cd komennon avulla

cd komento toimii kirjoittamalla seuraavan alikansion nimen tai palaamalla takaisin cd .. komennolla.

C:\Users\käyttäjä>cd documents

C:\Users\käyttäjä\Documents> cd ..

C:\Users\käyttäjä> cd \Users

C:\Users> cd D:\

## Olettaen sinulla on toinen levyasema

D:\>
komennolla dir voit tarkistaa mitä kansioita ja tiedostoja kansiossa on

dir
Komennolla mkdir voit luoda uuden kansion

mkdir kansio

## siirrytään kansioon

cd kansio
Kun olet kansiossa johon haluat luoda kirjaston, kirjoita komento git init, komento luo versiohistorian kansioon, ja voit aloitta työskentelyn.

git init

## Kirjaston yhdistäminen GitHubiin terminaalilla/komentokehotteella

Jos käytit git clone komentoa, kanio saattaa olla jo yhdistetty GitHubiin. Testaa käyttämällä git status komentoa

git status

## tämä komento näyttää valmiit yhteydet

git remote -v
Jos Kirjastosi on julkinen, voit käyttää git remote add komentoa joka lisää yhteyden kyseiseen kirjastoon.

git remote add origin github.com:Käyttäjä/Kirjasto.git
Url on joko HTTPS tai SSH linkki jonka löydät vihreän "<> code" näppäimen alta tai suoraan etusivulta. Molemmat linkit toimivat.

## Git workflow eli käyttäminen

## Haarojen (Branches) Käyttö

## Luo uusi haara

git branch haara-nimi

## vaihda haaraan

git checkout haara-nimi

## luo ja vaihda yhdellä komennolla

git checkout -b haara-nimi

## yhdistä pää haaraan

git checkout main , git merge haara-nimi

## poista haara

git branch -d haara-nimi

## Hyödyllisiä komentoja

### git historian tarkastelu

git log

### yksinkertainen historia

git log --online --decorate --graph --all

### näyttää committien erot

git diff

### tiedoston palautus aijempaan tilaan

git checkout -- tiedostonimi

## Forkkaaminen

## Forkin tekeminen

Etsi repositorio, jonka haluat forkata.
Klikkaa "Fork"-painiketta repositorion oikeassa yläkulmassa.
Tämä kopioi repositorion omaan GitHub-tiliisi.

## Forkantun repositorion kloonaaminen paikallisesti

Mene omaan GitHub-profiiliisi ja löydä forkattu repositorio.

## Kopioi kloonaus-URL

Klikkaa "Code"-painiketta ja kopioi HTTPS-URL.
Avaa terminaali ja suorita: git clone [def]
cd forkatun-repon-nimi

## pull reguestin teko

Mene GitHubiin ja siirry repositorion sivulle.

Valitse "Pull requests" -välilehti ja klikkaa "New pull request".

Vertaa haaroja:

Perushaara: main
Vertailuhaara: uusi-haara
Tarkista ja klikkaa "Create pull request".

Lisää otsikko ja kuvaus ja klikkaa uudelleen "Create pull request" vahvistaaksesi.

Yhdistä muutokset:

Klikkaa "Merge pull request" ja sitten "Confirm merge".
Poista haara:

Klikkaa "Delete branch" yhdistämisen jälkeen.

[def]: https://github.com/kayttajanimi/forkatun-repon-nimi.git
