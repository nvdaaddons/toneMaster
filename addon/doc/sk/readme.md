# Hracia skrynka #

* Autor: Hrvoje Katić
* Stiahnuť [stabilnú verziu][1]

Vitajte! Tento doplnok pre NVDA som vytvoril ako kratochvíľu a verím, že
budete mať s ním veľa zábavy.

NVDA dokáže pípať pri chybách a indikátore priebehu. Prečo by nemohlo zahrať
Mozzarta, Beethovena, prípadne niečo od Rollingstones? Také čosi nie je
úplne ľahké, a preto som vytvoril tento doplnok. Výsledok znie ako
niekdajšie zvonenia, ale stále je to zábavné.

Doplnok hracia skrynka uľahčuje vytváranie a následné prehrávanie súborov s
melódiami. Súbory môžete vytvoriť a uložiť v textovom editore.

## Súbory s melódiou

Najprv musíte vytvoriť súbor, do ktorého zapíšete melódiu. Súbor musí mať
príponu .tdf.

1. Na každom riadku *musia* byť tri parametre oddelené dvojbodkou (:). Prvý
   parameter je výška tónu, druhý dĺžka tónu a tretí je dĺžka ticha, ktoré
   bude nasledovať za tónom.
2. Výšku a dĺžku tónu určujete v celých číslach, dĺžku ticha je možné určiť
   ako reálne číslo a môžete použiť aj desatinné miesta. (Poznámka
   prekladateľa: Autor doplnku neuvádza, v akých jednotkách času sa uvádzajú
   dĺžky, predpokladám, že pôjde o milisekundy. Výšku tónu zapisujeme v
   hertzoch).
3. Komentár do súboru s melódiou môžete napísať na samostatný riadok, ktorý
   začnete znakom krížik (#).

Takto napríklad zahráme sekvenciu troch tónov:

1500:100:0.5

1000:100:0.09

500:100:0.7

Prvý tón má výšku 1500 hertzov, dĺžku 100 a nasleduje ticho v trvaní
0.5. Druhý má výšku 1000, trvanie 100, s ticho je 0.09. Tretí tón má výšku
500, trvanie 100, a ticho 0.7.

Vždy musíte špecifikovať aj parameter ticho a to aj v prípade, že žiadne
ticho nechcete vložiť. Inak bude NVDA tóny ignorovať.

Aby ste lepšie pochopili fungovanie súborov s melódiou, pozrite si ukážkovú
melódiu, ktorú nájdete v priečinku "tones" v priečinku doplnku. Do tohto
adresára tiež musíte uložiť aj vaše súbory s melódiami.

## Klávesové skratky

* Alt+nvda+T: Prehrá súbor s melódiou.
* Alt+Shift+NVDA+T: Zastaví prehrávanie.
* Alt+NVDA+N: Otvorí poznámkový blok s a umožní vytvoriť nový súbor s
  meódiou.
* Alt+NVDA+L: Otvorí zoznam melódií, z ktorého môžete vybrať súbor na
  prehratie.
* Alt+NVDA+E: Otvorí v poznámkovom bloku súbor s melódiou, ktorý ste
  načítali zo zoznamu melódií.
* Alt+NVDA+O: Otvorí priečinok, v ktorom musia byť uložené melódie.

## Poznámky

Priečinok s melódiami je možné otvoriť z menu NVDA > nástroje > Hracia
skrynka.

Keď vytvárate nový súbor s melódiou cez skratku nvda+alt+n, názov zadávajte
bez prípony. Ak nevložíte názov, doplnok priradí názov "bez
názvu". Vytvorenie nového súboru môžete zrušiť klávesom escape.

Na vytváranie a úpravu používa doplnok poznámkový blok, keďže Notepad je
súčasťou operačného systému a predpokladá sa, že bude k dispozícii.

V dialógu na načítanie melódie vyberte šípkami požadovanú melódiu a otvorte
ju klávesom enter.

Súbory s príponou .tdf môžete priamo otvoriť a upravovať z priečinka
"tones". Ak chcete upravovať melódiu a súčasne počuť výsledok, najprv
melódiu načítajte cez skratku nvda+alt+l. Po uložení budete môcť rovno
opakovane prehrávať výsledok.

## Verzia 1.3

* Upravené pre nové verzie NVDA.

## Verzia 1.2

* Opravená chyba, ktorá nastala ak ste sa pokúsili prehrať prázdny súbor a
  potom už nefungovalo ani prehrávanie ostatných súborov.

## Verzia 1.1

* Pridaná možnosť vytvorenia súboru.
* Pridaná možnosť otvoriť súbor s melódiou z ponuky doplnku.
* Upravené chybové hlásenia.
* Na zabezpečených obrazovkách viac nie je možné upravovať a vytvárať súbory
  s melódiou.
* NVDA upozorní na skončenie prehrávania.
* Zakázané prehrávanie viacerých súborov súčasne.

## Verzia 1.0

* Prvé vydanie.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
