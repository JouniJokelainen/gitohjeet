# Git ja GitHub ohjeet
<img src="https://i.imgur.com/JWb85dN.png" width="100" />

## Git
Git on versionhallinnan menetelmä, joka tarjoaa säilytyspaikan käytettävälle tiedolle ja pitää kirjaa tehdyistä muutoksista

## GitHub
GitHub mahdollistaa yhtäaikaisen työskentelyn saman tiedon kanssa usealta eri koneelta/käyttäjältä.
GitHub toimii myös työn varmuuskopiona versionhallinnan ohessa.


## Git peruskäyttö
Git:iä voidaan käyttää komentoriviltä ja tai kehitystyökalun (esim. Visual Studio Coden) kautta.

**Git järjestelmä koostuu kolmesta osasta:**
 - työkansio (working directory)
 - Git indeksi (staing area
 - paikallinen versiohallinta repositio .git hakemistossa (local .git)
   
**Git määrityskomentoja:**
- Git versiohallinnan ottaminen käyttöön työkansiossa: `git init`
- Git käyttäjänimen määrittäminen: `git config user.name "etunimi sukunimi"`
- sähköpostiosoitteen määrittäminen: `git config --global user.email "erkki.esimerkki@example.com"`
- Git tietojen näyttäminen: `git config --list --global`

**Git peruskomentoja:**
- tiedon lisääminen Git indeksiin: `git add b.txt tai git add`
- Commit:n luominen indeksissä olevista tiedoista: `git commit -m "Commit viesti"`
- Git commit:n listaaminen: `git log tai git log --oneline`
- Git tilan tarkastaminen: `git status`

## GitHub <-> Git työskentely:
**Työhakemiston synkronointi GitHub:iin:**
- Paikallisen työkansion kytkeminen GitHub repositorioon: `git remote add origin https://github.com/GitHubTunnus/GitHubRepositorio.git`
- etärepositorio kytköksen tarkistaminen: `git remote -v`
- paikallisen työkansion tietojen puskeminen GitHub:n: `git push -u origin master`

**GitHub:issa olevien tietojen synkronointi paikalliseen työkansioon:**
- GitHub repositorion ja paikallisen työkansion tilenteen erojen päivittäminen: `git fetch`
- Tietojen lataaminen GitHub repositoriosta paikalliseen työkansioon: `git pull`

**GitHub fork** on GitHub repositio, joka on syntynyt syntynyt fork -toiminnolla, jonkun toisen GitHub repositorista, joka sisältää kaikki samat tedot kuin alkuperäinen repositorio.

**Fork komentoja:**
- Upstream remoten lisääminen paikalliseen Git työhakemistoon: `git remote add upstream <git://github.com/GitHubTunnus>/GitHubRepositorio.git>`
- Upstream remoten tietojen synkronoiminen Giot työhakemistoon: `git fetch upstream`

**Branch eli haara** mahdollistaa tietojen muuttamisen ilman, että muutoksilla on vaikutusta työkansion muihin tietoihin.
Sitä voidaan käyttää sovelluksen erilaisten toiminnallisuuksien kehittämiseen ilman että kehitystyöllä on vaikutusta sovelluksen muun lähdekoodin toimintaan. Haarassa olevat tiedot yhdistetään lopulta sovelluksen päähaaran (master tai main) sisältämään lähdekoodiin.

**Branch komentoja:**
- Git haarojen listaaminen: `git branch`
- Uuden haaran lisääminen: `git branch haaran_nimi tai git checkout haaran_nimi`
- Haaran tietojen yhdistäminen master päähaaraan: `git merge haaran_nimi`
- Haaran poistaminen: `git branch -d uusibranch`
