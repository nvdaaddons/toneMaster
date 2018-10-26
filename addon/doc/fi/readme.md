# Tone Master #

* Tekijä: Hrvoje Katić
* Lataa [vakaa versio][1]

Tervetuloa Tone Masteriin! Tein tämän lisäosan vain huvin vuoksi, mutta myös
sinua varten, jotta voit pitää hauskaa käyttäessäsi sitä.

Olen aina halunnut luoda sävelmiä NVDA:lla sen sijaan, että kuuntelisin sen
edistymispalkkeja ilmaisevia ja virhetilanteista kertovia äänimerkkejä. Se
ei kuitenkaan ole kovin helppoa, joten halusin ensin tehdä siitä
helpompaa. Siksi tein Tone Masterin. Kuvittele, millaista olisi kuulla
NVDA:n soittavan Mozzartin tai Beethovenin kappaletta, tai ehkä Rolling
Stonesin suurimpia hittejä. Vaikka lopputulos kuulostaakin vanhojen
kännyköiden soittoääneltä, se voi olla siitä huolimatta hauskaa.

Tone Master yksinkertaistaa sävelsarjojen toistamista säveldatatiedostoja
käyttäen. Voit muokata näitä tiedostoja suosikkitekstieditorillasi ja
tallentaa sitten NVDA:lla toistettavaksi. Jatka lukemista saadaksesi
ohjeita!

## Säveldatatiedostot

Ennen kuin voit soittaa Tone Masterilla ensimmäisen sävellyksesi, sinun on
ensin luotava ja ladattava säveldatatiedosto. Säveldatatiedostot ovat
yksinkertaisesti .tdf-tarkenteisia tekstitiedostoja. Tone Master käyttää
niitä sävelsarjojen käsittelyyn ja toistamiseen. Luo säveldatatiedosto
seuraamalla alla olevia yksinkertaisia ohjeita.

1. Jokaisen .tdf-tiedoston rivin *täytyy* sisältää kolme kaksoispisteellä
   (:) eroteltua parametria. Ensimmäinen on sävelkorkeus, toinen on kesto ja
   kolmas on sävelten välissä olevan hiljaisuuden määrä. Kaikki kolme
   parametria on määritettävä, tai muuten Tone Master ei pysty toistamaan
   säveldataa.
2. Sävelkorkeus- ja kestoparametrit  on määritettävä positiivisina
   kokonaislukuina ja hiljaisuus liukulukuna.
3. Rivin alussa oleva risuaitamerkki (#) käsitellään kommenttina, jonka Tone
   Master ohittaa.

Esimerkki: Soita kolmen sävelen sarja

1500:100:0.5

1000:100:0.09

500:100:0.7

Tässä esimerkissä ensimmäisen sävelen korkeus on  1500, kesto 100 ja
hiljaisuus 0.5. Toisen korkeus on 1000, kesto 100 ja hiljaisuus
0.09. Viimeisen sävelen korkeus on 500, kesto 100 ja hiljaisuus 0.7.

Huom: Hiljaisuusparametri on määritettävä, vaikka saattaakin vaikuttaa
siltä, ettei sitä tarvita. Jos hiljaisuutta ei määritetä, NVDA korvaa
edellisen sävelen seuraavalla, jolloin lopputulos on odottamaton.

Voit tutustua tarkemmin säveldatatiedostojen syntaksiin tarkastelemalla ja
muokkaamalla tämän lisäosan mukana toimitettua esimerkkitiedostoa. Se löytyy
"tones"-alikansiosta, jossa myös kaikkien luomiesi .tdf-tiedostojen on
oltava.

## Pikanäppäimet

* Alt+NVDA+T: Toistaa ladatun säveldatatiedoston, mikäli sen syntaksi on
  kunnossa.
* Alt+Shift+NVDA+T: Pysäyttää ladatun säveldatatiedoston toiston, mikäli
  toisto on käynnissä.
* Alt+NVDA+N: Luo uuden, tyhjän säveldatatiedoston ja avaa sen Muistiossa
  muokattavaksi.
* Alt+NVDA+L: Avaa valintaikkunan, josta voit valita jonkin käytettävissä
  olevista säveldatatiedostoistasi ladattavaksi toistamista varten.
* Alt+NVDA+E: Avaa ladatun säveldatatiedoston Muistiosssa muokattavaksi.
* Alt+NVDA+O: Avaa säveldatatiedostojen kansion, jonne myös itse luodut
  tiedostot on tallennettava, jotta Tone Master löytää ne.

## Muita huomautuksia

Voit luoda, muokata ja ladata säveldatatiedostoja tai avata  tones-kansion
myös menemällä NVDA-valikkoon, valitsemalla Työkalut ja avaamalla Tone
Master -alavalikon.

Kun uuden säveldatatiedoston luomisen valintaikkuna näytetään, kirjoita
tiedostonimi ilman .tdf-päätettä. Tone Master lisää sen
automaattisesti. Mikäli nimeä ei määritetä, käytetään oletusnimeä
"untitled.tdf". Uusi tiedosto luodaan ja ladataan sekä avataan Muistiossa
muokattavaksi. Peruuta tiedoston luominen painamalla tiedostonimikehotteessa
Esc-näppäintä.

Huom: Tone Master käyttää Muistiota säveldatatiedostojen muokkaamiseen,
koska se tulee oletuksena Windowsin mukana, joten sen pitäisi olla
käytettävissä kaikilla tietokoneilla.

Kun säveldatatiedoston luomisen valintaikkuna on avoinna, valitse ladattava
tiedosto nuolinäppäimillä ja paina sitten Enteriä. Peruuta lataaminen
painamalla Esciä.

Voit ladata .tdf-tiedostoja tekstieditorissasi tarkasteltavaksi ja
muokattavaksi avattuasi niitä sisältävän kansion. Jotta kuulisit
lopputuloksen lennossa, on kuitenkin erittäin suositeltavaa ladata tiedosto
ensin Tone Masteriin, mikäli mahdollista. Tämän jälkeen voit muokata
tiedostoa, tallentaa edistymisesi ja käyttää jokaisen tallennuksen jälkeen
toista-komentoa kuullaksesi lopputuloksen.

## Muutokset versiossa 1.3

* Korjattu: Yhteensopivuusongelma uudempien NVDA-versioiden kanssa.

## Muutokset versiossa 1.2

* Korjattu: Huomattava ongelma, jossa tyhjän säveldatatiedoston
  valitsemisesta ja sitten toisen tiedoston valitsemisesta ja toiston
  yrittämisestä on seurauksena se, ettei säveldataa toisteta.

## Muutokset versiossa 1.1

* Lisätty: Vaihtoehto uuden säveldatatiedoston luomiseen sekä Muistiossa
  avaamiseen ja muokkaamiseen.
* Lisätty: Vaihtoehto nykyisen ladatun säveldatatiedoston muokkaamiseen
  Muistiossa.
* Parannus: Virheilmoitukset ovat nyt käyttäjäystävällisempiä.
* Parannus: Ttietyt lisäosan ominaisuudet, kuten tones-kansion avaaminen tai
  säveldatatiedostojen muokkaaminen Muistiossa, estetään nyt suojatuissa
  ruuduissa.
* Parannus: Käyttäjälle ilmoitetaan, jos säveldatan toisto on pysäytetty.
* Korjattu: Säveldatan toisto estetään, jos toisen tiedoston toisto on
  käynnissä.

## Muutokset versiossa 1.0

* Ensimmäinen versio.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
