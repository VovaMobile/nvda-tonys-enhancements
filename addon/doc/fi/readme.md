# Tonyn laajennukset #

* Tekijä: Tony Malykh
* Lataa [vakaa versio][1]
* Yhteensopivuus: NVDA 2022.4 ja 2023.1

Tämä lisäosa sisältää useita pieniä NVDA-ruudunlukijan parannuksia, jotka
ovat liian pieniä ansaitakseen erillisen lisäosan.

## Laajennetut taulukkonavigointikomennot

* NVDA+Ctrl+numero: Siirrä taulukon
  ensimmäiseen/toiseen/kolmanteen/... kymmenenteen sarakkeeseen.
* NVDA+Alt+numero: Siirrä taulukon
  ensimmäiselle/toiselle/kolmannelle/... kymmenennelle riville.

## Poistetut taulukkonavigointikomennot

Seuraavat taulukkonavigointikomennot on poistettu, koska ne sisältyvät
NVDA:n uusimpaan versioon.

* Siirrä taulukon ensimmäiseen/viimeiseen sarakkeeseen.
* Siirrä taulukon ensimmäiselle/viimeiselle riville.
* Lue taulukon tämänhetkinen sarake nykyisestä solusta alaspäin.
* Lue taulukon tämänhetkinen rivi nykyisestä solusta alaspäin.
* Lue taulukon tämänhetkinen sarake ylimmästä solusta alkaen.
* Lue taulukon tämänhetkinen rivi sen alusta lähtien.

Huom: Saat selville näiden ominaisuuksien oletusarvoiset
NVDA-näppäinkomennot NVDA:n käyttöoppaasta.

## Taulukoiden kopiointi leikepöydälle

Seuraavilla pikanäppäimillä voit kopioida muotoiltuna joko koko taulukon tai
nykyisen rivin/sarakkeen, jotta voit liittää sen taulukkona
rikastekstieditoreihin, kuten Microsoft Word tai WordPad.

* NVDA+Alt+T: Näyttää ponnahdusvalikon, jossa on vaihtoehdot taulukon tai
  sen osan kopioimiseen.

Taulukoiden, rivien, sarakkeiden ja solujen kopiointia varten on myös
erilliset komennot, mutta niille ei ole määritetty pikanäppäimiä. Ne on
mahdollista määrittää NVDA:n Näppäinkomennot-valintaikkunassa.

## Laajennetut sananavigointikomennot

