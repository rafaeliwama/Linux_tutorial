# Linux_tutorial

## Se localizando no terminal utilizando <i>pwd<i>, <i>ls<i>, <i>mkdir<i>, <i>cd<i>, <i>man<i> e <i>help<i>.

A imagem abaixo representa uma janela do terminal.


![Screenshot from 2023-03-08 15-21-31](https://user-images.githubusercontent.com/46658489/223791482-39940e71-fa26-44e3-8705-205159d6fd11.png)


Repare a linha: (base) rafael@malaco:~$

Significado de cada item na linha acima:

(base): ignora isso agora. A gente vê isso depois.

rafael: usuário. O mesmo que você loga com sua senha.

malaco: nome do computador

~: caminho para o diretório atual. O diretório é a mesma coisa que a pasta no windows (err credo, pior sistema operacional). o charactere ~ indica o diretório de usuário.
Também conhecido como /home. Todos os seus arquivos e diretórios estão armazenados dentro deste diretório /home. A notação utilizada para descrever o diretório é a seguinte:

    /home/directory1/directory2/directory3

$: sei lá o que é isso

O coiso piscante: isso é o prompt. Quando ele está piscando, o terminal está disponível para receber comandos.

### Comando <i>pwd<i>

Para verificar o seu diretório atual, digite o comando <i>pwd<i>.

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ pwd
/home/rafael/Dropbox/working_folder_dropbox/Andrade_lab/Genomes
```

### comando <i>ls<i>

Para listar os arquivos e diretórios presentes no diretório atual, utilize o comando <ls>.

```
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls
AmpAmp  notebook_genomes.txt  PolPol  SacCar  SemBal
```

### opções de comandos

Normalmente, comandos podem aceitar ou exigir a utilização de opções. Apesar de cada comando ter formatos de opções diferentes, no geral, utiliza-se um dos seguintes formatos:
-opção1, --opção2, -o3.

Além das opções, algumas opções podem requerer valores. Estes valores podem ser um conjunto de characteres (ex. nome de um arquivo), ou um valor numérico (ex. uma fração).

Para verificar quais as opções disponíveis do comando <ls>, digite:

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls --help
```
Na linha de comando acima, a opção --help é direcionada ao comando ls.

**Pergunta:** o que a linha de comanda acima retorna? Quais são as informações contidas no retorno da opção --help (preste atenção na linha que contem o 'usage'? 
Como esta opção é útil no cotidiano do bioinformata?

Digite no prompt o seguinte comando:

``` 
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls -l -h -a
total 36K
drwxrwxr-x  6 rafael rafael 4,0K fev 14 14:37 .
drwxr-xr-x 10 rafael rafael 4,0K fev 14 12:49 ..
drwxrwxr-x  2 rafael rafael 4,0K fev 13 12:03 AmpAmp
-rw-rw-r--  1 rafael rafael 8,5K mar  7 17:30 notebook_genomes.txt
drwxrwxr-x  2 rafael rafael 4,0K fev 13 14:06 PolPol
drwxrwxr-x  2 rafael rafael 4,0K mar  8 13:58 SacCar
drwxrwxr-x  3 rafael rafael 4,0K fev 14 14:41 SemBal
```

**Pergunta:** utilizando os retorno da opção '--help', quais são as funções das opcoes -l, -h e -a?
Obs: arquivos ocultos começam com o character '.'.

Digite o seguinte comando:
```
(base) rafael@malaco:~/Dropbox/working_folder_dropbox/Andrade_lab/Genomes$ ls -lha
```
**Pergunta:** qual a diferença entre este comando e o comando anterior?

Cada coluna do retorno desta linha de comando é um detalhe do arquivo. Veja a figura abaixo:

![Screenshot from 2023-03-08 17-01-02](https://user-images.githubusercontent.com/46658489/223824854-240ba39c-94e4-488a-ac3c-5b050ccd1383.png)

**Permissões:** as permissões são descrições de quais ações o presente usuário pode efetuar com o arquivo. Exemplos de permissões são: escrever (alterar) e executar o arquivo.

**Tamanho:** o tamanho do arquivo, quando a opção -h é dada, é medida em B, kB, GB, TB.

**Data de criação:** Dá a data e a hora de criação do arquivo. Um detalhe importante é que a hora de criação é a hora em que o arquivo foi alterado pela última vez.


## Utilizando o Google: sim, eu tô ensinando isso!

Em programação a ferramenta mais efetiva é o Google. É muito comum que o programador não saiba como realizar uma determinada tarefa, o significado do retorno de um comando ou como utilizar um comando específico.
Para isso temos o Google!

Mas não é tão fácil assim. Pesquisar conteúdos de programação no Google requer um pouco de prática e paciência para achar os termos certos.

**Atividade:** procure no google o que as outras colunas retornadas da linha de comando acima significam.

## Criando e navegando por diretórios. mkdir, cd.

Para trabalhar com as linhas de comando, umas das principais atividades é navegar pelos diretórios. Navegar pelos diretórios significa mudar o diretório atual, aquele que você está. Para navegar pelos seus diretórios, nós vamos criar um novo diretório, chamado 'new_directory'. Após o novo diretório ser criado nós vamos mudar de diretório para criar novos arquivos neste 'new_directory'.


Para checar qual é diretório atual, use o comando pwd apresentado anteriormente.

```
(base) Rafaels-MacBook-Pro:~ rafael$ pwd
```

**Pergunta:** qual é o seu diretório atual?

Para criar um novo diretório, utilize o comando mkdir

```
(base) Rafaels-MacBook-Pro:~ rafael$ mkdir new_directory

```

**Pergunta:** como você pode checar se o novo diretório foi criado?

Para mudar o seu diretório atual para o novo diretório, utilize o comando cd.

```
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ cd new_diretory
```
**Pergunta:** como você pode checar se está no diretório desejado?


É importante notar, o comando cd obedece a seguinte estrutra: cd [directory_path]

O path the de um arquivo ou diretório é todo o caminho utilizado para chegar até um determinado arquivo ou diretório. 

Por exemplo: 

/home/rafael/Dropbox/working_folder_dropbox/Andrade_lab/Genomes

Esta linha indica que o diretório 'Genomes' está dentro do diretório 'Andrade_lab' e assim por diante.

Contudo, o prompt assume o path do seu diretório atual, e por isso você não precisa digitar o caminho inteiro de arquivos e diretórios que estão dentro do seu diretório atual. Esta regra serve tanto para o comando cd, como para outros comandos.

Por exemplo:

```
(base) Rafaels-MacBook-Pro:new_diretory rafael$ cd ~/Users/rafael/Dropbox/working_folder_dropbox/Andrade_lab/IC/tutorial1_linux/new_diretory

(base) Rafaels-MacBook-Pro:new_diretory rafael$ cd new_diretory
```

Ambos os comandos acima, são equivalentes caso você esteja no diretório 'Tutorial1_linux', mas são diferentes se você estiver em outro diretório.
    
Outro ponto importante é que escrever todo o path do diretório que você quer que seja o seu diretório atual é uma forma rápida de navegar por diretórios que não estejam diretamente acima ou abaixo do seu diretório atual. Nós vamos ver isso em exemplos mais pra frente.
    
Use o comando 'cd ..' para navegar para o diretório diretamente acima do seu diretório atual e verifique seu diretório atual com o comando pwd.
    
```
(base) Rafaels-MacBook-Pro:new_diretory rafael$ cd ..
(base) Rafaels-MacBook-Pro:new_diretory rafael$ pwd
```
    

## Criando e printando arquivos de texto utilizando touch, nano e cat
    
Certo. Você já sabe como navegar pelos diretórios, mas esses diretórios estão completamente vazios. Como você pode começar a criar arquivos para trabalhar?
    
Dois comandos podem ser úteis para criar arquivos: 'touch' e 'nano'.

O comando 'touch' cria arquivos vazios e pode ser útil qnd você quer redirecionar o conteúdo de um outro arquivo ou diretamente da linha de comando para este arquivo vazio.

```
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ touch empty_file.txt
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ ls
empty_file.txt	new_diretory
```
Observe que dois itens retornaram do comando ls, e um deles é o novo arquivo criado.
    
Nós nomeamos o novo arquivo utilizando o charactere '_' para separar as palavras. Isso ocorre, porque utilizar um espaco pode fazer com que o prompt entenda que nós estamos digitando o nome de dois arquivos, o empty e o file.txt
    
Perceba tbm o '.txt' no final do nome do arquivo. Este elemento é a extensão do arquivo, e possibilita que muitos softwares identifiquem de maneira rápida qual o formato do arquivo. Nós falaremos de outras extensões e formatos de arquivos mais tarde.
    

Para criar e editar arquivos de textos, nós podemos utilizar o comando 'nano'. Este comando abre um editor de text no próprio terminal e permite a edição rápida de arquivos .txt sem que você precise abrir o arquivo. Esta estratégia possui duas vantagens. Você não precisa abrir um editor de text fora do terminal, que pode consumir muita memória caso o arquivo seja grande. E a outra vantagem é que você não precisar fazer upload e download de arquivos de textos de um servidor para editá-los.


Digite a a seguinte linha de comando:

```
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ nano nano_file.txt
```

Repare que nós especificamos o nome do novo arquivo criado. Você pode omitir o nome do novo arquivo e nomeá-lo depois, no próprio nano caso dejesar.


A figure abaixo é uma representação do editor de texto nano:
    
<img width="675" alt="Screen Shot 2023-03-08 at 9 15 21 PM" src="https://user-images.githubusercontent.com/46658489/223884877-bbad847b-dd06-437a-ab0b-a4c83884e32d.png">

Digite a seguinte frase no editor de texto: "Truce fatos!"

Feche o nano utilizando o comando ctr+x e siga as instruções para salvar o arquivo.

Em seguida utilize o comando cat para inspecionar o conteúdo dos arquivos 'empty_file.txt' e 'nano_file.txt'.

```
Rafaels-MacBook-Pro:tutorial1_linux rafael$ cat empty_file.txt 
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ cat nano_file.txt 
Truce fatos!
```

**Pergunta:** o que acontece após você utilizar o comando cat para cada um dos arquivos?
    

# Baixando dados do GitHub, inspecionando arquivos reais e extraindo dados de arquivos de texto
    
Muitos dos programas, base de dados e dados de sequenciamento são públicos e estão disponíveis para download. Você pode baixar os arquivos manualmente em suas respectivas páginas da web, mas esse processo pode consumir muito tempo e não permite um alto nível de reproducibilidade.
    
Por isso, é muito comum fazer o download desses programas, bases de dados e dados públicos direto do terminal, para que esse processo possa ser o mais automatizado possível.
    
Há muitos repositórios que armazenam dados de diferentes naturezas. O GitHub é um deles e ele permite o download de qualquer tipo de arquivo, inclusive softwares inteiros.
    
Nos próximos exercícios, nós vamos trabalhar com dados que já foram publicados e que eu estou disonibilizando para download pelo GitHub para fins didáticos.


Para baixar o repositório com todos os dados necessário para realizar os próximos exercícios digite:

```
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ git clone https://github.com/rafaeliwama/Linux_tutorial.git
(base) Rafaels-MacBook-Pro:tutorial1_linux rafael$ ls
Linux_tutorial	empty_file.txt	nano_file.txt	new_diretory
```

O comando passa a opção clone para o software git, que faz clona o diretório Linux_tutorial do meu repositório no GitHub para a seu diretório atual. Por fim, o comando ls lista os arquivos e diretórios presentes no seu diretório atual.

**Atividade:** mova-se para o diretório 'Linux_tutorial' e inspecione o arquivo 'anti_dec2016.fasta' utilizando o comando 'cat'.


Perceba que este arquivo é grande e pode ser difícil a visualização do comeco e do final do arquivo.

Arquivos de utilizados em bioformática normalmente são extensos e possuem muitos dados. inspecianar esses arquivos com 'cat' pode se tornar inviável rapidamente, pela falta de praticidade. 


Para inspecionar apenas o começo do arquivo, digite utilize o comando 'head'.

```
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ head anti_dec2016.fasta
Rafaels-MacBook-Pro:Linux_tutorial rafael$ head anti_dec2016.fasta 
>gi|3411116|gb|AAC31158.1|_FXa-directed_anticoagulant_precursor_Aedes_aegypti
MYLKIVILVTFPLVCFTQDDTPLSKPMAIDYQAEFAWDLYKKLQLGFTQNLAIAPYSLRKIFVCLQQLTV
STNPASAALSEQLKMYLRFNPKGKLPDLVRRRYSSQRAMLERENSFNTTTLAAVIGREKKTNSFWDLPNS
CAIFVGSLRPGSPKQMSRRFNAAMRNISKSGMQNFLSTSDIDRDLDFLIADSWIFKGLWSYQFEEQHTTT
CNFYTNSTSKGLMRFMYLQEYLKYGYFSEWNVEAVELPLHHGSSFSCMLMMPVKADIGVLIKSLNHRRFK
DIYSKMSFSKTDVRLPQFTLRIKFSAKSILQQFGFNAAFNESVFHVFDNKNAVPLGDVIQKVKLVMDHDG
EQSAKMYVDRRMGNLFIAHQPFIFVIFEKTQLVPIIVGHMVTASTPKDIGPESDEISCDRPPRYQ

>gi|56417456|gb|AAV90669.1|_FXa-directed_anticoagulant_precursor_Aedes_albopictus
MNLKIAIIVICQLVYFTQGDTVPSKPLSVDYQAEFSWDLYKKLYPEFRRNMVISPYSLRKIFVCLHQLTD

```

Apenas 10 linhas são printadas utilizando o comando head. Para mudar o número de linhas printadas adicione no comando a opção '-n <INT>', onde '<INT>' é o número de linhas que você deseja que sejam printadas.

Da mesma forma que o comando 'head' printa as primeiras linhas do arquivo, o comando 'tail' printa as últimas linhas do arquivo!


**Atividade:** printe as 20 primeiras e 20 últimas linhas do arquivo 'anti_dec2016.fasta'.


## arquivos fasta, o principal formato de arquivo para sequencias biológicas!
    
Se você ainda não fechou seu terminal, você deve estar confuso com tanta coisa escrita no seu terminal.
    
Pode ser muito gratificante ter a sensação de um terminal novo, sem perder as informações printadas nele. Para isso, utilize o comando 'clear'. E inspecione novamente as 20 primeiras linhas do arquivo 'anti_dec2016.fasta'.
    
```
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ clear
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ head -n 20 anti_dec2016.fasta 
>gi|3411116|gb|AAC31158.1|_FXa-directed_anticoagulant_precursor_Aedes_aegypti
MYLKIVILVTFPLVCFTQDDTPLSKPMAIDYQAEFAWDLYKKLQLGFTQNLAIAPYSLRKIFVCLQQLTV
STNPASAALSEQLKMYLRFNPKGKLPDLVRRRYSSQRAMLERENSFNTTTLAAVIGREKKTNSFWDLPNS
CAIFVGSLRPGSPKQMSRRFNAAMRNISKSGMQNFLSTSDIDRDLDFLIADSWIFKGLWSYQFEEQHTTT
CNFYTNSTSKGLMRFMYLQEYLKYGYFSEWNVEAVELPLHHGSSFSCMLMMPVKADIGVLIKSLNHRRFK
DIYSKMSFSKTDVRLPQFTLRIKFSAKSILQQFGFNAAFNESVFHVFDNKNAVPLGDVIQKVKLVMDHDG
EQSAKMYVDRRMGNLFIAHQPFIFVIFEKTQLVPIIVGHMVTASTPKDIGPESDEISCDRPPRYQ

>gi|56417456|gb|AAV90669.1|_FXa-directed_anticoagulant_precursor_Aedes_albopictus
MNLKIAIIVICQLVYFTQGDTVPSKPLSVDYQAEFSWDLYKKLYPEFRRNMVISPYSLRKIFVCLHQLTD
AKDPATTKFSKQLHKVFKFNPTGQLPDLVRRRYENQREAYAQDQGLNTTTLAVVLGRKKKTTHALNNLPK
SCGIFARSLKSGSPKQMTRSLNAAMKNISNGAAQSFLSESDLNRDWDFFVADSWLFKGFWRYQFEEEYTT
TCNFYTNAKKKGLMRFMYLEEMLRVGHFPQWNVRAVELPLHRESPFSCVLMMPVAADIEELIESLSHKRF
KEIYDNMSASKTTVRLPQFRLRMKLSAKSMLEQLGFDTAFKESVFRVFEKDGAIPLGDAIQKMDLSMAHE
GEDLAKTYVDRSLGQQFTAHQPFMFVIFDRKELVPIIVGNVVAAITPKDVGPQSDEKLCDNPPRFNGR

>gi|56417462|gb|AAV90672.1|_salivary_serpin_putative_anticoagulant_Aedes_albopictus
MNPLVFAVLSVFFVSSIRTQSTSTPPLSDDTHNEFTWIAFKKVSADYKENFVMSPYSLRRLFSCFQGVKL
LSAGAGTNLQQELNSVLNIVPNQQPSGQDHRPYVDQWLRYANAKQLNRTAMAVAIGSEKASSIFDSITNY
CVVYTGYLQPSDGQRMGQVVNDALKKITNNSVLNYLADTDINPNWKFFAIDSWQFDGLWKYKSQEEFTAT
```
Veja que o arquivo possui um padrão. Há múltiplos '>' seguidos por uma descrição e na linha seguinte há várias letras em uppercase.
    
Basicamente, este é o formato fasta e sua estrutra é ilustrada na figura abaixo:
    

<img width="551" alt="Screen Shot 2023-03-08 at 11 24 47 PM" src="https://user-images.githubusercontent.com/46658489/223902873-c94ffeb1-bb6b-4158-8c8c-09003f86d09a.png">

    
 - O character '>' indica o ínicio de uma nova sequência.
 - A descrição da sequencia pode conter o nome do gene, a espécie que a sequência foi isolada e outras informações úteis
 - A sequência pode ocupar múltiplas linhas, e podem ser sequencia de DNA, RNA e proteínas.
    
 **Pergunta:** que tipo de sequências estão armazenadas no arquivo 'anti_dec2016.fasta'.
    
    
 Antes de começar a trabalhar com os arquivos com sequências reais, é uma boa prática fazer o backup dos arquivos. Nós podemos fazer uma cópia do arquivo que contém essas sequencias com o comando 'cp'.
    
```
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ cp anti_dec2016.fasta anti_dec2016_backup.fasta
```
Utilizando o comando ls, você verá que uma cópia desse arquivo foi criada no diretório atual. O segundo argumento é o nome da cópia que será criada. Você pode especificar o path de outro diretório também.

![iludido](https://user-images.githubusercontent.com/46658489/223901880-389d421d-729c-4890-9f3d-b5c32ae3e7fc.jpg)

Você acaba de ser iludido!

Realmente é uma boa prática fazer cópias dos seus arquivos. Mas né, isso é só um exercício. Quem liga?
    
Vamos deletar esse arquivo sobrando aí? Utilize o comando rm para remover arquivos. Acrescente as opções -rf para remover diretórios e tds os seus respectivos arquivos e diretórios. Aproveite e cheque se o arquivo realmente foi deletado!
    
```
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ rm anti_dec2016_backupc.fasta    
```   

## Utilizando 'grep' para inspecionar arquivos
    
É muito comum que durante as atividades de pesquisa em bionformática seja necessário entender muito bem os nossos dados, e conferir se o que nós queremos fazer realmente foi feito.
    
Uma das ferramentais fundamentais para esta atividade é o comando 'grep'. Com este comando é possível buscar por padrões dentro do arquivo de texto. Em princípio, o 'grep' retorna as linhas que contem o padrão procurado.
    
Por exemplo, procure pelo padrão 'Macrobdella' no arquivo 'anti_dec2016.fasta'.
    
```
(base) Rafaels-MacBook-Pro:Linux_tutorial rafael$ grep Macrobdella anti_dec2016.fasta 
>Macrobdella2B10strict38_Ctype_lectin
>Macrobdella10A03strict686_ficolin
>Macrobdella14D11strict26_kazal_type_serpin
>Macrobdella18C11strict18_HIS_ASP_rich
>Macrobdella14F06strict7_HIS_rich
>MacrobdellaN4G11strict45_KGD_disintegrin
>MacrobdellaN4E09strict41_leucocyte_elastase_inhibitor
```
O grep retorna 7 linhas que contem esse padrão. O padrão dado para o grep é exato. Isso quer dizer que ele diferencia uppercase e lowercase.
    
**Exercício:** vamos supor que você queira contar quantas sequencias há no arquivo 'anti_dec2016.fasta'. Como você faria?
    
Esse exercício tem uma pegadinha. o charactere '>' indica o começo de uma nova sequencia, portanto ele é o mais indicado para ser utilizado para contabilizar as sequências em formato fasta. Contudo, esse caractere tem um outro significado em UNIX que eu vou demostrar mais para frente.

Para que o 'grep' entenda que você está procurando por esse padrão, você pode utilizar aspas single ou double para indicar o padrão. Na realidade as aspas single ou double indicam sempre uma sequência de caracteres em quase todas as linguagens de programação. Essas sequências são chamadas de strigs, mas isso a gente vê melhor depois.
    

