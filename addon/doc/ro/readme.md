# Tone Master #

* Autori: Hrvoje Katić
* Descărcați [versiunea stabilă][1]

Bine ați venit la Tone Master! Am creat acest micuț supliment NVDA doar
pentru distracție, dar și pentru dumneavoastră pentru a vă distra
utilizându-l.

În totdeauna am vrut să creez tonuri muzicale cu NVDA, mai degrabă decât să
ascult progresul NVDA și bipurile de eroare. Totuși, nu este așa de ușor să
fac asta, așa că am vrut întâi să-l fac ușor de folosit. De asta am creat
Tone Master. Imaginați-vă cum ar fi să auziți NVDA-ul cântând melodii de
Mozzart sau Beethoven, sau hituri cunoscute, interpretate de artiști
celebri. Rezultatul final al sunetelor, asemănătoare cu ringtonurile la
vechile telefoane mobile, este distractiv.

Tone Master simplifică procesul de redare a secvențelor de tonuri utilizând
fișierele data. Aceste fișiere pot fi editate utilizând editorul tău favorit
de text apoi salvând pentru a fi redate cu NVDA. Citiți mai departe pentru
instrucțiuni!

## Fișierele data

Înainte de a reda prima ta melodie cu Tone Master, trebuie să creezi și să
încarci fișierul tău data mai întâi. Fișierele data sunt fișiere text simple
cu extensia .tdf. Tone Master utilizează aceste fișiere pentru procesarea și
redarea secvențelor sonore. Pentru a crea un fișier data care poate fi citit
și interpretat de către NVDA, trebuie să urmezi câțiva pași descriși mai
jos.

1. Fiecare linie din fișierul .tdf *trebuie* să conțină trei parametri
   separați de două puncte (:). Primul parametru este înălțimea tonului, al
   doilea fiind durata, iar al treilea fiind timpul de pauză între fiecare
   ton. Toți cei 3 parametri sunt necesari de specificat, sau Tone Master nu
   va fi capabil să redea fișierul tău data.
2. Parametri de înălțime și durată trebuie să fie specificați ca întregi, și
   pauza trebuie să fie specificată ca punct de floating valoare reală.
3. Semnul # la începutului unei linii în fișierul .tdf va fi ignorat ca
   fiind un comentariu.

Exemplu: Redarea unei secvențe de 3 tonuri

1500:100:0.5

1000:100:0.09

500:100:0.7

În acest exemplu, primul ton într-o secvență are înălțimea 15000, durata 100
și pauza 0.5. Înălțimea tonului al doilea este 10000, durata 100 și pauza
0.09. Iar la ultimul ton, înălțimea este 500, durata 100 și pauza 0.7.

Notă, parametrul de pauză este necesar pentru a fi specificat chiar dacă
crezi că nu este, deoarece dacă nu e specificat, NVDA va sări peste tonul
fără durată la celălalt, și vei obține rezultate incorecte. Deaceea l-am
făcut necesar.

Pentru a deveni mai familiar cu sintaxa fișierelor data, încearcă să vezi și
să editezi tonurile date ca exemplu în pachetul add-on-ului. Acestea sunt
loalizate în subfolderul „tones”, unde toate fișierele .tdf trebuie să fie
salvate.

## Scurtărturile pentru tastatură

* Alt+NVDA+T: Redă fișierul data încărcat, dacă totul este OK.
* Alt+Shift+NVDA+T: Oprește redarea fișierului data.
* Alt+NVDA+N: Crează un nou fișier .tdf în notepad pentru ca acesta să poată
  fi editat.
* Alt+Nvda+L: Deschide o casetă de dialog care te lasă să selectezi un
  fișier data dintre cele disponibile pentru a fi redate.
* Alt+NVDA+E: Deschide fișierul data încărcat în Notepad ca acesta să poată
  fi editat.
* Alt+NVDA+O: Deschide un folder unde sunt fișierele data. Fișierele data pe
  care le creezi trebuie să fie salvate aici ca Tone Master să le poată
  localiza.

## Alte note

Poți, de asemenea, să creezi, editezi și încarci fișierele data, sau să
deschizi un folder unde aceste fișiere sunt localizate. Pentru aceasta,
mergi în meniul NVDA, Instrumente, Tone Master.

Când caseta de dialog pentru crearea noilor fișiere data este afișată, scrie
numele fără extensia .tdf. Extensia va fi adăugată automat de către Tone
Master. Dacă nu e specificat niciun nume, Tone Master va folosi numele
implicit „untitled.tdf”. Tone Master va crea automat și va încărca noul
fișier data, și va fi deasemenea deschis în Notepad pentru a fi
editat. Apasă escape în câmpul de editare a numelui pentru a anula.

Notă: Tone Master utilizează Notepad pentru a edita fișierele data, deoarece
acesta se conține în pachetul Windows, și orice computer îl are.

Când caseta de dialog pentru a încărca un ton este deschisă, folosește
segețile pentru a selecta un fișier pentru a-l încărca, apoi apasă
Enter. Apasă Escape pentru a anula încărcarea.

Când deschizi un folder cu fișiere .tdf, poți să le încarci într-un editor
pentru a le vedea și edita. Dar, pentru a auzi melodia interpretată, îți
recomand să încarci fișierul data în Tone Master mai întâi, dacă este
posibil. După aceea poți edita fișierul, poți salva progresul, și după orice
salvare poți să redai melodia folosind comanda de tastatură.

## Changes for 1.3

* fixes wx4 compatibility

## Modificări aduse în versiunea 1.2

* Rezolvat: A fost rezolvată o problemă unde la selectarea unui fișier data
  gol, după la selectarea altuia și la încercarea de redare, Tone Master nu
  redă niciun fișier.

## Modificări aduse în versiunea 1.1

* Adăugat: O opțiune pentru a crea un fișier data și a-l deschide în Notepad
  pentru a fi editat.
* Adăugat: O opțiune pentru a edita melodia încărcată curent, în Notepad.
* Îmbunătățit: Mesajele de eroare sunt acum mai prietenoase.
* Îmbunătățit: Unele caracteristici ale add-on-ului cum ar fi deschiderea
  folderului de tonuri sau editarea fișierelor data în Notepad sunt acum
  interzise în spațiul de lucru sigur.
* Îmbunătățit: Utilizatorul va fi notificat de către NVDA dacă redarea
  fișierului data a fost oprită.
* Rezolvat: A fost interzisă redarea unui ton când altul deja se redă.

## Modificări aduse în versiunea 1.0

* lansarea inițială.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
