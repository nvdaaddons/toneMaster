# Tom Master (Tone Master) #

* Autores: Hrvoje Katić
* Baixe a [versão estável][1]

Bem-vindo ao Tom Master! Criei este pequeno complemento NVDA apenas por
diversão, mas também para você se divertir enquanto o usa.

Eu sempre quis criar composições musicais com o NVDA, em vez de apenas ouvir
os bipes de progresso e erro do NVDA. No entanto, não é muito fácil de
fazer, então primeiro eu queria facilitar. Foi por isso que escrevi Tom
Master. Imagine como poderia ser para você ouvir o NVDA tocando a música de
Mozzart ou Beethoven, ou talvez os maiores sucessos dos Rolling
Stones. Embora o resultado final pareça com os toques em celulares antigos,
ainda pode ser engraçado.

O Tom Master simplifica o processo de reprodução de seqüências de tons
implementando arquivos de dados de tom. Esses arquivos podem ser editados
com o seu editor de texto favorito e salvos para reprodução com o NVDA. Leia
para obter instruções!

## Arquivos de dados de tom

Antes de poder tocar a sua primeira música com o Tom Master, deve primeiro
criar e carregar o seu arquivo de dados de tom. Arquivos de dados de tom
(Tone data files) são simplesmente arquivos de texto com extensão .tdf. O
Tom Master usa esses arquivos para processar e reproduzir seqüências de
tons. Para criar um arquivo de dados de tom para que o Tom Master possa
reproduzi-lo com sucesso, deve seguir as regras simples descritas abaixo.

1. Cada linha no arquivo .tdf *deve* conter três parâmetros separados por
   dois pontos (:). O primeiro parâmetro é a tonalidade (afinação) do tom, o
   segundo parâmetro é a duração do tom e o terceiro é o tempo de silêncio
   entre cada tom. Todos os três parâmetros são necessários para
   especificar, caso contrário, o Tom Master não poderá reproduzir os seus
   dados de tom.
2. Os parâmetros de tonalidade (afinação) e duração devem ser especificados
   como números inteiros assinados (signed integers) e o silêncio deve ser
   especificado como valor real de ponto flutuante.
3. Um sinal de hash (#) no início de qualquer linha no arquivo .tdf será
   tratado como um comentário e será ignorado pelo Tom Master.

Exemplo: Reproduz uma sequência de 3 tons

1500:100:0.5

1000:100:0.09

500:100:0.7

Neste exemplo, o primeiro tom em uma sequência tem uma tonalidade (afinação)
de 1500, duração de 100 e 0,5 de silêncio. A tonalidade do segundo tom é
1000, a duração é 100 e o silêncio é de 0,09. O último tom em uma sequência
tem tonalidade 500, duração 100 e o silêncio é 0,7.

Observe que o parâmetro silêncio é necessário para especificar mesmo que
ache que não é, porque se não for especificado, o NVDA irá sobrescrever o
tom anterior pelo próximo, e você obterá resultados inesperados. É por isso
que eu fiz isso ser necessário.

Para se familiarizar com a sintaxe dos arquivos de dados de tom, veja e
tente editar o arquivo de exemplo incluído neste complemento. Ele está
localizado na subpasta "tones", onde todos os seus arquivos .tdf também
devem estar localizados.

## Teclas de atalho

* Alt+NVDA+T: Reproduz dados de tom carregados no momento, se tudo estiver
  ok.
* Alt+Shift+NVDA+T: Pára a reprodução dos dados de tom carregados no momento
  se algum dado estiver sendo reproduzido.
* Alt+NVDA+N: Cria e abre um novo arquivo de dados de tom em branco no Bloco
  de Notas para edição.
* Alt+NVDA+L: Abre uma caixa de diálogo que permite escolher um dos arquivos
  de dados de tom disponíveis para serem carregados para reprodução.
* Alt+NVDA+E: Abre o arquivo de dados de tom carregado atualmente no Bloco
  de Notas para edição.
* Alt+NVDA+O: Abre uma pasta com arquivos de dados de tom onde você também
  deve salvá-los para que sejam localizados pelo Tom Master.

## Outras notas

Também pode criar, editar e carregar arquivos de dados de tons ou abrir a
pasta de tons onde esses arquivos estão localizados indo para o menu do
NVDA, Submenu Ferramentas, Submenu Tom Master.

Quando a caixa de diálogo para criar o novo arquivo de dados de tom for
exibida, escreva o nome sem a extensão .tdf. A extensão será adicionada
automaticamente pelo Tom Master. Se nenhum nome for especificado, o Tom
Master usará o nome padrão "untitled.tdf". O Tom Master criará e carregará
automaticamente um novo arquivo para você e também será aberto no Bloco de
Notas para edição. Pressione Escape no prompt do nome do arquivo para
cancelar a criação do novo arquivo.

Nota: O Tom Master usa o Bloco de Notas (Notepad) para editar arquivos de
dados de tom, já que ele vem com o Windows por padrão e, portanto, qualquer
computador deve tê-lo disponível.

Quando o diálogo para carregar o arquivo de dados de tom estiver aberto, use
as teclas de seta para selecionar um arquivo para carregar e, em seguida,
pressione Enter. Pressione Escape para cancelar o carregamento.

Ao abrir uma pasta com arquivos .tdf, pode carregá-los no seu editor de
texto para visualização ou edição. No entanto, para ouvir seus resultados
rapidamente, recomendo que carregue o arquivo no Tom Master primeiro, se
possível. Em seguida, você pode editar o arquivo, salvar seu progresso e,
após cada arquivamento, pode usar o comando reproduzir para ouvir seu último
resultado.

## Mudanças para 1.3

* Corrigido: Corrigido problema de compatibilidade com versões mais novas do
  NVDA.

## Mudanças para 1.2

* Corrigido: Problema importante resolvido, em que selecionar um dado de tom
  vazio, em seguida selecionar outro e tentar reproduzi-lo, resultando na
  não reprodução dos dados do tom.

## Mudanças para 1.1

* Adicionado: Uma opção para criar um novo arquivo de dados de tom e abri-lo
  no Bloco de Notas para edição.
* Adicionado: Uma opção para editar o arquivo de dados de tom carregado
  atualmente no Bloco de Notas.
* Aprimorado: As mensagens de erro agora são mais fáceis de usar.
* Aprimorado: Certos recursos adicionais, como a abertura de pasta de tons
  ou a edição de arquivos de dados de tom no Bloco de notas, agora não são
  permitidos em telas seguras.
* Aprimorado: O utilizador será notificado pelo NVDA se a reprodução dos
  dados de tom for interrompida.
* Corrigido: Não permitia a reprodução de dados de tom enquanto o mesmo já
  estava sendo reproduzido.

## Mudanças para 1.0

* Versão inicial.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=tmast
