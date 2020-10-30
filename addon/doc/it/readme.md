# Tone Master #

* Autore: Hrvoje Katić
* Scarica la [versione stabile][1]

Benvenuti in Tone Master! Ho creato questo piccolo add-on per NVDA solo per
divertimento, ma anche perché voi vi divertiate quando lo usate.

Ho sempre desiderato creare melodie musicali con NVDA, piuttosto che
ascoltare soltanto i suoni di errore e delle barre di progresso di
NVDA. Tuttavia ciò non è molto semplice da fare, perciò ho voluto, per prima
cosa, renderlo più semplice.

Tone Master semplifica il processo di riproduzione di sequenze di segnali
acustici, implementando i tone data files. Questi file possono essere
modificati con il vostro editor di testi preferito e poi salvati per essere
riprodotti con NVDA. Leggi oltre per le istruzioni!

## Tone data files

Prima che possiate riprodurre la vostra prima melodia con Tone Master,
dovrete creare e caricare il vostro tone data file. I tone data files sono
semplici file di testo con estensione .tdf. Tone Master usa questi file per
trattare e riprodurre sequenze di segnali acustici. Per creare tone data
files perché Tone Master li possa riprodurre con successo, dovete seguire
semplici regole scritte più avanti.

1. Nei file .tdf, ogni linea deve contenere tre parametri separati da due
   punti (:). Il primo parametro è il tono del suono, il secondo parametro è
   la durata del suono, e il terzo è il tempo di silenzio tra ogni suono. E'
   necessario specificare tutti e tre i parametri, altrimenti Tone Master
   non potrà riprodurre i tone data.
2. I parametri tono e durata vanno specificati come numeri interi con segno,
   mentre il silenzio deve essere specificato come numero reale in virgola
   mobile.
3. Un cancelletto (#) all'inizio di ogni riga nei file .tdf sarà trattato
   come un commento e quindi ignorato da Tone Master.

Esempio: riprodurre una sequenza di tre toni

1500:100:0.5

1000:100:0.09

500:100:0.7

In questo esempio, il primo segnale acustico nella sequenza ha tono pari a
1500, durata pari a 100 e silenzio pari a 0.5. Il tono del secondo suono è
1000, la durata è 100 e il silenzio è 0.09. L'ultimo suono nella sequenza ha
tono 500, durata 100 e il silenzio è 0.7.

Nota: è necessario specificare il parametro silenzio anche se pensate che
non lo sia, perché, se non specificato, NVDA sostituirà il suono precedente
con il successivo, e otterrete risultati imprevisti. Ecco perché l'ho reso
necessario.

Per acquisire familiarità con la sintassi dei Tone data files, leggete e
provate a modificare il file di esempio incluso in questo add-on. Si trova
nella sottocartella "tones", dove devono essere salvati anche tutti i vostri
file .tdf.

## Tasti rapidi

* Alt+NVDA+T: riproduce il suono al momento caricato se tutto è ok.
* Alt+Shift+NVDA+T: interrompe la riproduzione del suono al momento caricato
  se ce n'è uno.
* Alt+NVDA+N: crea ed apre nel blocco note un nuovo tone data file per
  l'editing.
* Alt+NVDA+L: apre una finestra di dialogo che vi permette di scegliere uno
  dei vostri tone data files per caricarlo e riprodurlo.
* Alt+NVDA+E: apre nel blocco note il tone data file al momento caricato per
  l'editing.
* Alt+NVDA+O: apre una cartella con i tone data file, nella quale dovreste
  anche salvarli perché Tone Master li possa trovare.

## Altre note

Potete anche creare, editare e caricare tone data files, o aprire la
cartella dei suoni dove si trovano questi files, andando nel menù di NVDA,
sottomenù Strumenti, sottomenù Tone Master.

Quando appare la finestra per creare nuovi tone data files, scrivete il nome
senza l'estensione .tdf. L'estensione verrà aggiunta automaticamente da Tone
Master. Se non è stato specificato nessun nome, Tone Master utilizzerà il
nome di default "untitled.tdf". Tone Master creerà e caricherà il nuovo file
automaticamente per voi e questo sarà anche aperto nel blocco note per
l'editing. Premete escape alla richiesta del nome del file per annullare la
creazione del nuovo file.

Nota: Tone Master usa il blocco note per editare i tone data files, perché
viene fornito da Windows per default e quindi ogni computer dovrebbe averlo.

Quando si apre la finestra per caricare i tone data file usate i tasti
freccia per selezionare un file da caricare e poi premete Invio. Premete
Escape per annullare il caricamento.

Quando aprite una cartella con file .tdf, potete poi caricarli nel vostro
editor di testi per leggerlo o editarlo. Ad ogni modo, per ascoltare il
vostro risultato al volo, vi suggerisco caldamente di caricare prima il file
in Tone Master se possibile. Poi potrete editare il file, salvare il vostro
progresso, e dopo ogni salvataggio utilizzare il comando Play per ascoltare
il vostro ultimo risultato.

## Novità nella versione 1.3

* Risolto: risolti i problemi di  compatibilità con le nuove versioni di
  NVDA.

## Novità nella versione 1.2

* Risolto: risolto un grosso problema, in cui selezionando un suono vuoto,
  poi selezionandone un altro e provando a riprodurlo dava luogo alla
  mancata riproduzione del suono.

## Novità nella versione 1.1

* Aggiunta: un'opzione per creare un nuovo tone data file ed aprirlo nel
  blocco note per modificarlo.
* Aggiunta: un'opzione per editare nel blocco note il tone data file al
  momento caricato.
* Migliorato: i messaggi di errore ora sono più amichevoli.
* Migliorato: alcune caratteristiche dell'add-on, come aprire la cartella
  dei suoni o modificare i tone data file nel blocco note, sono ora inibite
  nella modalità desktop sicuro.
* Migliorato: gli utenti saranno avvertiti da NVDA se la riproduzione dei
  suoni viene interrotta.
* Risolto: inibita la riproduzione di unsuono quando se ne sta riproducendo
  un altro.

## Novità nella versione 1.0

* Versione iniziale.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
