# TÄRKEIMMÄT ASIAT

### Mikä Github on?
Github on palvelu jonka avulla voidaan julkaista, tehdä ja säilyttää projekteja.
Se on esimerkiksi koodaajille hyvä työkalu.

<img width="758" alt="github" src="https://user-images.githubusercontent.com/120164121/208043277-fef81bff-3710-42f2-91f8-560a5b38df92.png">


## Git perus komennot

> - `**git status**` on tiedostojen tilan tarkistaminen
> - `**git add**` on tiedon lisääminen
> - `**git commit**` on commitin tekeminen tiedostosta
> - `**git init**` on versionhallinnan
> - `**git push**` on tietojen puskeminen
> - `**git branch**` on haarojen listaaminen
[video komennoista](https://youtu.be/PSJ63LULKHA)

## Tavat perua muutoksia

> - git checkout on
> - git revert on turvallinen tapa perua muutokset
> - git reset on tapa perua muutokset

## Forkkaus

Toisen henkilön repositorion forkkaus onnistuu menemällä repositorioon ja
oikealla ylhäällä näkyy fork. Painamalla fork nappulaa ja sen jälkeen painamalla create fork.
 ## Muuta
- Paikallisen työkansion kytkeminen repositorioon onnistuu
  git remote add origin https://github.com/GitHubTunnus/GitHubRepositorio.git 
  
  ## Upstream
  
  - forkataan repositorio
  - cloonataan forkki paikalliseksi työkansioksi **git clone https://linkki_omaan_forkkiin.git**
  - Lisätään paikallisen työkansion upstream alkuperäiseen vieras repositorioon **git remote add upstream https://linkki_vieraaseen_repoon.git**
  - git remote -v
  - pullataan **git fetch upstream
git merge upstream/main**
  - muutoksia paikalliseen hakemistoon
  - commitoidaan muutokset
  - Työnnetään muutokset *git push*
  - ja sitten pull request
  
  
