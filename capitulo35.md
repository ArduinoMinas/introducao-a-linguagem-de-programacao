Raramente um algortimo não precisa interagir com o mundo externo, e raramente ele não terá que obter dados, pois é através da variação de dados externos que o programa reage e assim apresenta novas alternativas e resultados.

Para obtermos dados do mundo externos iremos usar um comando muito prático do Portugol para VisuAlg, o comando `leia` ele pode ser considerado o inverso do comando `escrever` já que ao invez de imprimir o conteúdo de uma variável na tela, ele irá ler do teclado em uma varíavel o que for digitado até que se tecle enter.

Ao usar o comando `leia` o VisuAlg espera que seja digitado algum dado compátivel a variável informada como parametro. Você pode informar mais de uma variável para que sejam digitadas em sequência.

Caso seja digitado um dado incomátivel com o valor esperado, este é ignorado, por exemplo, se é esperado um `inteiro` e é digitado um um caracter, este dado será ignorado e descartado, atribindo 0 a variável que foi informada.

Veja o exemplo abaixo:

```
algoritmo "teste"
// Autor: Carlos Delfino (consultoria@carlosdelfino.eti.br)
// demonstra como usar o comando leia, com uma ou mais variáveis.

// variáveis globais   podes aumentar [1..?] pra quantos quiser
Var
   var1, var2, var3: inteiro
   var4, var5: caracter

inicio
   escreva("Digite algo e veja o resultado a seguir")
   leia(var1)
   escreval("Você digitou: ",var1)
   escreva("Digite 3 dados e enter a seguir)
   leia(var2,var3,var4)
   escreval("você digitou: ",var2:4,var3:4)
   escreva("Agora vamos reaproveitar uma das variáveis, insira um breakpoint aqui e veja 'area de das variáveis de memória, como o conteúdo é alterado', digite dois dados e enter para cada um deles")
   leia(var5,var1)
   escreval("Você digitou: ", var5:10, var1:10)
fimalgoritmo
```
Vamos aproveitar o momento e analisar o comportamento também do comando `escreva` e `escreval`, é nestes momentos que descobrimos peculiaridades da linguagem usada. Faça testes.
