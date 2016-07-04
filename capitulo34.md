No portugol é possível se comunicar com o mundo esterno apresentando dados através da interface, toda informação externalizada será apresentada na seção "Área de Visualização de Resultados".

Todo programa precisa obter dados, tomar decisções ou calcular sobre tais dados, e externalizar de alguma forma, não faz sentindo um programa que não externalize algo. Para isso o Portugol do VisuAlg tem comandos para leitura de teclado e escrita na tela. Futuramente quando estivermos convertendo nossos algoritmos para Arduino iremos usar as funções e classes do Arduino que nos permite obter dados e se comunicar com o mundo esterno conforme recursos disponíveis.

Vejamos o algoritmo abaixo:

```
algoritmo "exemplo"
var x: real
    y: inteiro
    a: caractere
    l: logico
    c: inteiro const
    
inicio
   x <- 2.5
   y <- 6
   a <- "teste"
   l <- VERDADEIRO
   c <- 5
   escreval ("x", x:4:1, y+3:4) //Escreve: x 2.5 9
   escreval (a, "ok") //Escreve: conteúdo de a seguido de ok (e depois pula linha)
   escreval (a, " ok") //Escreve: conteúdo de a seguido de ok (e depois pula linha)
   escreval (a + " ok") //Escreve: conteúdo de a seguido de ok (e depois pula linha)
   escreva ("valor lógico:", l, ".") // Escreve: VERDADEIRO
fimalgoritmo
```

Veja, fizemos um algoritmo mesmo que de exemplo com a indentação adequada, sempre devemos nos preocupar com isso, nesta apostila iremos sempre cuidar desta prática pois é muito importante.

Nosso foco neste subcapítulo ´e o uso da instrução `escreva` e `escreval`, pois nossa intenção é sempre apresentar dados ao usuário.

A instrução `escreva` permite apresentar dados puramente, ou com certa formação, veja a primeira linha onde ocorre a instrução `escreva`, ela recebe três parametros, ("x", x4:1, y+3:4).

O primeiro parametro "x", é uma simples string e será impresso como é.

Já o segundo parametro, representa a variável ```x``` e os dois numéros separados por ":" (dois pontos) formatam a impressão númerica, dizendo ao comando `escreva` que ele deve imprimir o ```x``` como um numero real, onde o primeiro número, quatro (4), diz o número de casas antes do ponto decimal, se ouver mais casas que números a serem impressoas, será preenchido com espaço em branco. o segundo número, dois (2) informa o numero de casas a ser usado após o ponto, sendo preenchido com zeros a direita se ouver mais casas que a parte fracional a ser preenchida. (faça testes e observe o comportamento do VisuAlg e comente).

E finalmente o terceiro parametro imprime a variável ```y```, mas antes soma o valor 3 a ela, e o valor a seguir separado por 2 pontos funciona como a formatção já explicada no paragrafo anterior, no caso imprime o valor em pelo menos 4 casas, preenchendo com espaço em branco as casas que não são preenchidas com números. (faça testes e observe o comportamento do VisuAlg, e comente).

Veja o valor de y é um **inteiro**, neste caso não tem parte fracional, se tentar formatar a parte fracional, ela será preenchida com zeros conforme o número de casas sugerido, faça alguns testes com esta formatação.

## Salto de Linha.
Como viram existe dois tipos de ```escreva```, o primeiro acrescido de um **l**, e o segundo sem o **l**, o primeiro insere um salto de linha após fazer a impressão do conteúdo solicitado.

Faça testes de formtação com ambos os comando sde escrita na tela.

## Próximo Passo (Próximo subcapítulo)
Agora que vimos como nos comunicar com o mundo externo apresentando dados, veremos no próximo capítulo como solicitar ao mundo externo dados, pedindo ao usuário que digite através do teclado os dados necessários ao nosso algoritmo.