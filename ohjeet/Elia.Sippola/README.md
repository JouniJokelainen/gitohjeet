Git ja Githubin toiminta ja käyttö
------

Git versionhallinnan toiminta ja käyttö, sekä GitHubin toimiminen.


## Git toiminta

Git on ilmainen tallennustapa/menetelmä jonka ideana on dokumentin tallentaminen monena versiona ilman suuria määriä ylimääräisiä tiedostoja. Se toimii luomalla tiedostolle versiohistorian, ja pitämällä kirjaa muutoksista jota tiedostoon on tehty. Sen avulla muutoksia pystyy pitämään kirjalla, ja peruuttamaan jos on tarve.

## GitHub toiminta

GitHub on myöskin ilmainen tietojen säilytyspaikka, joka toimii hyvin Git:in kanssa. GitHub tarjoaa esimerkiksi verisonhallinnalle ja ongelmien kirjaamiselle käytännöllisiä työkaluja. Git:iä käytetään yleensä GitHubin kaltaisten palveluiden yhteydeksi, sillä tiedostojen jakaminen ja varmuuskopioiminen on paljon helpompaa.

## Git käytön aloittaminen

Git:in käyttö kannattaa aloittaa asentamalla tarvittavat sovellukset ja kirjautumalla/rekisteröitymällä GitHubiin tai vastaavaan palveluun.

