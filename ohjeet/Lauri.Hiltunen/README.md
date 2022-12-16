# **Git ja GitHub** 


## _Versiohallinta_
> Git on versioidenhallitaan tarkoitettu ohjelma. Gitissä pystyy perumaan muutoksia, joka tekee gitistä hyvän ohjelman versioidenhallitsemiseen. Tietokoneen työhakemiston voi siirtää myös "github" nimiseen ohjelmaan, jossa hakemiston voi vaikka viedä toiselle tietokoneen helpommin.
> 
> [Gitbook](https://www.gitbook.com/)

![](18133.png)

***

## _Käytännölliset gitin komennot_

### git init
    * Tekee halutusta hakemistosta gitin hakemiston
### git branch
    * Näyttää gitin eri haarat ja sen joka on käytössä
    * Uuden branchin voi luoda git branch [nimi] komennolla
### git status
    * Näyttää tiedostot, joita ei ole commitoitu
### git remote
    * Linkittää git työkalun githubiin
    * Remoten teon voi vahvistaa "git remote -v" komennolla
### git add
    * Lisää tiedoston indeksiin
### git commit
    * Lisää indeksissä olevat tiedotot committiin
### git push
    * Siirtää git hakemistoon tehdyt muutokset tietokoneesta githubiin
### git fetch
    * Siirtää githubissa olevat muutokset tietokoneelle
### git log
    * Näyttää commitit
    * "git log --oneline" näyttää commitit peräkkäin ja yksittäinen committi on yhtenä rivinä.
### git reset
    * git reset [committi] peruuttaa kaikki commitit valitun commitin jälkeen
### git revert
    * luo uuden commitin, jossa versio on sama kuin commitissa, jonne halutaan peruuttaa
### git checkout
    * mahdollistaa gitin branchien välillä liikkumisen
### git merge
    * Yhdistää branchien commitit

***

## Gitin käyttö

Gitin hakemiston voi liittää githubiin, tekemällä githubiin hakemiston, jonka URL-osoite kopioidaan ja se liitetään git remote komentoon ja lähetetään komento. Tämän jälkeen laitataan vielä "git remote -v" komento. Git push siirtää tietoa githubiin ja git fetch hakee githubin version tiedosta.

| **Komento**   | **Toiminto**                          |                     
|---------------|---------------------------------------|
| git push      | Siirtää tiedot githubiin              |
| git fetch     | Siirtää githubin tiedot tietokoneelle |

Githubissa voi forkata muiden tekemiä hakemistoja menemällä forkattavan hakemiston tekijän profiiliin ja etsimällä oikean hakemiston ja painamalla nappia fork. Githubin repositorio voidaan kloonata käyttämällä komento "git clone [Githubin hakemiston URL] kansiossa, jonne haluaa kloonata sen repositorion.
Githubista forkattuun hakemistoon voidaan liittää monia remoteja. Joku näistä remoteista voi olla vaikka hakemiston tekijän githubiin ja toinen remote voi olla omaan github repositorioon.