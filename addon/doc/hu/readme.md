# Hangmester #

* Írta: Hrvoje Katić
* Letöltés [stabil verzió][1]

Üdvözlöm a hangmesterben! Ezt a kis NVDA-bővítményt viccből írtam, és
megosztom Önnel, hogy egy kicsit jobb kedvre derítsem, míg használja.

Mindig szerettem volna zenei hangokat készíteni az NVDA-val ahelyett, hogy a
folyamatjelzője vagy hibajelzése hangjait hallgatnám. Ezeket azonban nem
könnyű megalkotni, így először lehetővé szerettem volna tenni, hogy
könnyebben lehessen dallamokat készíteni. Ezért írtam meg a
hangmestert. Most képzelje el, milyen lenne, ha az NVDA Mozartot, Beethovent
vagy mondjuk  a Rolling Stones egy nagy slágerét játszaná. Bár az
elkészített dallamok úgy szólnak, mint a régi mobilokon, ez még így is
vicces.

A hangmester leegyszerűsíti a hangfájlok elkészítését. Ehhez használja
kedvenc szövegszerkesztőjét, majd mentse el a fájlt és játssza le az
NVDA-val. Olvassa el ehhez  a további tudnivalókat!

## A hangadat-fájlok

Ahhoz, hogy lejátssza első dallamát a hangmesterrel, először meg kell
alkotnia és be kell töltenie hangadat-fájlját. A hangadat-fájlok egyszerű
szöveges fájlok .tdf kiterjesztéssel. A hangmester ezeket a fájlokat
használja a dallam előállítására és lejátszására. Ahhoz, hogy a hangmester
megfelelően lejátssza az alkotott dallamot, tartsa be az alábbi egyszerű
szabályokat!

1. A tdf fájl minden sorának *három* paramétert kell tartalmaznia, melyeket
   : (kettős pont9 választ el. Az első paraméter a hangmagasság, a második a
   hang hossza, a harmadik pedig a szünet hossza két hang között. Mind a
   három paramétert meg kell adni, különben a hangmester nem tudja
   lejátszani a hangadatokat.
2. A hangmagasságnak és a hang hosszának egész számnak kell lennie, a szünet
   pedig lebegőpontos valós érték legyen.
3. Ha a sor elejére # (kettős kereszt) kerül, a hangmester a sort
   megjegyzésnek tekinti és figyelmen kívül hagyja.

Példa: játsszunk le egy háromhangos dallamot!

1500:100:0.5

1000:100:0.09

500:100:0.7

Ebben a példában az első hang a sorban 1500-as hangmagasságú, a hossza 100
és 0.5 a szünet. A második hang magassága 1000, hossza 100 és a szünet
0.09. Az utolsó hang hangmagassága a sorban 500, hossza 100 és a szünet 0.7.

Megjegyzés: A szünetet kötelező minden hangnál megadni, különben az egyik
hang rátorlódik a másikra és ez váratlan eredményekhez vezet. Ezért kötelező
ez a paraméter.

Ha szeretné tanulmányozni a hangkészítés szabályait, kérem, tekintse meg és
szerkessze át a bővítményhez mellékelt példafájlt. A fájlt a "tones"
almappában találja, ide kell tennie a saját .tdf fájljait is.

## Billentyűparancsok

* Alt+NVDA+T: Lejátssza a betöltött hangfájlt, ha minden rendben.
* Alt+Shift+NVDA+T: ha szól egy dallam, megálítja a lejátszást.
* Alt+NVDA+N: Készít és megnyit egy üres hangadat-fájlt a jegyzettömbben
  szerkesztés céljából.
* Alt+NVDA+L: Megnyit egy párbeszédpanelt, hogy megnyithassunk egy
  hangadat-fájlt lejátszásra.
* Alt+NVDA+E: Megnyitja a betöltött fájlt jegyzettömbben szerkesztésre.
* Alt+NVDA+O: Megnyit egy mappát, melyben hangadat-fájlok vannak, és ahová a
  hangadatokat menteni lehet a hangmesterrel.

## Egyéb megjegyzések

Hangadat-fájlokat készíteni, szerkeszteni és betölteni vagy hangadat-mappát
megnyitni, melyben ilyen fájlok vannak, az NVDA/eszközök/hangmester menüben
is lehet.

Ha az új hangadat-fájl készítése párbeszédpanel megnyílik, írjon be egy
nevet .tdf kiterjesztés nélkül. A kiterjesztést a hangmester automatikusan
hozzáadja a fájlnévhez. Ha nem ad meg fájlnevet, a hangmester az
alapértelmezés szerinti "untitled.tdf" fájlnevet használja. A hangmester az
új fájlt automatikusan létrehozza és megnyitja a jegyzettömbben
szerkesztésre. Nyomjon escape-et a fájlnév bekérésekor, ha mégsem szeretne
új fájlt készíteni.

Megjegyzés: A hangmester a jegyzettömböt használja szerkesztésre, mert ez a
Windows tartozéka, és minden számítógépen megtalálható.

Ha a hangadatok betöltése párbeszédpanel nyitva van, használja a nyilakat a
betöltendő fájl kiválasztására, majd nyomjon entert. Nyomjon escape-et a
betöltés mellőzéséhez.

Ha megnyit egy mappát, mely tdf fájlokat tartalmaz, a megtekintésüket és
szerkesztésüket a szövegszerkesztővel végezheti. Ha azonnal szeretné hallani
az eredményt, erősen ajánlom, hogy először töltse be a fájlt a hangmesterbe,
ha lehetséges. Ezt követően szerkesztheti a fájlt, mentse el az eredményt,
majd minden mentés után használhatja a lejátszás parancsot az utolsó
eredmény meghallgatásához.

## Az 1.2. verzió változásai

* Javítás: egy nagyobb címzési hiba, ahol egy üres hangadat-fájl választása
  után egy másik választásakor annak lejátszása meghiúsult.

## Az 1.1. verzió változásai

* Hozzáadva egy új opció, mellyel új hangfájlt lehet készíteni és megnyitni
  szerkesztésre a jegyzettömbben.
* Hozzáadva egy opció, mellyel a jelenleg betöltött hangfájlt lehet
  szerkeszteni a jegyzettömbben.
* Fejlesztés: a hibaüzenetek felhasználóbarátabbá váltak.
* Fejlesztés: a bővítmény bizonyos funkciói, például a hangfájlok mappájának
  megnyitása vagy a hangfájlok szerkesztése jegyzettömbben tiltva lettek a
  biztonsági képernyőkön.
* Fejlesztés: Az NVDA tájékoztatja a felhasználót, ha a lejátszás leáll.
* Javítás: ha egy hangfájl lejátszása folyamatban van, már nem lehet egy
  másikat is elindítani.

## Az 1.0. verzió változásai

* Eredeti kiadás.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