Git:iä ei ole mukava käyttää suoraan komentokehotteesta, joten suosittelen käyttämään *Visual Studio Codea* (VSCode). Sen voi asentaa [Tästä](https://code.visualstudio.com/download). VSCoden avulla voi kirjoittaa koodia helposti monella eri ohjelmointikielellä, ja sen lisäosiin kuuluu myöskin Git:n työkaluja.

Git ei ole windowsin oma työkalu, joten sitä todennäköisesti ei ole esiasennettu tietokoneelle automaattisesti. Git voidaan asentaa [tästä](https://git-scm.com/downloads)

> Linkistä löytyy Git:n setup. Seuraa setupin ohjeita. Setup asettaa oletukseksi ihan hyvät asetukset.
>
> Jos haluat käyttää VSCodea automaattisesti Git:n editorina, muista asettaa se kohdassa ***Choosing the default editor used by GIT***
> 
> Kohdassa ***Adjusting the name of the initial branch*** voidaan valita Git:n käyttämä oletus*branch* GitHub käyttää useimmiten nimeä **main**, joten sen asettaminen nyt saattaa helpottaa uusien kirjastojen *(repository)* luomisessa. Branch:in *"haaran"* nimeäminen voidaan tehdä myöskin myöhemmin, tai se voidaan jättää oletukseksi.
>
> **Kohdassa *Adjusting yous PATH enviroment* muista asentaa Git tietokoneen PATH ympäristöön. Sen avulla muut sovellukset voivat käyttää Git:n komentoja.** 
>
> Kohdassa *Configuring the terminal emulator to use with Git Bash* kannattaa valita *Use windows' default console* jos sinulla ei ole kokemusta MinTTY ympäristöstä.
>

### Git:n käyttäminen ensimmäistä kertaa

Kun käytät Git:iä ensimmäistä kertaa tietokoneella, sinun täytyy asettaa käyttäjänimi ja sähköposti järjestelmään. Git pitää kirjaa muutoksista, ja merkkaa näiden avulla kuka on tehnyt muutoksia milloinkin. Sähköpostin avulla sinut voidaan löytää jos jollain on sinulle asiaa. Käyttäjätunnus kannattaa olla tunnistettavissa. Se voi olla esimerkiksi GitHubin käyttäjänimi.

Käyttäjänimi asetetaan komennolla

    Git config --global user.name "erkkiEsimerkki"

Sähköposti taas komennolla

    Git config --global user.email "erkki.esimerkki@esi.merkki"
    
Jos sinulla on ongelmia Git:n komentojen kanssa, yritä lisätä komennon perään *--help*. Esim:

    Git --help
    
    #tai
    
    Git config --help

## Git:n kirjaston *(repository)* asettaminen terminaaliin

Kun haluat käyttää Git:iä, sinun tulee valita haluatko luoda kirjaston koneellesi vaiko suoraan GitHubiin. yleensä on helpompaa luoda ensin kirjasto GitHubissa, ja sitten kopioida se omalle tietokoneelle.

### kirjaston luominen Git:illä

Ensin avaa komentokehote (tai jokin muu terminaali) joko suoraan kohdekansiosta, tai liikkumalla ***cd*** komennon avulla

***cd*** komento toimii kirjoittamalla seuraavan alikansion nimen tai palaamalla takaisin *cd ..* komennolla.

    C:\Users\käyttäjä>cd documents
    
    C:\Users\käyttäjä\Documents> cd ..
    
    C:\Users\käyttäjä> cd \Users
    
    C:\Users> cd D:\
    
    # Olettaen sinulla on toinen levyasema
    
    D:\>

komennolla *dir* voit tarkistaa mitä kansioita ja tiedostoja kansiossa on

    dir

Komennolla mkdir voit luoda uuden kansion

    mkdir kansio
    
    #siirrytään kansioon
    
    cd kansio

Kun olet kansiossa johon haluat luoda kirjaston, kirjoita komento git init, komento luo versiohistorian kansioon, ja voit aloitta työskentelyn.

    git init
    
### Kirjaston luominen GitHubiin ja sen kopiointi

Githubin etusivulla, tai oikeasta yläkulmasta löytyvästä "+" valikosta löydät kohdan ***create new repository*** tai ***new repository***

Tämän jälkeen voit asettaa kirjastolle nimen ja asettaa sen julkiseksi tai yksityiseksi. Kirjstoille luodaan usein myöskin README.md tiedosto, jossa kerrotaan kirjaston tarkoituksesta ja tiedoista.

Kun olet luonut kirjaston, etsi sen osoite painamalla vihreää **<> code** näppäintä ja painamalla HTTPS kohtaa. jos kirjastossa ei ole tiedostoja, se löytyy kohdasta HTTPS suoraan etusivulta

-----

Kun olet löytänyt linkin, mene terminaalilla kansioon johon haluat kopioida kirjaston, tai avaa kansio VSCodella ja kirjoita terminaaliin komento

    git clone https://githubl.com/käyttäjä/kirjasto
    
Komento luo uuden kansion kirjaston nimellä

## Kirjaston yhdistäminen GitHubiin terminaalilla/komentokehotteella

Varmista että olet oikeassa kansiossa, git clone luo uuden kansion.

**Jos käytit git clone komentoa, kanio saattaa olla jo yhdistetty GitHubiin. Testaa käyttämällä git status komentoa**

    git status
    
    # tämä komento näyttää valmiit yhteydet
    
    git remote -v

Jos Kirjastosi on julkinen, voit käyttää *git remote add* komentoa joka lisää yhteyden kyseiseen kirjastoon.

    git remote add origin git@github.com:Käyttäjä/Kirjasto.git

Url on joko HTTPS tai SSH linkki jonka löydät vihreän "<> code" näppäimen alta tai suoraan etusivulta. Molemmat linkit toimivat.

## Git workflow eli käyttäminen terminaalilla/komentokehotteella

Varmista että olet oikeassa kansiossa *git status* kertoo jos kaikki on kunnossa.

Git toimii tallentamalla ja varmistamalla muutokset ennen kuin ne päivitetään kirjastoon.

![Git workflow](https://github.com/EliaSippola/Markdown/blob/main/workflow.png)

Jos kirjaston **main** haaraan on tullut muutoksia käytä komentoa *git fetch*. Ennen kuin aloitat tiedostojen muokkaamisen, kannattaa tarkistaa ettei päähaarassa ole muutoksia.

    git fetch
    
    git status
    
*Git fetch* komento katsoo onko valittuun haaraan tullut muutoksia, ja git status näyttää ne. Jos *git status* komento keroo päähaaran sisältävän muutoksia, kirjoita *git pull* jotta saat muutokset tietokoneellesi.

    git pull
    
    git status
    
Kun *git status* näyttää *Your branch is up to date* voit alkaa muokata tiedostoja.

------

Kun olet valmis tallentamaan ja lähettämään tiedot päähaaralle (main branch) tarkista ensin päähaaran tila uudelleen. Jos muutoksia on käytä *git pull* komentoa päivittääksesi omat tiedostosi (haarasi)

    git fetch
    
    git status
    
    # jos muutoksia on
    
    git pull

Jos kaikki on kunnossa lukuun ottamatta omia muutoksia käytä *git add* komentoa

    # kaikki tiedostot
    
    git add -A
    
    # yksi tiedosto
    
    git add tiedosto.txt
    
 Seuraavaksi kirjoita komento *git commit*
 
    git commit -a
    
    # tai
    
    git commit tiedosto.txt
    
Kun nyt käytät *git status* komentoa tulisi sen kertoa että haarasi on edellä päähaaraa.

Kaiken varalta voi vielä käyttää komentoa *git pull* jos siitä on jo aikaa kon olet viimeksi päivittänyt tiedostosi, ja sitten kirjoittaa *git push*

    git pull
    
    git push
    
*Git push* komento työntää kaikki *git commit* muutokset sille haaralle mihin olet yhteydessä.

Komennolla *git remote -v* voit tarkistaa mihin haaraan olet yhteydessä

## Git workflow VSCoden avulla

GitHubia pystyy myöskin käyttämään VSCoden Source Conrtol:in avulla. 

<img width="250" alt="image" src="https://user-images.githubusercontent.com/120164112/208076659-6350a69b-e995-4a0c-a45b-8962ec6af5e2.png">

VSCoden Source Control:in avulla ei tarvitse käyttää komentoja. Työkalu tarkistaa automaattisesti tiedostojen versiohistorian ja muutokset. 

Painamalla kiertäviä nuolia *"synchronize changes"* työkalu suorittaa komennot *git pull* ja *git push*

Kun olet valmis työntämään muutokset päähaaraan, kirjoita viesti ja paina commit kohtaa. Tämän jälkeen voit synkronoida muutokset serverille. Source Contro suorittaa aina *git pull* ja *git push* komennot. Jos haluat tehdä jomman kumman ilman toista paina kolmea pistettä oikeassa reunassa haaran vieressä ja Työkalu näyttää kaikki komennot erittäin.

## Muutoksien peruminen

Jos olet tehnyt muutoksia jotka haluat poistaa tai haluat palauttaa kaiken päähaaran tasolle, voit käyttää komentoa *git checkout*. Komennolla pystyy palauttamaan omieen tiedostojen muutokset päähaaran tasolle. -f pääte (--force) kertoo että komento suoritetaan pakolla.

    git checkout -f

Jos haluat perua muutoksen kirjoita komento *git revert HEAD"*. Komennolla voi myöskin perua tietyn muutoksen, tai tietyn verran muutoksia. Lisätietoja [tästä linkistä](https://git-scm.com/docs/git-revert)

    # peruuta edellinen muutos joka tehtiin
    
    git revert HEAD
    
Jos haluat pitää muutokset sen jälkeen, käytä ```git push```
   
Ero näillä kahdella on se, että *git checkout* peruu tilan päähaaran nykyiseen tilaan kun taas *git revert* peruu tilan päähaaralla edelliseen tilaan.

## Forkkaaminen eli toisen kirjaston kopioiminen

GitHubissa on helppoa kopioida ja käyttää muiden julkisia tiedostoja. Etsi kirjasto (repositary) jonka haluat kopioida ja paina kohtaa Fork. Tämä avaa ikkunan jossa voit kopioida kirjaston omalle käyttäjällesi.

Jos haluat antaa tekemäsi muutokset haaralle josta kopioit tiedot, paina kohtaa ***Pull Requests***, ja *New pull request*.

## Hyödyllisiä komentoja

Kaikki Git ympäristön komennot läytyvät [tästä linkistä](https://git-scm.com/docs).

Hyödyllisiä ovat esim:

    # haaran kopiointi
    git clone <url>
    
    # .git kansion luonti
    git init
    
    # haaran tilan tarkistaminen
    git status
    
    # haaran yhteyksien tarkistaminen
    git remote -v
    
    # päähaaran tarkistaminen muutosten varalta
    git fetch
    
    # päähaaran tietojen lataaminen
    git pull
    
    # yhteyden muodostaminen
    git remote add <nimi> <url>
    
    # muutoksien lisääminen odotustilaan
    git add <tiedosto>
    git add -A
    
    # tiedostojen varmistus
    git commit <tiedosto>
    git commit -a
    
    # tiedostojen työntäminen päähaaraan
    git push [<haara>]
    git push
    
    # haaran nimeäminen uudelleen
    git branch -m <vanha_nimi> <uusi_nimi>
    
    # yleisien asetusten muuttaminen
    git config <>
    
    # kansioissa liikkuminen
    cd <sijainti>
    
    # kansion tiedostojen listaaminen
    dir
    
    # kansion luonti
    mkdir <nimi>
