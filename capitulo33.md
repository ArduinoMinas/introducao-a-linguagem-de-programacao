Vejamos neste capítulo o que são variáveis e constantes, e quais os tipos podem ser usados no Portugol.

Em toda linguagem de programação temos tipos de dados, algumas não levam isso em consideração deixando que o usário transforme as variáveis de um tipo a outro no decorrer da execução de código, isso pode ser bom, ou ruim, depende da disciplina do programador, não iremos discutir esta prática agora, e usaremos linguagens fortemente tipadas, ou seja, uma vez declarado o dito de dado que será depositado na variável, a tentativa de usar outro tipo irá acarretar erros.

Não veremos ainda como os dados são armazenados na memória do microcontrolador ou do computador, apenas entenderemos que tipo de dado, seus valores limites e como lidar com cada tipo de variável. Tal entendimento será absorvido no decorrer do uso de cada variável, mas quando iniciarmos os estudos da linguagem C/C++ será necessarío compreender mais a fundo como tais veriáveis são representadas na memória ou registradores.

### Variáveis vs Constantes
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

### Outros tipos
##### Caractere
Define variáveis do tipo string, ou seja, cadeia de caracteres.

Exemplo de uso: nome, endereço, frase

##### Lógico
Define variáveis do tipo booleano, ou seja, com valor VERDADEIRO ou FALSO.


O VisuAlg permite também a declaração de variáveis estruturadas através da palavra chave vetor.

Por hora lidar com estes tipos nos será suficiente, vamos usa-los para desenvolver nossa habilidade em escrever algoritimos básicos de tratamento de dados, calculos e conversões conforme circunstãncias bem controladas.

## Atribuindo Valores as Variáveis e Constantes
A Atribuição de valores as variáveis, e a inicialização das constantes, devem ser feitas com o símbolo `<-`, simbolo de *menor que* seguido de um *ífem*, sem espaços entre os dois.

A atribuição de novos valores deve ser feita sempre que oportuna para as variáveis, e no caos das constantes deve ser feito no inicio do algortimo somente.

## Próximos Passos (Próximo Subcapítulo)
O próximo passo é entender como os dados são apresentados ao usuário utilizando o **"Portugol"** no VisuAlg e em seguida como obter dados do usuário (ler dados externos).
