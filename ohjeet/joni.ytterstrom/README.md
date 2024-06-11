# Git Peruskäyttöohje

![Gitin ja GitHubin logot](https://github.com/jjlehto1337/gitohjeet/blob/main/ohjeet/joni.ytterstrom/gitjagithub.jpg)

## Johdanto
[**Git**](https://git-scm.com/) on hajautettu versionhallintajärjestelmä, josta on tullut käytännössä standardi ohjelmistokehitysprojekteissa, niin pienissä kuin suurissa. Git mahdollistaa tiedostojen muutosten seurannan, hallinnan ja versioinnin sekä yhteistyön ohjelmistokehittäjien kesken. Tiedostoihin tehtävät muutokset tallennetaan versioiksi (ns. “commit”), jolloin koodista muodostuu versiohistoria. Versiohistoria taas toimii varmuuskopiona, josta voi helposti tarvittaessa palauttaa vanhoja versioita.

[**GitHub**](https://github.com/) taas on palvelu, joka perustuu Git-versionhallintajärjestelmään ja tarjoaa käyttöliittymän Gitin toimintojen hallintaan. Kenties olennaisimpana ominaisuutena GitHubiin voi luoda aiemmin mainitsemiani etätietovarastoja (”remote repository”) projektista. Tämä mahdollistaa monien kehittäjien yhteistyön samassa projektissa, kun kehittäjät voivat ottaa omia kopioitaan tästä GitHubissa olevasta keskitetystä tietovarastosta ja myöhemmin taas liittää uudet tai muutetut koodinsa takaisin.

----

### Muutamia yleisesti käytettyjä komentoja

```git init``` - Git versiohallinnan ottaminen käyttöön työkansiossa

```git log``` tai ```git log --oneline``` - *Git commit:n* listaaminen

```git status```  *Git* tilan tarkastminen

```git fetch```  *GitHub* repositorion ja paikallisen työkansion tilenteen erojen päivittäminen





![Git:n toimintaa kuvaava kuva.](https://bytesofgigabytes.com/IMAGES/git/git%20commands/git%20commands.png)
*Git:n* toimintaa kuvaava kuva.
