# Tutorial Linux 2


Antes seguir para os próximos passos, vamos fazer mais alguns exercícios com o grep.

É possível executar o comando 'grep -E' simplesmente executando o comando 'egrep'. Desta forma, todos os exemplos utilizarão a forma 'egrep'.


## Blast. Uma ferramenta para identificar sequências homólogas

Da mesma forma que nós podemos estabelecer relações de homologia entre estruturas morfológicas, é possível estabelecer relações de homologia entre sequências. Por exemplo, a hemoglobina de humanos é homóloga à hemoglobina de chipanzés. O conceito de homologia em moléculas, no entando, é um pouco mais complexo. Foge do objetivo deste tutorial abordar este conceito, mas nós um uso importante do conceito de homologia entre sequências é a identificação de sequências.

Por exemplo, digamos que você tenha um arquivo fasta, com várias proteínas que são produzidas por uma espécie animal. Você não sabe quais são estas protéinas, mas você tem a sequência. Você pode utilizar o conceito de homologia para identificar estas proteínas e tentar entender possíveis funções destas proteínas.

O conceito de homologia, prediz que proteínas homólogas serão mais similares entre si, do que proteínas não-homólogas. Desta forma, é possível utilizar algorítmos que calculam se a similaridade entre duas sequências é maior do que o esperado por processos aleatórios. O processo é mais complexo do que isso, claro. Mas a linha de raciocínio é esta.

O Blast é um destes programas que são utilizados para estabelecer uma relação de homologia entre sequências. Mais tarde eu vou explicar melhor como o blast funciona, mas nós podemos 



