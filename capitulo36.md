Agora nosso estudo vai começar a ficar mais divertido, pois passaremos a ter maior controle sobre o algortimo, é aprenderemos a fazer com que o computador faça exatamente o que queremos, conforme dados forem fornecidos a ele. Este aprendizado é muito importante e será usado ao longo de toda a sua vida como desenvolvedor de softwares e firmwares (código para microcontroladores e hardware).

## Operadores Lógicos e Relacionais
Iremos antes de tudo aprender o que são operadores lógicos e relacionais, assim poderemos usa-los com facilidade com as instruções de controle.

mas antes de continuarmos, precisamos conhecer duas constantes muito importantes:

* `VERDADEIRO`
* `FALSO`

São auto descritiveis e podem ser usadas para auxiliar na composição de expressões lógicas em instruções de controle de fluxo (execução de blocos) e instruções de controle de laço.

### Operadores Relacionais 

| Operador | descrição      |  Teste  | Resultado   |
|    --    |     --         |    --   |     --      |
|    =     | Igual          | 2  = 2  | verdadeiro  |
|          |                | 1  = 5  | falso       |
|   <>     | Diferente      | 3 <> 3  | falso       |
|          |                | 2 <> 4  | falso       |
|    <     | Menor          | 1  < 5  | verdadeiro  |
|          |                | 3  < 2  | falso       |
|    >     | Maior          | 1  > 5  | falso       |
|          |                | 3  > 2  | verdadeiro  |
|   <=     | menor ou Igual | 2 <= 7  | verdadeiro  |
|          |                | 4 <= 4  | verdadeiro  |
|          |                | 8 <= 3  | falso       |
|   >=     | maior ou Igual | 2 >= 7  | falso       |
|          |                | 4 >= 4  | verdadeiro  |
|          |                | 8 >= 3  | verdadeiro  |

### Operadores Lógicos

| Operador | descrição      |  Teste  | Resultado   |
|    --    |     --         |    --   |     --      |
| Nao | Operador unário de negação, tem maior precedencia sobre os demais operadores, faz a inversão da lógica, ou seja, verdaeiro se torna falso e falso verdadeiro | nao 2 = 2 | falso |
|  ou | Operador similar a soma binária, quando um dos valores for verdadeiro ou ambos forem, retorna verdadeiro          | verdadeiro ou verdadeiro  | verdadeiro |
|     |                     | falso ou verdadeiro       | verdadeiro |
|     |                     | falso ou falso            | falso |
|  e  | Operador similar a multiplicação binária, apenas quando ambos os valores forem verdadeiro, retorna verdadeiro          | verdadeiro e falso        | falso |
|     |                     | verdadeiro e verdadeiro   | verdadeiro   |
| xou | Operador similar ao `ou`, porém apenas retorna verdadeiro se somente um dos valores forem verdadeiros                 | verdadeiro xou verdadeiro | falso      |
|     |                     | verdadeiro xou falso      | verdadeiro |
|     |                     | falso xou falso           | falso      |


### Controles de Desvios
Iremos ver dois controles de desvios de execução, que nos ajudará a dar mais inteligência ao nosso Algortimo. O primeiro um desvio por decisão com base em expressões lógicas, muito indicado para tomada de decisões, e já deixo aqui um gancho para pesquisas de algortimos avançados como o "C4.5", não veremos tais algortimos em nosso curso, então vamos ao nosso primeiro controle o `se`, em seguida veremos o comando `escolha`, um controle de seleção multipla.

### Se

O comando `se` espera em seguência uma expressão lógica que irá definir "se" executará "então" um bloco de código, seja de apenas uma linha, ou seja de muitas linhas, ou "se não" executará outro bloco.

A estrutura padrão do comando é:

```
se m < 7.0 entao
   Escreva ("Em EXAME")
Senao
   Escreva ("APROVADO")
fimse
```
No pedaço de algortimo acima, temos o seguinte algortimo interpretado: Se "m" menor que o valor real 7.0 então escreva "Em EXAME" na tela, agora se "m" não for menor nem igual, então, escreva "APROVADO" na tela.

É possível inserir uma estrutura de decisão dentro da outra, veremos tal prática com exercícios.

### Escolha
o comando `escolha` em algumas situações é melhor que o comando `se`, quando temos uma quantidade de analise de decisão maior, como por exemplo em códigos de menu, ou que receba caracteres como resposta e precisa tomar decisões.

Vejamos um exemplo da estrutura do uso do `escolha`:

```
escolha acao
   caso "correr", "andar"
      escreverl("vou andar")
   caso "pular"
      escreverl("vou pular")
   outrocaso
      escreverl("faço o que tiver vontade")
fimescolha
```

Como podem ver o comando `escolha` permite diversos casos, no **Portugol** do **VisuAlg**, não executam um após outro apartir do escolhido, mas cuidado o outras linguagem como o C/C++ exige um comando de interrupção.

No comando `escolha` também podendo ter uma opção `outrocaso` que será executado caso nenhuma outra opçao seja identificada.

### Controles de Laços (loops)

Alguns blocos de código precisam ser executados durante um periodo de tempo ou enquanto uma determianda condição não é atingida. Para isso existens duas instruções no **Portugol** que nos permitem controlar de forma diferente um bloco de código.

#### Enquanto

a instrução de controle de laços `enquanto`, é usada para permitir a execução de um bloco de instruções finitamente, antes de cada execução do bloco uma condição é analisada, enquanto ela retornar verdadeiro.

Vejamos como é a instrução de forma completa:

```
algoritmo "demonstracao enquanto"
Var
   contador: inteiro

inicio
   contador <- 1
   escreval("Começando Enquanto:",contador)
   enquanto contador < 20 faça
      escreval(contatodor)
      contador = contador + 1
   fimenquanto
   escreva("Equanto Finalizado:",contador)
fimenquanto
