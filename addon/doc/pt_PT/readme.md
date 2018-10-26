# Tone Master #

* Autor: Hrvoje Katić
* Baixar [versão estável][1]

Bem-vindo ao mestre de tom! Eu criei este pequeno extra do NVDA apenas por
diversão, mas também para que se possa divertir enquanto o usa.

Eu sempre quis criar aspectos musicais com o NVDA, em vez de apenas ouvir os
seus bips de progresso e erro. No entanto, não é muito fácil fazer isto,
então primeiro eu queria facilitar. É por isso que escrevi Tone
Master. Imagine como seria ouvir o NVDA tocando música de Mozzart ou
Beethoven, ou pode ser o maior sucesso dos Rolling Stones. Embora o
resultado final soe como aqueles toques em celulares antigos, ainda pode ser
engraçado.

O Tom Master simplifica o processo de execução de seqüências de tons,
implementando arquivos de dados de tom. Estes arquivos podem ser editados
com o seu editor de texto favorito e depois salvos para reprodução com o
NVDA. Leia para instruções!

## Ficheiros de dados de tom

Antes de tocar a sua primeira música com o Tone Master, deve primeiro criar
e carregar o seu ficheiro de dados de tom. Ficheiros de dados de tom são
simplesmente ficheiros de texto com extensão .tdf. O Tom Master usa esses
ficheiiros para processar e reproduzir seqüências de tons. Para criar um
ficheiro de dados de tom para que o Tone Master possa reproduzi-lo com
sucesso, deve seguir as regras simples descritas abaixo.

1. Cada linha no ficheiro .tdf * deve * conter três parâmetros separados por
   dois pontos (:). O primeiro parâmetro é o tom do tom, o segundo parâmetro
   é a duração do som e o terceiro é o tempo de silêncio entre cada
   tom. Todos os três parâmetros são necessários para especificar, caso
   contrário, o Tom Master não poderá reproduzir os seus dados de tom.
2. Os parâmetros de entoação e duração devem ser especificados como inteiros
   , e o silêncio deve ser especificado como valor real de ponto flutuante.
3. Um sinal de cardinal (#) no início de qualquer linha no ficheiro.tdf será
   mostrado como um comentário e será ignorado.

Exemplo: reproduz uma sequência de 3 tons

1500:100:0.5

1000:100:0.09

500:100:0.7

Neste exemplo, o primeiro tom em uma sequência tem um tom de 1500, duração
de 100 e 0,5 silêncio. O pitch do segundo tom é 1000, a duração é 100 e o
silêncio é de 0,09. O último tom em uma sequência tem pitch 500, duração 100
e o silêncio é 0.7.

Note que o parâmetro silêncio é necessário para especificar mesmo que ache
que não é, porque se não for especificado, o NVDA irá sobrescrever o tom
anterior pelo próximo, e você obterá resultados inesperados. É por isso que
eu fiz isso para ser necessário.

Para se familiarizar com a sintaxe dos ficheiros de dados de tom, veja e
tente editar o ficheiro de exemplo incluído neste complemento. Ele está
localizado na subpasta "tons", onde todos os seus arquivos .tdf devem estar
localizados também.

## Teclas de atalho:

* Alt+NVDA+T: Reproduz dados de tom carregados no momento, se tudo estiver
  ok.
* Alt+Shift+NVDA+T: Pára a reprodução dos dados de tom carregados
  actualmente se algum dado de tom estiver a ser reproduzido.
* Alt+NVDA+N: Cria e abre um novo ficheiro de dados de tom em branco no
  Bloco de Notas para edição.
* Alt+NVDA+L: Abre uma caixa de diálogo que permite escolher um dos
  ficheiros de dados de tom disponíveis para serem carregados para
  reprodução.
* Alt+NVDA+E: Abre o ficheiro de dados de tom carregado actualmente no Bloco
  de Notas para edição.
* Alt+NVDA+O: Abre uma pasta com ficheiros de dados de tom, onde também deve
  guardá-los para serem localizados pelo extra.

## Outras notas

Também pode criar, editar e carregar ficheiros de dados de tons ou abrir a
pasta de tons onde esses ficheiros estão localizados indo para o menu do
NVDA, submenu de ferramentas, submenu de mestre de tons.

Quando a caixa de diálogo para criar o novo ficheiro de dados de tom for
mostrada, escreva o nome sem a extensão .tdf. A extensão será adicionada
automaticamente pelo Tom Master. Se nenhum nome for especificado, o Mestre
de Tom usará o nome padrão "untitled.tdf". O Tone Master irá criar e
carregar automaticamente novos ficheiros para si, e também será aberto no
Bloco de Notas para edição. Pressione Escape no prompt do nome do ficheiro
para cancelar a criação de novos ficheiros.

Nota: O Tom Master usa o Notepad para editar ficheiros de dados de tom, já
que ele vem com o Windows por padrão e, portanto, qualquer computador deve
tê-lo disponível.

Quando a caixa de diálogo para carregar o ficheiro de dados de tom estiver
aberta, use as teclas de seta para seleccionar um ficheiro para carregar e,
em seguida, pressione Enter. Pressione Escape para cancelar o carregamento.

Quando abre uma pasta com ficheiros.tdf, pode carregá-los no seu editor de
texto para visualização ou edição. No entanto, para ouvir os seus resultados
em tempo real, recomendo que carregue o ficheiro no Tone Master primeiro, se
possível. Então pode editar o ficheiro, guardar o seu progresso, e após cada
arquivamento pode usar o comando play para ouvir o seu último resultado.

## Mudanças para 1.3

* Corrigido: Corrigido problema de compatibilidade com versões mais novas do
  NVDA.

## Mudanças para 1.2

* Corrigido: Um Problema importante resolvido, em que seleccionar um dado de
  tom vazio e, em seguida, seleccionar outro e tentar reproduzi-lo resultava
  em dados de tom que não eram reproduzidos.

## Mudanças para 1.1

* Adicionado: uma opção para criar um novo ficheiro de dados de tom e
  abri-lo no Bloco de Notas para edição.
* Adicionado: uma opção para editar o ficheiro de dados de tom carregado
  actualmente no Bloco de Notas.
* Aprimorado: as mensagens de erro agora são mais fáceis de usar.
* Aprimorado: Certos recursos adicionais, como a abertura de pasta de tons
  ou a edição de ficheiros de dados de tom no Bloco de notas, agora não são
  permitidos em ecrãs seguros.
* Melhorado: O utilizador será notificado pelo NVDA se a reprodução dos
  dados de tom for interrompida.
* Corrigido: não permitia a reprodução de dados de tom enquanto o outro já
  estava sendo reproduzido.

## Mudanças para 1.0

* Versão inicial

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
