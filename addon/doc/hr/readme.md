# Tone Master #

* Autori: Hrvoje Katić
* Preuzmi [stabilnu verziju][1]

Dobrodošli u Tone Master! Stvorio sam ovaj mali NVDA dodatak iz čiste
zabave, ali također i zato da biste se i vi imali priliku malo zabaviti
koristeći ga.

Uvijek sam htio praviti muzičke melodije koje bi mi NVDA onda odsvirao,
umjesto da slušam samo njegove bip signale koji označavaju neki napredak ili
pogrešku. Međutim, to nije baš tako lagano za izvesti, pa sam stoga prvo
htio taj proces učiniti lakšim. To je razlog zašto sam napisao Tone Master
dodatak. Zamislite si samo kako bi vam bilo čuti da NVDA svira neku skladbu
od Mozzarta ili Beethovena, ili možda čak najveće hitove Halida
Bešlića. Iako konačan rezultat zvuči kao one monofone melodije na starim
mobitelima, i dalje to može biti zabavno za čuti.

Tone Master pojednostavljuje proces izvođenja tonskih sekvenci primjenom
datoteka koje sadrže tonski zapis. Te datoteke je moguće uređivati pomoću
vašeg omiljenog tekst editora, a potom spremiti kako bi ih NVDA odsvirao. Za
daljnje upute, čitajte dalje!

## Datoteke s tonskim zapisom

Prije nego što će vam Tone Master moći odsvirati vašu željenu melodiju, prvo
ćete morati stvoriti, a zatim učitati vašu datoteku s tonskim
zapisom. Datoteke s tonskim zapisom (engl. Tone data files) su jednostavno
tekstualne datoteke s nastavkom .tdf. Tone Master koristi te datoteke za
procesuiranje i reprodukciju tonskih sekvenci. Da biste stvorili datoteku s
tonskim zapisom kako bi Tone Master mogao uspješno odsvirati tonsku
sekvencu, morat ćete slijediti jednostavna pravila opisana u nastavku.

1. Svaki redak u .tdf datoteci *MORA* sadržavati tri parametra odvojena
   dvotočkom (:). Prvi parametar je visina tona, drugi parametar je duljina
   tona, a treći je vrijeme tišine između svakog tona. Sva tri parametra je
   obavezno navesti, jer u protivnom Tone Master neće biti sposoban
   reproducirati vaš tonski zapis.
2. Visinu i duljinu potrebno je navesti kao pozitivne brojeve, a tišina mora
   biti navedena kao decimalan broj.