Tämä toiminnallisuus on siirretty versiosta 1.8 lähtien
[Sananavigointi-lisäosaan](https://github.com/mltony/nvda-word-nav/).

## Automaattinen kielen vaihtaminen

Mahdollistaa puhesyntetisaattorin kielen vaihtamisen automaattisesti
merkistön perusteella. Kielten säännölliset lausekkeet voidaan määrittää
tämän lisäosan asetuksista. Varmista, että käyttämäsi syntetisaattori tukee
kaikkia niitä kieliä, joista olet kiinnostunut. Kahden latinalaista tai
samankaltaista merkistöä käyttävän kielen välillä vaihtaminen ei ole
toistaiseksi mahdollista.

## Pikahakukomennot

Voit määrittää enintään kolme säännöllistä lauseketta tekstin etsimiseen
muokattavista kentistä. Niiden pikanäppäimiksi on määritetty
oletusarvoisesti `Print Screen`, `Scroll Lock` ja `Pause`. Voit suorittaa
haun eteen- tai taaksepäin painamalla `Vaihto`-näppäintä yhdessä näiden
näppäinten kanssa.

## Estä häiritsevät NVDA:n "ei valittu" -ilmoitukset

Oletetaan, että sinulla on tekstiä valittuna tekstieditorissa, ja painat
sitten näppäintä, kuten Home tai Nuoli ylös, joka siirtää toiseen kohtaan
asiakirjassa. NVDA sanoo tällöin "ei valittu" ja sen jälkeen valittuna
olleen tekstin, mikä voi olla häiritsevää. Tämä toiminto estää NVDA:ta
puhumasta tällaisissa tilanteissa valittuna ollutta tekstiä.

## Dynaamiset näppäinkomennot

Voit määrittää tietyt näppäinpainallukset dynaamisiksi. Tällaisen
näppäinpainalluksen jälkeen NVDA tarkistaa aktiivisena olevan ikkunan
mahdollisten päivitysten varalta, ja jos rivi päivittyy, NVDA puhuu sen
automaattisesti. Esimerkiksi tietyt tekstieditorien näppäinpainallukset
tulee merkitä dynaamisiksi, kuten "siirry kirjanmerkkiin", "siirry toiselle
riville" ja virheenkorjausnäppäimet, kuten siirrä kohdalle/siirrä ohi.

Dynaamisten näppäinpainallusten taulukon muoto on yksinkertainen. Kukin rivi
sisältää säännön seuraavassa muodossa:
```
sovellus näppäinpainallus
```
jossa `sovellus` on sen sovelluksen nimi, jonka näppäinpainallus merkitään
dynaamiseksi (tai `*`, jolloin se merkitään dynaamiseksi kaikissa
sovelluksissa), ja `näppäinpainallus` on näppäinpainallus NVDA:n
ymmärtämässä muodossa, esim. `control+alt+shift+pagedown`.

Selvitä sovelluksen nimi seuraavasti:

1. Siirry sovellukseen.
2. Avaa NVDA:n Python-konsoli painamalla NVDA+Vaihto+Z.
3. Kirjoita `focus.appModule.appName` ja paina Enter.
4. Siirry tulostusruutuun painamalla F6 ja etsi viimeiseltä riviltä appNamen
   arvo.

## Ikkunoiden näyttäminen ja piilottaminen

Voit piilottaa nykyisen ikkunan ja näyttää kaikki tällä hetkellä
piilotettuina olevat ikkunat. Tästä saattaa olla hyötyä, jos käytät useita
ikkunoita samassa sovelluksessa (esim. Chromessa) ja haluat
uudelleenjärjestää ne.

* NVDA+Vaihto+-: Piilota nykyinen ikkuna.
* NVDA+Vaihto+=: Näytä kaikki tällä hetkellä piilotettuina olevat ikkunat.

Huom: Mikäli suljet NVDA:n, kun ikkuna on piilotettuna, sitä ei ole tällä
hetkellä mahdollista tuoda näkyviin NVDA:n uudelleenkäynnistyksen jälkeen.

## Konsolin parannukset

Tämä lisäosa sisälsi aiemmin useita konsoliin liittyviä
ominaisuuksia. Versiosta 1.8 lähtien ne on siirretty [Konsolin työkalupakki
-lisäosaan](https://github.com/mltony/nvda-console-toolkit/). Erityisesti:

* Reaaliaikainen konsolitulostus
* Reaaliaikainen konsolin tulostus, Anna äänimerkki konsolin päivittyessä,
  Pakota Ctrl+V konsoleissa
* Toteuta Ctrl+V konsoleissa

## Anna äänimerkki, kun NVDA on varattu

Valitse tämä vaihtoehto, jos haluat NVDA:n antavan äänipalautteen, kun se on
varattu. NVDA:n varattuna oleminen ei välttämättä tarkoita ongelmaa, vaan se
on merkki käyttäjälle siitä, että NVDA-komentoja ei käsitellä heti.

## Äänenvoimakkuuden säätö

* NVDA+Ctrl+Page up/Page down: säädä NVDA:n äänenvoimakkuutta.
* NVDA+Alt+Page up/Page down: Säädä kaikkien sovellusten paitsi NVDA:n
  äänenvoimakkuutta.

## Äänenjako

Äänenjakotilassa NVDA ohjaa kaiken äänitulosteen oikeaan kanavaan, kun taas
sovellukset toistavat ääntä vasemmassa kanavassa. Kanavia voidaan vaihtaa
tämän lisäosan asetuksissa.

* NVDA+Alt+S ottaa käyttöön äänenjakotilan tai poistaa sen käytöstä.

Huom: Sovelluksen äänituloste saatetaan rajoittaa tietyissä tilanteissa
yhteen kanavaan, vaikka NVDA ei ole käynnissä. Tätä voi tapahtua
esim. silloin, jos NVDA on kaatunut äänenjaon ollessa käytössä tai kun NVDA
sulkeutui puhtaasti kun kyseinen sovellus ei ollut
käynnissä. Uudelleenkäynnistä NVDA tällaisissa tilanteissa ja poista
äänenjako käytöstä, kun kyseinen sovellus on käynnissä.

## Laajennetut hiiritoiminnot

* Alt+Laskinnäppäimistön jakomerkki: Osoita hiirikohdistin nykyiseen
  objektiin ja napsauta sitä.
* Alt+Laskinnäppäimistön kertomerkki: Osoita hiirikohdistin nykyiseen
  objektiin ja napsauta siinä hiiren oikeaa näppäintä.
* Alt+Laskinnäppäimistön plus/Laskinnäppäimistön miinus: Osoita
  hiirikohdistin nykyiseen objektiin ja vieritä alas/ylös. Tästä on hyötyä
  jatkuvan vierityksen verkkosivuilla sekä sellaisissa, jotka lataavat lisää
  sisältöä vieritettäessä.
* Alt+Laskinnäppäimistön Del: Siirrä hiirikohdistin näytön vasempaan
  yläkulmaan. Tästä voi olla hyötyä, kun halutaan estää hiiren jääminen
  ikkunoiden päälle tietyissä sovelluksissa.


## Lisäystilan havaitseminen tekstieditoreissa

Jos tämä asetus on käytössä, NVDA antaa äänimerkin, kun se havaitsee
lisäystilan tekstieditoreissa.

## Estä kaksinkertainen Insert-näppäimen painallus

NVDA:ssa Insert-näppäimen painaminen kahdesti peräkkäin ottaa sovelluksissa
käyttöön lisäystilan. Joskus se kuitenkin tapahtuu vahingossa. Koska tämä on
erityinen näppäinpainallus, sitä ei voi poistaa käytöstä asetuksissa. Tämä
lisäosa tarjoaa tavan tämän pikanäppäimen estämiseen. Kun kaksinkertainen
Insertin painallus on estetty, lisäystila voidaan ottaa käyttöön painamalla
NVDA+F2 ja sitten Insert.

Tämä asetus ei ole oletusarvoisesti käytössä, ja se on otettava käyttöön
asetuksissa.

## NVDA-prosessin järjestelmäprioriteetti

Tämä mahdollistaa NVDA-prosessin järjestelmäprioriteetin lisäämisen, mikä
saattaa parantaa NVDA:n reagointia erityisesti suoritinta paljon
kuormitettaessa.

## Kohdistuksen jääminen jumiin tehtäväpalkkiin painettaessa Win+numero-pikanäppäintä

Windows 10:ssä ja mahdollisesti muissakin versioissa on bugi. Kun
sovellusten välillä siirrytään Win+numero-pikanäppäimellä, kohdistus jää
toisinaan jumiin tehtäväpalkkiin sen sijaan, että siirtäisi ikkunaan, johon
ollaan vaihtamassa. Koska tämän raportoiminen Microsoftille on toivotonta,
tähän lisäosaan on toteutettu kiertotie. Kun lisäosa havaitsee tämän
ongelman, se toistaa matalan äänimerkin ja korjaa ongelman automaattisesti.

[[!tag dev stable]]

[1]: https://www.nvaccess.org/addonStore/legacy?file=tonysEnhancements
