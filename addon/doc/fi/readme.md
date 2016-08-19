# Tone Master #

* Tekijä: Hrvoje Katić
* Lataa [vakaa versio][1]

Tervetuloa Tone Masteriin! Tein tämän pienen lisäosan vain huvin vuoksi,
mutta myös sinua varten, jotta voit pitää hauskaa käyttäessäsi sitä.

Olen aina halunnut luoda sävelmiä NVDA:lla sen sijaan, että kuuntelisin sen
edistymispalkkeja ilmaisevia ja virhetilanteista kertovia äänimerkkejä. Se
ei kuitenkaan ole kovin helppoa, joten halusin ensin tehdä siitä
helpompaa. Siksi tein Tone Masterin. Kuvittele vain, millaista olisi kuulla
NVDA:n soittavan Mozzartin tai Beethovenin kappaletta, tai ehkä Rolling
Stonesin suurimpia hittejä. Vaikka lopputulos kuulostaakin vanhojen
kännyköiden soittoääniltä, se voi olla siitä huolimatta hauskaa.

Tone Master yksinkertaistaa sävelsarjojen toistamista säveldatatiedostoja
käyttäen. Voit muokata näitä tiedostoja suosikkitekstieditorillasi ja
tallentaa sitten NVDA:lla toistettavaksi. Jatka lukemista saadaksesi
ohjeita!

## Säveldatatiedostot

Ennen kuin voit soittaa Tone Masterilla ensimmäisen musiikkisävelmäsi, sinun
on ensin luotava ja ladattava säveldatatiedosto. Säveldatatiedostot ovat
yksinkertaisesti .tdf-tarkenteisia tekstitiedostoja. Tone Master käyttää
niitä sävelsarjojen käsittelyyn ja toistamiseen. Luo säveldatatiedosto
seuraamalla alla olevia yksinkertaisia ohjeita.

1. Jokaisen .tdf-tiedoston rivin *täytyy* sisältää kolme kaksoispisteellä
   (:) eroteltua parametria. Ensimmäinen on sävelen korkeus, toinen on kesto
   ja kolmas on hiljaisuuden määrä jokaisen sävelen välissä. Kaikki kolme
   parametria on määritettävä, tai muuten Tone Master ei pysty toistamaan
   säveldataasi.
2. Pitch and duration parameters must be specified as signed integers, and
   the silence must be specified as floating point real value.
3. A hash sign (#) at the beginning of any line in .tdf file will be treeted
   as a comment and will be ignored by Tone Master.

Example: Play a sequence of 3 tones

1500:100:0.5

1000:100:0.09

500:100:0.7

In this example, the first tone in a sequence has a pitch of 1500, duration
of 100 and 0.5 silence. The second tone's pitch is 1000, duration is 100,
and the silence is 0.09. The last tone in a sequence has pitch 500, duration
100, and the silence is 0.7.

Note, the silence parameter is necessary to specify even if you think that
it's not, because if not specified, NVDA will override the previous tone by
the next one, and you will get unexpectable results. That's why I made it to
be necessary.

To get more familiar with tone data files syntax, please view and try
editing the example file included with this add-on. It's located in the
"tones" subfolder, where all your .tdf files must be located as well.

## Shortcut keys

* Alt+NVDA+T: Plays currently loaded tone data if everything is ok.
* Alt+Shift+NVDA+T: Stops playback for currently loaded tone data if any
  tone data is playing.
* Alt+NVDA+N: Creates and opens a new blank tone data file in Notepad for
  editing.
* Alt+NVDA+L: Opens a dialog that lets you choose one of your available tone
  data files to be loaded for playback.
* Alt+NVDA+E: Opens currently loaded tone data file in Notepad for editing.
* Alt+NVDA+O: Opens a folder with tone data files where you should also save
  them in order to be located by Tone Master.

## Other notes

You can also create, edit and load tone data files, or open tones folder
where these files are located by going into the NVDA menu, Tools SubMenu,
Tone Master SubMenu.

When the dialog for creating new tone data file is displayed, type the name
without .tdf extension. The extension will be automatically added by Tone
Master. If no name was specified, Tone Master will use the default name
"untitled.tdf". Tone Master will automatically create and load new file for
you, and it will also be opened in Notepad for editing. Press Escape at the
file name prompt to cancel new file creation.

Note: Tone Master uses Notepad for editing tone data files, since it comes
with Windows by default and therefore any computer should have it available.

When the dialog for loading tone data file is open, use the arrow keys to
select a file to load and then press Enter. Press Escape to cancel loading.

When you open a folder with .tdf files, you can then load them in your text
editor for viewing or editing. However, in order to hear your results on the
fly, I highly recommend you to load the file into Tone Master first if
possible. Then you can edit the file, save your progress, and after each
save you can use play command to hear your last result.

## Muutokset versiossa 1.2

* Korjattu: Osoitettu suuri ongelma, jossa tyhjän säveldatatiedoston
  valitsemisesta ja sitten toisen tiedoston valitsemisesta ja toiston
  yrittämisestä on seurauksena se, ettei säveldataa toisteta.

## Muutokset versiossa 1.1

* Lisätty: Vaihtoehto uuden säveldatatiedoston luomiseen sekä Muistiossa
  avaamiseen ja muokkaamiseen.
* Lisätty: Vaihtoehto nykyisen ladatun säveldatatiedoston muokkaamiseen
  Muistiossa.
* Paranneltu: Virheilmoitukset ovat nyt käyttäjäystävällisempiä.
* Paranneltu: Ttietyt lisäosan ominaisuudet, kuten tones-kansion avaaminen
  tai säveldatatiedostojen muokkaaminen Muistiossa, on nyt estetty
  suojatuissa ruuduissa.
* Paranneltu: Käyttäjälle ilmoitetaan, jos säveldatan toisto on pysäytetty.
* Korjattu: Säveldatan toisto estetty, mikäli toisen tiedoston toisto on
  käynnissä.

## Muutokset versiossa 1.0

* Ensimmäinen versio.

[[!tag dev stable]]

[1]: http://addons.nvda-project.org/files/get.php?file=tmast
