Vejamos neste capítulo o que são variáveis e constantes, e quais os tipos podem ser usados no Portugol.

Em toda linguagem de programação temos tipos de dados, algumas não levam isso em consideração deixando que o usário transforme as variáveis de um tipo a outro no decorrer da execução de código, isso pode ser bom, ou ruim, depende da disciplina do programador, não iremos discutir esta prática agora, e usaremos linguagens fortemente tipadas, ou seja, uma vez declarado o dito de dado que será depositado na variável, a tentativa de usar outro tipo irá acarretar erros.

Não veremos ainda como os dados são armazenados na memória do microcontrolador ou do computador, apenas entenderemos que tipo de dado, seus valores limites e como lidar com cada tipo de variável. Tal entendimento será absorvido no decorrer do uso de cada variável, mas quando iniciarmos os estudos da linguagem C/C++ será necessarío compreender mais a fundo como tais veriáveis são representadas na memória ou registradores.

## Como tudo é manipulado no computador.

Você já deve ter ouvido falar de Byte, Bit, e já deve saber que o computador se comunica atráves de eletricidade, com sinais ligados ou desligados, em especial em barramentos de memória, onde isso trafega em uma alta taxa de velocidade, chegando a velocidades inimagináveis a uma decada atrás, temos processadores ultrapassano a taxa do Ghz, ou seja 1 bilhão de alterações de estados entre 1 e 0 (ligado e desligado) e um dos fios do barramento.

Além disso vemos hoje processadores cada vez maiores sendo capazes de lidar com uma quantidade de Bits simultaneos cada vez maior, o primeiro processador era capaz de lidar com os incriveis 8 bits ou seja um byte, hoje temos computadores com 64bits seja 8 bytes o que permite  capacidades absurdas de endereçamento de mémoria, a incrível capacidade de 18.446.744.073.709.551.616 (18.446 Teras) posições de memória de tamnhos típicos de um byte.

Bem, como podem perceber o bit é a menor unidade que um computador consegue lidar hoje, é representado por 0 e 1, já um conjunto de 8 bits é chamado de Byte, e será a unidade que mais usaremos, há também i niple que representa metade de 1 byte, ou seja 4 bits.

Temos também ```world``` que representam 2 bytes, e ```double world``` para 4 bytes e ```quad world``` para 8 bytes.

No universo dos microcontroladores isso não muda, são as mesas medidas, porém microcontroladores tipo PIC e AVR são normalmente de 16 bits de endereçamento apesar de lidar com 8 bits por vez, há microcontroladores como o ARM que lidam com 32bits e barramentas de endereço do mesmo tamanho, mesmo que não tenham toda a mémoria disponível realmente, parte dela é usada como dispositivos de entrada e saida, e como barramentos de comunicação com ouors dispositovos internos. Veremos isso na [apostila de micro controladores](mcu.ed.carlosdelfino.eti.br)

## Variáveis vs Constantes

Um conceito muito importante a se compreender é a diferença entre Variáveis e Constantes, como o própiro nome sugere, variável é passivel de alteração já as constantes não, esta ultima, uma vez atribuida não poderá mais ser alterada, em contra partida as variáveis podem ser alteradas ilimitadamente sem nenhuma perda de sua qualidade.

As variáveis devem ser usadas para armazenar dados que serão regularmente alterados ou não, que por exemplo será informado spelo usuário, mesmo que não sejam alterados durante a execuçaõ do programa, mas será alteradas depois de sua declaração por uma entrada por exemplo.

As constantes devem ser usadas para armazenar dados que será regularmente usados no programa,como por exemplo um fator constante de conversão para um calculo, facilitando assim o uso da formula, um bom exemplo seria o valor de "PI" que ficar armazenado na constante de mesmo nome.

## E o que são tipos de dados?

Tipos de dados é o formato do dado a ser armazenado, este dado pode ser um número, uma letra, ou uma sequência de letras, formando assim uma palavra ou frase.

Os números podem ter diversos tipos, por exemplo, podemos ter números inteiros de 0 a 255, observando os limites do computador no caso de compuadores/microcontroladores de 8 bits, podemos ter números inteiros de 0 a 65536 já mais facilmente trabalhado por computadores/microcontroladores de 16 bits, e também podemos ter também números fracionados, do tipo longo ou de ponto flutuante como utilizados na engenhária.

Vejamos então quais são os tipos de dados que o Portugol pode trabalhar sem problemas, lembrando que Portugol é uma pseudo linguagem, portanto ela terá tipos que independem do computador utilizado.

### Tipos númericos

##### inteiros
A diretiva **inteiro** define variáveis numéricas do tipo inteiro, ou seja números que não tenha casas decimais, podendo armazenar aproximadamente o valor entre 2147483647 e -2147483648

Exemplos de uso: idade, número de filhos, quantidade de estados do Brasil.

##### Real
Define variáveis numéricas do tipo real, ou seja, com casas decimais. Conforme norma IEEE 754.

Valor máximo: 356 x e ^-43

Exemplos de uso: salário, peso, temperatura.

**ATENÇÃO** As constantes são sempre inteiro, não existindo o tipo Real para elas, portanto mesmo que venha usar o valor fracionado, declare as constantes como sendo `inteiro`

### Outros tipos
##### Caractere
Define variáveis do tipo string, ou seja, cadeia de caracteres.

Exemplo de uso: nome, endereço, frase

##### Lógico
Define variáveis do tipo booleano, ou seja, com valor VERDADEIRO ou FALSO.

O VisuAlg permite também a declaração de variáveis estruturadas através da palavra chave vetor.

Por hora lidar com estes tipos nos será suficiente, vamos usa-los para desenvolver nossa habilidade em escrever algoritimos básicos de tratamento de dados, calculos e conversões conforme circunstãncias bem controladas.

## Declarando as variáveis e Constantes.


Vimos anteriormente como é a estrutura de um algoritimo, mas vamos rever como declarar variáveis aqui para fixarmos este procedimento no Portugol do VisuAlg.

Sempre a declação de um bloco de variáveis, seja global ou local, deve ser feito com a diretiva `var` precedendo o bloco, seguido dos nomes das variáveis separados por virgula e finalizando com *:* seguido do tipo de variável.

Quando constante deve ser utilizado a diretiva `const` no final da linha, finalizando a declaração, vejam o exemplo a seguir:

```
var x: real
    y: inteiro
    a: caractere
    l: logico
    c: inteiro
```

Para se declarar uma constant, basta declaralas na seção constante, listando cada constante em uma linha atribindo seu valor com operador igual `=`

```
const
   notaMinima = 70
   notaMaxima = 100
   opcaoFixa = `A`
```

Defina as constantes antes das variáveis.

## Atribuindo Valores as Variáveis e Constantes

A Atribuição de valores as variáveis, e a inicialização das constantes, devem ser feitas com o símbolo `<-`, simbolo de *menor que* seguido de um *ífem*, sem espaços entre os dois.

A atribuição de novos valores deve ser feita sempre que oportuna para as variáveis, e no caos das constantes deve ser feito no inicio do algortimo somente.

## Próximos Passos (Próximo Subcapítulo)
O próximo passo é entender como os dados são apresentados ao usuário utilizando o **"Portugol"** no VisuAlg e em seguida como obter dados do usuário (ler dados externos).

---
Atualizado: 12/07/2016 - 11:00 | Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}

