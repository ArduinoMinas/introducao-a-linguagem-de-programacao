A linguagem C tem alguns tipos de dados extras, além do que vimos no Portugol. Veremos os tipos de dados úteis para quem programa para microcontroladores. Veremos também um pouco sobre Array e como usa-los no C, seu impacto na segurança, e como manipula-los aprendendo assim um pouco sobre ponteiros, mas só o necessário.

## Um pouco mais sobre a manipulação de dados

Como já vimos o computador lida com bits, 8 bits são 1 byte, e 2 bytes um word, 4 bytes um double word e finalmente um quad word são 16 bytes.

Portanto quando armazenamos dados na mémoria o computador estará manipulando tipicamente bytes, seja um byte ou grupos, veremos abaixo que cada tipo de dado na linguagem C tem uma representação típica em bytes, é importantissimo compreendermos como estes dados são armazenados e como são manipulados, veremos para isso os tipos de dados e veremos também os ponteiros para estes típos de dados.

Para entendermos bem como o C manipula os dados na memória e como podemos acelerar este acesso pelo nosso programa, em especial quando lidamos com sequências tipo string, ou até mesmo estruturas de dados é preciso entender a aritmética de ponteiros, porém esta apostila não iremos aprofundar neste assunto por se tratar de um tema avançado.



## Ponteiros

Como já sabemos cada variável ocupa um espaço de momória, este espaço tem o tamanho do tipo de dado utilizado, como vimos no portugol, um tipo inteiro pode ocupar 2 bytes, no C isso pode ser diferente, um tipo como `caracter` é variável no portugol porque guarda sequências que representam texto ou sejam strings de caracteres.

No C, não temos o conceito de string, mas como veremos a frente temos o tipo `char` pode ser um array e assim representar uma string.

Para manipular as variávels de forma mais eficiente, em especial arrays é preciso enteder pelo menos superficialmente o conceito de ponteiro.

Ponteiro é uma referência ao endereço de memória onde está armazenado a variável então referenciada, uma variável do tipo ponteiro pode ser declarada usando o asterisco antes do nome da variável que irá armazenar o endereço, e o tamanho desta variável é compátivel com o espaço de endereçamento de memória. Ou seja se temos um computador que é 16bits teremos um ponteiro de 2 bytes, se for 32bits no ambiente windows comum teremos 4 bytes, e se for 64 bits como nos computadores modernos e windows 64Bits teremos um ponteiro de 8 bytes.

A variável que irá armazenar um ponteiro, deverá ser do mesmo tipo que a variável que será referência do ponteiro, portanto um ponteiro para uma variável do tipo `double` deve ser do mesmo tipo. Abaixo segue uma declaração para um ponteiro do tipo `int`.

```
int *ponteiro;
```

Como vê o simbolo `*` (asterisco) quando antecede uma variável, está informando que ela é um ponteiro para uma posição de memória.

Para se obter a referência para uma variável, devemos usar o simbolo `&` (ampersand) que retorna a posição na memória onde esta variável está sendo armazenada.

Veremos um caso especial que é quando tratamos de arrays, logo a seguir.

## Valor, Referência e Ponteiro quando usar?

%%%%%%%%%%%%%%

## Declarações e Definições

Uma declaração diz ao compilador qual o típo de variável, ou função estamos lidando, no caso do C++ é mais perceptível, já que é preciso que criemos primeiro a declarção do objeto que iremos lidar no programa, esta declação do tipo de objeto é chamado de Classe.

Uma definição aloca um espaço de memória para a variável ou objeto (no caso do C++) ou a implementação da função. 

Podemos ter multiplas declarações por exemplo uma estrutura de dados pode ter diversos espaços de memória alocado para lidar com elas, porém apenas uma única definião é permitido, sendo assim uma variável do tipo Inteiro, ou seja `int` terá apenas uma definição deste tipo, qualquer variação usará uma definição diferente como por exemplo para típos Longo teremos `long`, apesar de serem números são definições diferentes.

Algumas declarações que não são definições como em:

```
extern int i;
int abraPorta(int);
```

Acima temos uma variável sendo declara como sendo do tipo `int`, porém o espaço de memória para ela não foi reservado portanto não foi definido o local de sua existência devido a diretiva `extern` que informa que isso será feito em outro arquivo que compõem nosso programa.

Na segunda linha temos a declação de nossa função, porém ela não foi definida ainda, será definida no mesmo arquivo ou em outro.

Em mabos os casos a compilação ocorre normalmente, porém a mémoria somente é alocada posteriormente quando é feita a Linkedição dos arquivos onde as declarações e definiões são cruzadas para definir a existência do espaço de memória e como estão sendo usados.

## E como tudo isso é guardado na mémoria?

A memória de um programa em C em comum é dividida em três partes muito importantes:

1) Código
2) Heap
3) Stack

Normalmente a área de mémoria onde o programa é armazenado, é a mémoria ROM e não sofre nenhum tipo de alteração durante a execução, porém os outras seções de memória são alocados de forma bem distintas e são usados também de forma bem especificas.

O HEAP normalmente é alocado no início da mémoria RAM, e o Stack no final da memória, e ambos crescem em direção um ao outro.

O Heap é usado para armazenar variáveis globais e estáticas e outras criadas especialmente através de alocação de mémoria, como veremos a frente, já o Stack é usado para armazenar variáveis locais e estado de funções que chamam outras funções sendo assim recuperadas tais informações quando a função retoma o controle.

O Heap vai crescendo conforme é ocupado e pode ser fragmentado, se o algoritmo de alocação de memória não for bem implementado, e isso não é uma preocupação que teremos pois o C que usáremos já tem um alocador que cuidará de tudo para nós.

Já o Stack é uma fila do tipo: primeiro a entrar primeiro a sair, ou seja FIFO. Portanto, nunca se fragmenta, mas se ouver muitas funções encadeadas ou com longa recursividade, com grande número de variáveis locais pode ocorrer o que chamamos de estouro da pilha, e assim esta pode vir a sobreescrever o Heap, como vimos um cresce em direção ao outro, hoje isso é raro de ocorrer uma vez que os computadores tem muita mémoria, mas quando se trata de microcontroladores onde memória é um recurso escasso, é preciso ter muito cuidado, principalmente com funções recursivas.

## A seguir

Neste capítulo temo sais três subcapítulo que nos apresentaram conceitos ligados a visibilidade, ao tempo de vida das variáveis, seu conteúdo e também os tipos de dados.

---
Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
---