3. Znak ljestve (#) na početku bilo kojeg retka u .tdf datoteci označava
   redak s komentarom i Tone Master će stoga ignorirati takve retke.

Primjer: Odsviraj sekvencu od 3 tona

1500:100:0.5

1000:100:0.09

500:100:0.7

U ovom primjeru, prvi ton u sekvenci ima visinu s vrijednošću 1500, duljinu
100 i tišinu 0.5. Drugi ton ima visinu 1000, duljinu 100, a tišinu
0.09. Posljednji ton u sekvenci ima visinu 500, duljinu 100, a visinu 0.7.

Napomena, parametar za tišinu je obavezan za navesti čak i ako vi mislite da
nije, jer ako ga ne navedete, NVDA će pregaziti prethodni ton sa sljedećim,
pa ćete dobiti neočekivane rezultate. Iz tog razloga sam napravio da ovo
bude obavezno.

Kako biste se bolje upoznali sa sintaksom datoteka sa tonskim zapisom, molim
proučite i probajte izmijeniti datoteku s primjerom koja dolazi uz ovaj
dodatak. Ta datoteka se nalazi u podmapi "tones", gdje ćete također morati
smjestiti i sve vaše .tdf datoteke.

## Tipkovni prečaci

* Alt+NVDA+T: Svira trenutno učitan tonski zapis ako je sve u redu.
* Alt+Shift+NVDA+T: Zaustavlja sviranje trenutno učitanog tonskog zapisa
  ukoliko neki tonski zapis trenutno svira.
* Alt+NVDA+N: Stvara, a zatim otvara novi prazan tonski zapis u Notepad-u za
  uređivanje.
* Alt+NVDA+L: Otvara dijaloški okvir koji vam omogućuje odabir neke od
  dostupnih datoteka s tonskim zapisom koje je moguće učitati za sviranje.
* Alt+NVDA+E: Otvara trenutno učitanu datoteku s tonskim zapisom u Notepad-u
  za uređivanje.
* Alt+NVDA+O: Otvara mapu koja sadrži datoteke s tonskim zapisima gdje ih je
  također potrebno i spremati kako bi ih Tone Master mogao pronaći.

## Ostale napomene

Također možete stvarati, uređivati i učitavati datoteke s tonskim zapisom
ili otvoriti mapu s tonovima gdje se te datoteke nalaze tako da pođete na
NVDA izbornik, podizbornik Alati, pa zatim podizbornik Tone Master.

Kad se prikaže dijaloški okvir za stvaranje novog tonskog zapisa, upišite
ime bez nastavka .tdf. Tone Master će automatski dodati nastavak umjesto
vas. Ukoliko niste naveli ime, Tone Master će upotrijebiti zadano ime
"untitled.tdf". Tone Master će automatski stvoriti i učitati novu datoteku
za vas, a datoteka će se također otvoriti u Notepad-u za
uređivanje. Pritisnite Escape kod zahtjeva za unos imena datoteke da biste
otkazali stvaranje nove datoteke.

Napomena: Tone Master koristi Notepad za uređivanje datoteka s tonskim
zapisom, budući da Notepad dolazi predinstaliran s Windows sustavom i stoga
bi ga svako računalo trebalo imati.

Kad se otvori dijaloški okvir za učitavanje datoteke s tonskim zapisom,
koristite strelice na tipkovnici za odabir datoteke koju želite učitati, a
zatim pritisnite Enter. Pritisnite Escape da biste otkazali učitavanje.

Kad otvorite mapu s .tdf datotekama, možete ih tada učitati u vašem tekst
editoru kako biste ih pregledali ili uredili. Međutim, da biste odmah čuli
svoj rezultat u hodu, preporučio bi vam da prvo učitate datoteku u Tone
Master ako je to ikako moguće. Tada ćete moći uređivati datoteku, spremiti
svoj napredak, a nakon svakog spremanja možete koristiti naredbu za sviranje
kako biste čuli svoj posljednji rezultat.

## Promjene u 1.3

* Ispravak: Ispravljen problem kompatibilnosti s novom NVDA verzijom.

## Promjene u 1.2

* Ispravak: Ispravljena ozbiljna greška gdje učitavanje praznog tonskog
  zapisa, a zatim učitavanje novog rezultira nemogućnošću sviranja pri
  pokušaju da se tonski zapis odsvira.

## Promjene u 1.1

* Dodano: Mogućnost stvaranja nove datoteke s tonskim zapisom te otvaranje
  iste u Notepad-u za uređivanje.
* Dodano: Mogućnost uređivanja trenutno učitane datoteke s tonskim zapisom u
  Notepad-u.
* Poboljšano: Poruke koje najavljuju grešku sada su više prijateljski
  raspoložene prema korisniku.
* Poboljšano: Određene mogućnosti dodatka kao što je otvaranje mape tonova
  ili uređivanje datoteka s tonskim zapisima u Notepad-u sada su zabranjene
  na sigurnosnim ekranima.
* Poboljšano: Korisnik će biti obaviješten od strane NVDA ako je sviranje
  tonskog zapisa zaustavljeno.
* Ispravljeno: Zabranjeno je sviranje tonskog zapisa za vrijeme dok jedan
  još svira.

## Promjene u 1.0

* Prva verzija.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
