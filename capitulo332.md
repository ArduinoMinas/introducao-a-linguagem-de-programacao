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
 y,c: inteiro
 a: caractere
 l: logico
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



A atribuição de novos valores deve ser feita sempre que oportuna para as variáveis, e no caos das constantes deve ser feito no inicio do algortimo somente. e não se esqueça quando se inicializa as constante se deve usar o simbolo `=` e não o simbolo de atribuição como em variáveis.ç



## Lidado com vetores

No portugol é possível lider com vetores de dados, ou seja uma lista de mesmo tipo de dados, como por exemplo uma coleção de amostras de tempo.

para declarar um vetor de Inteiros por exemplo podemos usar o seguinte comando na seção de declaração de variáveis:

```
const
 MAX_ITEM_TEMP = 10

var
 temperatura: vetor[1..MAX_ITEM_TEMP] de Inteiro
```

No exemplo acima, para ajudar na manipulação do vetor, eu criei uma constante chamada `MAX_ITEM_TEMP`, esta constante contem o tamanho do vetor, e veremos mais a frente porque isso é útil, em segunda na seção `var` declarei o vetor chamado `temperatura` que terá o tamanho de 1 a 10 (conteudo da constante) e será do tipo `inteiro`


## Próximos Passos (Próximo Subcapítulo)

O próximo passo é entender como os dados são apresentados ao usuário utilizando o **"Portugol"** no VisuAlg e em seguida como obter dados do usuário (ler dados externos).

---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
