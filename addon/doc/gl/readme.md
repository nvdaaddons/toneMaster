# Tone Master #

* Autores: Hrvoje Katić
* Descargar [versión estable][1]

¡Benvido ao Tone Master! Creéi este pequeno complemento de NVDA só por
divertimento, pero tamén para que te devirtas ti mentres o usas.

Sempre quixen crear tons musicais co NVDA, en lugar de escoitar os seus
pitidos de progreso e de erro. Nembargantes, non é moi sinxelo de facer, así
que primeiro quixen facelo máis sinxelo. É por elo que escrebín Tone
Master. Só imaxina o que sería para ti escoitar ao NVDA reproducindo
cancións de Mozzart ou de Beethoven, ou dos grandes éxitos dos Rolling
Stones. Aíndaque os resultados últimos soan como aqueles tons de chamada dos
teléfonos móviles vellos, ainda pode ser divertido.

Tone Master simplifica o proceso de tocar secuencias de tons implementando
ficheiros de datos de melodías. Estos ficheiros poden editarse co teu editor
de textos favorito e entón gardalos para reproducilos co NVDA. ¡Le para
instruccións!

## Ficheiros de datos de melodías

Antes de que podas reproducir a túa primeira melodía musical co Tone Master,
tes que crear e cargar o teu ficheiro de datos da melodía primeiro. Os
ficheiros de datos de melodía son simples ficheiros de texto coa extensión
.tdf. Tone Master utiliza estos ficheiros para procesar e reproducir
secuencias de tons. Para crear ficheiros de datos de melodías para que Tone
Master poda reproducilos con éxito, tes que seguir unhas sinxelas regras
descritas abaixo.

1. Cada liña no ficheiro .tdf *debe* conter  tres parámetros separados por
   dous pontos (:). O primeiro parámetro é o ton, o segundo parámetro é a
   duración, e o terceiro é o tempo do silencio entre cada ton. É necesario
   especificar todos os parámetros , de outro xeito Tone Master non poderá
   reproducir os teus datos de melodía.
2. Os parámetros ton e duración  deben especificarse coma enteiros, e o
   silenzo debe especificarse coma un valor real de coma frotante .
3. Un signo de número (#) ao comezo de calquera liña no ficheiro .tdf
   tratarase coma un comentario e ignorarase polo Tone Master.

Exemplo: reproduce unha secuencia de 3 tons

1500:100:0.5

1000:100:0.09

500:100:0.7

Neste exemplo, a primeira nota nunha secuencia ten un ton de 1500, unha
duración de 100 e un silenzo de 0.5. a nota do segundo ton é 1000, a
duración é 100, e o silenzo é 0.09. a derradeira nota nunha secuencia ten
ton 500, duración 100, e o silenzo é 0.7.

Nota, é necesario especificar o parámetro silenzo incluso se pensas que non
o é, porque se non se especifica, NVDA anulará a nota anterior coa seguinte,
e obterás resultados inesperados. É por eso que fíxeno ser necesario.

Para chegar a estar máis familiarizado coa sintaxis dos ficheiros de datos
de melodías, por favor revisa e intenta editar o ficheiro exemplo incluido
con este complemento. Atópase no subcartafol "tones" , onde tamén se deben
colocar todos os teus ficheiros .tdf.

## Atallos de teclado

* Alt+NVDA+T: reproduce o ficheiro de melodías actualmente cargado se todo
  está ben.
* Alt+Shift+NVDA+T: detén a reproducción para o ficheiro de datos de melodía
  actualmente cargado se calquera melodía se está a reproducir.
* Alt+NVDA+N: crea e abre un ficheiro de datos de melodía novo no Bloc de
  Notas para editar.
* Alt+NVDA+L: abre un diálogo que che permite escoller un dos teus ficheiros
  de datos de melodía dispoñibles para se cargar para reproducirse.
* Alt+NVDA+E: abre o ficheiro de datos de melodía actualmente cargado no
  Bloc de Notas para editar.
* Alt+NVDA+O: abre un cartafol con ficheiros de datos de melodía onde tamén
  deberías gardalos para seren localizados polo Tone Master.

## Outras notas

Tamén podes crear, editar e cargar ficheiros de datos de melodía, ou abrir o
cartafol de melodías onde se atopan estos ficheiros indo ao menú NVDA,
submenú Ferramentas, submenú Tone Master.

Cando se amose o diálogo para crear ficheiros de datos de melodía novos,
teclea o nome sen a extensión .tdf. A extensión engadirase automáticamente
polo Tone Master. Se non se especificou nome algún, Tone Master utilizará o
nome predeterminado "untitled.tdf". Tone Master creará automáticamente und
novo ficheiro cargado para ti, e tamén se abrirá no Bloc de Notas para
editar. Preme Escape no indicativo do nome de ficheiro para cancelar a
creación do ficheiro novo.

Nota: Tone Master usa Bloc de Notas para editar ficheiros de datos de
melodía, xa que ven co Windows por defecto e polo tanto calquer computador
debería telo dispoñible.

Cando o diálogo para cargar ficheiro de datos de melodía estea aberto, usa
as teclas de frecha para selecionar un ficheiro para cargar e entón preme
Intro. Preme Escape para cancelar a carga.

Cando abres un cartafol con ficheiros .tdf, podes entón cargalos no teu
editor de texto para velos ou editalos. Non obstante, para escoitar os teus
resultados de inmediato, recoméndoche moito cargar o ficheiro no Tone Master
primeiro se é posible. entón podes editar o ficheiro, garda o teu progreso,
e despois de cada gardado podes usar a orde reproducir para escoitar o teu
derradeiro resultado.

## Changes for 1.3

* Fixed: Fixed compatibility issue with newer NVDA versions.

## Cambios para 1.2

* Correxido: dirixido un problema maior onde ao selecionar un ficheiro de
  datos de melodía valdeiro, logo ao selecionar outro e intentar reproducilo
  ocurre que os datos de melodía non se reproducen.

## Cambios para 1.1

* Engadida: Unha opción para crear un ficheiro novo de datos de melodía e
  para abrilo no Bloc de Notas para editar.
* Engadida: Unha opción para editar o ficheiro de datos de melodía
  actualmente cargado no Bloc de Notas.
* Mellorado: as mensaxes de erro agora son máis amigables para o usuario.
* Mellorado: certas características do complemento como a apertura do
  cartafol de melodías ou a edición de ficheiros de datos de melodía no Bloc
  de Notas agora non se permiten nas pantallas seguras.
* Mellorado: notificarase ao usuario polo NVDA se a reprodución de datos de
  melodía se detén.
* Correxido: non se permite a reprodución de datos de melodía mentras un
  estea xa en reprodución.

## Cambios para 1.0

* Versión inicial.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
