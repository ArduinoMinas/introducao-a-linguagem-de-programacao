Agora nosso estudo vai começar a ficar mais divertido, pois passaremos a ter maior controle sobre o algortimo, é aprenderemos a fazer com que o computador faça exatamente o que queremos, conforme dados forem fornecidos a ele. Este aprendizado é muito importante e será usado ao longo de toda a sua vida como desenvolvedor de softwares e firmwares (código para microcontroladores e hardware).

## Operadores Lógicos e Relacionais
Iremos antes de tudo aprender o que são operadores lógicos e relacionais, assim poderemos usa-los com facilidade com as instruções de controle.

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

### Controles lógicos

### Laços (loops)
