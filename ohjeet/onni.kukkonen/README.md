![image](https://user-images.githubusercontent.com/120706372/208055579-cc7d1220-06c2-419a-bb1c-47d30bf7bde4.png)



------------------

## Versionhallinta?
Versionhallinnalla tarkoittaa menetelmää, joka säilöö tietoa ja siihen tehtyjä muutoksia.

Versionhallinta on hyödyllinen jos moni ihminen aikoo työstää samaa projektia, tai jos teet avoimen lähdekoodin projektia. 


## [Git](https://git-scm.com)?

Git on hajautetun versiohallinnan menetelmä jossa ideana on tarjota säilytyspaikka käytettävälle tiedolle ja pitää kirjaa tietoon tehdyistä muutoksista. Ohjelmistotyössä versiohallinnan käyttäminen yhteistyöskentelyyn ja muutosten jäljittämiseen on normi. Alunperin Git:n on kehittänyt suomalainen [Linus Thorvalds](https://fi.wikipedia.org/wiki/Linus_Torvalds) linuxia varten.

## [GitHub](https://github.com/)?

*GitHub* on pilvipalvelu, joka toimii paikkana jonne Git voi varastoida tietoja. 

Versiohallinta toimii myös varmuuskopiona työllesi. Näin tieto ei häviä, vaikka tietokoneesi hajoaisi jos committaat muutokset usein.

---------------

## Git:n peruskäyttö

Git:ä voidaan käyttää jokoa Git komentoriviltä tai suoraan kehitystyökalun (esim. Visual Studio Code) kautta. On hyvä tietää Git komentorivin peruskomennot vaikka jatkossa Git:ä käyttäisikin kehitystyökalun avulla. Näin Gitin toiminnot sisäistää paremmin.

Git järjestelmänä koostuu kolmesta osasta  
1. Työkansio tietoineen (*working directory*)
2. Paikallinen versionhallinta, repositorio ja stagatut commitit .git hakemistossa (*local .git*)
4. Etäinen versionhallinta pilvessä tai omalla servulla

![image](https://user-images.githubusercontent.com/120706372/208055976-3f9d0ff4-d421-4dc7-973b-200db8e60d82.png)


### Git työskentely:

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

### Github <-> Git työskentely:

Työhakemiston synkronoiminen *GitHub:n*:
- Paikallisen työkansion kytkeminen GitHub repositorioon:   
 ```git remote add origin https://github.com/GitHubTunnus/GitHubRepositorio.git```   
- Etärepositorio kytköksen tarkistaminen: ```git remote -v```   
- Paikallisen työkansion tietojen puskeminen *GitHub*:n:``` git push -u origin master```   

*GitHub*:a olevien tietojen synkronoiminen paikalliseen työkansioon:
- *GitHub* repositorion ja paikallisen työkansion tilenteen erojen päivittäminen: ```git fetch```  
- Tietojen lataaminen *GitHub* repositoriosta paikalliseen työkansioon: ``` git pull ```  

### GitHub fork:
Ns. *Fork* on *GitHub* repositorio joka syntynyt *fork* toiminnon takia kopiona jonkun toisen *GitHub* repositorista. *Fork* sisältää kaikki samat tiedot kuin alkuperäinen repositorio. *Fork*:n omistaa kopion luonut henkilö joten tietojen lisääminen *Fork* repositorioon on mahdollista.

Git *fork*:n liittyviä Git komentoja
- *Upstream remoten* lisääminen paikalliseen Git työhakemistoon:   
```git remote add upstream <git://github.com/GitHubTunnus>/GitHubRepositorio.git>```     
- *Upstream remoten* tietojen synkronoiminen Giot työhakemistoon: ```git fetch upstream```   

### Haarat eli branch:t:

Git haara (*branch*) on toiminto, joka mahdollistaa haarassa olevien tietojen muuttamisen ilman että muutoksilla on vaikutusta työkansion muihin tietoihin. Haaraa voitaisiin käyttää sovelluksen erilaisten toiminnallisuuksien kehittämiseen ilman että kehitystyöllä on vaikutusta sovelluksen muun lähdekoodin toimintaan. Haarassa olevat tiedot yhdistetään lopulta sovelluksen päähaaran (*master* tai *main*) sisältämään lähdekoodiin. 

Git haaroihin liittyvä työskentely:
- Git haarojen listaaminen: ```git branch```    
- Uuden haaran lisääminen: ```git branch haaran_nimi``` tai ```git checkout haaran_nimi```   
- Haaran tietojen yhdistäminen *master* päähaaraan: ```git merge haaran_nimi```   
- Haaran poistaminen: ```git branch -d uusibranch```

------------------

Linus Thorvalds
>"*Kun Microsoft alkaa tehdä ohjelmia Linuxille, se tarkoittaa että minä olen voittanut.*"
