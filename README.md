# Miguel_tutorial

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





```

```




```

```
```

```
```

```
```

```
