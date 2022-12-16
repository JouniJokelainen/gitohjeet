![Git ja GitHub](/gitjagithub.jpg)


------------------

# Mitä versiohallinnalla tarkoitetaan?
Versionhallinnalla tarkoittaa menetelmää, joka säilöö tietoa ja siihen tehtyjä muutoksia.

Sen käyttöön on pääsääntöisesti kaksi syytä: 
1. Versionhallinta mahdollistaa tiedon varmuuskopioinnin. Varmuuskopiot (*commitit*) sisältävät sekä tiedon nykyisen, että aikaisemman tilan.  
2. Versiohallinta (*GitHub:n* kautta) mahdollistaa tiedon jakamisen muille, sekä osallistumisen muiden projekteihin.


## Mikä [Git](https://git-scm.com) on?

Git on hajautetun versiohallinnan menetelmä jossa ideana on tarjota säilytyspaikka käytettävälle tiedolle ja pitää kirjaa tietoon tehdyistä muutoksista. Ohjelmistotyössä versiohallinnan käyttäminen yhteistyöskentelyyn ja muutosten jäljittämiseen on normi. Alunperin Git:n on kehittänyt suomalainen [Linus Thorvalds](https://fi.wikipedia.org/wiki/Linus_Torvalds).

### Mikä [GitHub](https://github.com/) on?

*GitHub* mahdollistaa myös saman tiedon parissa työskentelyn eri tietokoneilta. Saman tiedon parissa työskennellään kuitenkin usein eri tietokoneilta (mikroluokka, kotikone, jne.).

Toisaalta versiohallinta toimii myös varmuuskopiona työllesi. Näin tieto ei häviä, vaikka tietokoneesi hajoaisi.

*GitHub* (ja myös [GitLab](https://about.gitlab.com/)) ovat palveluita, joissa voidaan pitää Git-muotoisia varastoja (*Repository*). Ne mahdollistavat tiedon jakamisen muille saman tiedon parissa työskenteleville henkilöille. *GitHub*:a olevia repositorio joka on kytketty paikalliseen Git työkansioon on ns. *remote*. *Remote* taas puolestaan tunnetaan Git komennoissa nimellä *Origin*, tosin nimi on vaihdettavissa.  

---------------

### Git:n peruskäyttö

Git:ä voidaan käyttää jokoa Git komentoriviltä tai suoraan kehitystyökalun (esim. Visual Studio Code) kautta. On hyvä tietää Git komentorivin peruskomennot vaikka jatkossa Git:ä käyttäisikin kehitystyökalun avulla. Näin Git toiminnallisuudet sisäistää paremmin.

Git järjestelmänä koostuu kolmesta osasta  
1. Työkansio tietoineen (*working directory*)
2. Git indeksi (*staging area*)
3. Paikallinen versionhallinta repositorio .git hakemistossa (*local .git*)

![Git prosessi](https://uidaholib.github.io/get-git/images/workflow.png)

**Git työskentely:**

Git tietojen määrittäminen:
- Git versiohallinnan ottaminen käyttöön työkansiossa: ```git init```   
- Git käyttäjänimen määrittäminen: ```git config user.name "etunimi sukunimi"```   
- Sähköpostiosoitteen määrittäminen: ``` git config --global user.email "erkki.esimerkki@example.com" ```  
- Git tietojen näyttäminen: ```git config --list --global```    

Git työskentelyn peruskomentoja:
- Tiedon tuottaminen ja muokkaaminen Git työkansiossa   
- Tiedon lisääminen Git indeksiin: ```git add b.txt``` tai ```git add .```  
- *Commit:n* luominen indeksissä olevista tiedoista: ```git commit -m "Commit viesti"```   
- *Git commit:n* listaaminen: ```git log``` tai ```git log --oneline``` 
- *Git* tilan tarkastminen: ```git status```   

**Github <-> Git työskentely:**

Työhakemiston synkronoiminen *GitHub:n*:
- Paikallisen työkansion kytkeminen GitHub repositorioon:   
 ```git remote add origin https://github.com/GitHubTunnus/GitHubRepositorio.git```   
- Etärepositorio kytköksen tarkistaminen: ```git remote -v```   
- Paikallisen työkansion tietojen puskeminen *GitHub*:n:``` git push -u origin master```   

*GitHub*:a olevien tietojen synkronoiminen paikalliseen työkansioon:
- *GitHub* repositorion ja paikallisen työkansion tilenteen erojen päivittäminen: ```git fetch```  
- Tietojen lataaminen *GitHub* repositoriosta paikalliseen työkansioon: ``` git pull ```  

**GitHub* fork:**
Ns. *Fork* on *GitHub* repositorio joka syntynyt *fork* toiminnon takia kopiona jonkun toisen *GitHub* repositorista. *Fork* sisältää kaikki samat tiedot kuin alkuperäinen repositorio. *Fork*:n omistaa kopion luonut henkilö joten tietojen lisääminen *Fork* repositorioon on mahdollista.

Git *fork*:n liittyviä Git komentoja
- *Upstream remoten* lisääminen paikalliseen Git työhakemistoon:   
```git remote add upstream <git://github.com/GitHubTunnus>/GitHubRepositorio.git>```     
- *Upstream remoten* tietojen synkronoiminen Giot työhakemistoon: ```git fetch upstream```   

**Haarat eli *branch*:t**:

Git haara (*branch*) on toiminnallisuus joka mahdollistaa haarassa olevien tietojen muuttamisen ilman että muutoksilla on vaikutusta työkansion muihin tietoihin. Haaraa voitaisiin käyttää sovelluksen erilaisten toiminnallisuuksien kehittämiseen ilman että kehitystyöllä on vaikutusta sovelluksen muun lähdekoodin toimintaan. Haarassa olevat tiedot yhdistetään lopulta sovelluksen päähaaran (*master* tai *main*) sisältämään lähdekoodiin. 

Git haaroihin liittyvä työskentely:
- Git haarojen listaaminen: ```git branch```    
- Uuden haaran lisääminen: ```git branch haaran_nimi``` tai ```git checkout haaran_nimi```   
- Haaran tietojen yhdistäminen *master* päähaaraan: ```git merge haaran_nimi```   
- Haaran poistaminen: ```git branch -d uusibranch```

--------------------

### Git ja GitHub toiminta yleisellä tasolla

![Gitin peruskäyttö](https://gitlab.jyu.fi/tie/ohj2/esimerkit/k2020/raw/master/luennot/luento02/git.png)

------------------

Linus Thorvalds
>"*Kun Microsoft alkaa tehdä ohjelmia Linuxille, se tarkoittaa että minä olen voittanut.*"
