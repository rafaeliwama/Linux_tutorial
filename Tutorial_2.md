# Tutorial Linux 2


Antes seguir para os próximos passos, vamos fazer mais alguns exercícios com o grep.

É possível executar o comando 'grep -E' simplesmente executando o comando 'egrep'. Desta forma, todos os exemplos utilizarão a forma 'egrep'.


## Blast. Uma ferramenta para identificar sequências homólogas

Da mesma forma que nós podemos estabelecer relações de homologia entre estruturas morfológicas, é possível estabelecer relações de homologia entre sequências. Por exemplo, a hemoglobina de humanos é homóloga à hemoglobina de chipanzés. O conceito de homologia em moléculas, no entando, é um pouco mais complexo. Foge do objetivo deste tutorial abordar este conceito, mas nós um uso importante do conceito de homologia entre sequências é a identificação de sequências.

Por exemplo, digamos que você tenha um arquivo fasta, com várias proteínas que são produzidas por uma espécie animal. Você não sabe quais são estas protéinas, mas você tem a sequência. Você pode utilizar o conceito de homologia para identificar estas proteínas e tentar entender possíveis funções destas proteínas.

O conceito de homologia, prediz que proteínas homólogas serão mais similares entre si, do que proteínas não-homólogas. Desta forma, é possível utilizar algorítmos que calculam se a similaridade entre duas sequências é maior do que o esperado por processos aleatórios. O processo é mais complexo do que isso, claro. Mas a linha de raciocínio é esta.

O Blast é um destes programas que são utilizados para estabelecer uma relação de homologia entre sequências. Mais tarde eu vou explicar melhor como o blast funciona, mas no geral ele estabelece relações de homologia recentes entre sequências de nucleotídeos e proteínas.

Se você quiser entender melhor sobre o blast, consulte o manual do software em: https://www.ncbi.nlm.nih.gov/books/NBK279690/

Hoje, nós vamos instalar o blast, identificar sequências que são possíveis anticoagulantes utilizando como base aquelas sequências que nós isolamos no tutorial passado, e utilizar alguns comandos para analisar os resultados.


## Instalação

Uma das atividades que mais consome o tempo do bioinformata é instalar programas que são utilizados nas análises. Alguns softwares possuem uma instalação bem trabalhosa, mas o blast não é um desses. Exatamente por isso, a primeira coisa que a gente vai instalar é ele.

Caso você esteja utilizando uma distribuição do linux no Windows 10, não se esqueça de se dirigir ao diretório /home

``` 
cd ~
``` 

faco o download do diretório que contém os arquivos do Blast+ com 'wget'.

```
wget https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/2.10.0/ncbi-blast-2.10.0+-x64-linux.tar.gz
``` 
Com wget você pode fazer o download the arquivos apenas com o endereço em que o arquivo está hospedado.

Analise o nome do arquivo que você acabou de baixar. Hint: use o comando ls para listar os arquivos e diretórios.

Repare que o final do arquivo acaba com a sufixo .tar.gz
Arquivos .gz estão comprimidos e arquivos .tar são como diretórios que contém mais de um arquivo. Contudo este formato é especializado na distribuição de arquivos e não na execução e armazenamento.

Para descomprimir e converter arquivos .gz e .tar, utilize o comando 'tar'.

```
tar zxvpf ncbi-blast-2.10.0+-x64-linux.tar.gz
```

Lembre-se que 'zxvpf' são as opções que especificam a função de 'tar'.


Agora, inspecione o contéudo da pasta 'rmblast-2.13.0' utilizando os comandos 'cd' e 'ls'.

```
(base) rafael@malaco:~$ cd rmblast-2.13.0/
(base) rafael@malaco:~/rmblast-2.13.0$ ls
bin  LICENSE.rmblast  README.blast  README.rmblast
```

Perceba que há alguns arquivos com o sufixo '.rmblast' e '.blast'. Estes arquivos contém explicações sobre os softwares pertencentes ao 'Blast+ suite'. Dentro desse diretório, o diretório bin é o mais importante deste programa. Ela contém os arquivos binários que estão associados ao 'Blast+'. 

**Atividade:** inspecione o conteúdo do diretório 'bin'.

Estes arquivos binários são os arquivos executáveis do 'Blast+'. Para você executar estes arquivos, você terá que mudar de diretório atual para o diretório bin e indicar para o prompt que você deseja executar o arquivo binário no diretório em que ele está. Para isso utilize os seguintes comandos:

```
cd bin
./blastp
```

Onde:
bin - diretório que contém os arquivos binários.
./ - indica que você deseja executar o arquivo binário no diretório atual ou no path que você indicar.
blastp - é o software que você deseja executar. Neste caso, o blastp é a versão do blast que aceita sequências de proteína tanto como input, tanto como em sua base de dados.

Como resultado desses comandos, você verá um erro. Isso acontece porque nós utilizados a sintaxe correta do 'blastp'. Mas antes de utilizar-mos o blastṕ corretamente, nós temos que terminar de instalar o programa corretamente.

Assim como os comandos 'cd', 'mkdir', 'cat' ou 'grep' que você digita no terminal, estes programas podem ser chamados da mesma forma
