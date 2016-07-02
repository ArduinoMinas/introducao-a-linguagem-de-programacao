No portugol é possível se comunicar com o mundo esterno apresentando dados através da interface, toda informação externalizada será apresentada na seção "área de Visualização de Resultados".

Todo programa precisa obter dados, tomar decisções ou calcular sobre tais dados, e externalizar de alguma forma, não faz sentindo um programa que almenos externalize algo. Para isso o Portugol do VisuAlg tem comandos para leitura de teclado e escrita na tela. Futuramente quando estivermos convertendo nossos algoritmos para Arduino iremos usar as funções e classes do Arduino que nos permite obter dados e se comunicar com o mundo esterno conforme recursos disponíveis.

Vejamos o algoritmo abaixo:

```
algoritmo "exemplo"
var x: real
    y: inteiro
    a: caractere
    l: logico
inicio
   x <- 2.5
   y <- 6
   a <- "teste"
   l <- VERDADEIRO
   escreval ("x", x:4:1, y+3:4) //Escreve: x 2.5 9
   escreval (a, "ok") //Escreve: teste ok (e depois pula linha)
   escreval (a, " ok") //Escreve: teste ok (e depois pula linha)
   escreval (a + " ok") //Escreve: teste ok (e depois pula linha)
   escreva ("valor lógico:", l, ".") // Escreve: VERDADEIRO
fimalgoritmo
```

Bem, veja, fizemos um algoritmo mesmo que de exemplo com a indentação adequada, sempre devemos nos preocupar com isso, nesta apostila iremos sempre cuidar desta prática pois é muito importante.

Nosso foco neste subcapítulo ´e o uso da instrução "escreva" e escreval", pois nossa intenção é sempre apresentar dados ao usuário.

a instrução Escreva permite apresentar dados puramente, ou com certa formação, veja a primeira linha onde ocorre a instrução "escreva", ela recebe três parametros, ("x", x4:1, y+3:4).

O primeiro parametro "x", é uma simples string e será impresso como é.

Já o segundo parametro, representa a variável ```x``` e os dois numéros separados por ":" (dois pontos) dizem ao escreva que ele deve ser impresso como um numero real, com casas decimais e 
