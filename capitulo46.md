Vimos no portugol os três tipos principais de operadores, lógicos, relacionais e matemáticos, no C eles apresentam pequena diferença em alguns operadores, mas nada muito complicado.

No C também temos um novo tipo de Operador o operador de ponteiros e referências, que nos ajudam a manipular os dados diretamente na memória, acelerando assim seu tratamento, mas não iremos nos aprofundar muito neste tópico, mas precisamos de certa forma nos colocar a pár de seu funcionamento para entender algumas funções do C.

## Operadores Matemáticos

Os operadores matemáticos no C são identicos aos operadores do Portugol, com excessão da potenciação que pode ser expressa usando o simbolo `^`.

Há muitas funções também que podem nos auxiliar nas operações matemáticas, em especial ligadas a trignometria, veremos nos próximos passos algumas bibliotecas de função que irá nos ajudar com procedimentos corriqueiros no C, e neste caso a biblioteca ***Math*** que tem como ponto de entrada o cabeçalho `math.h` veja detalhes no capítulo [Funções Matemáticas no C](funcoesmatematicasnoc.md).

Para relembrarmos segue abaixo a lista dos peradores matemáticos, os valores númericos abaixo podem ser literais (os próprios números), constantes, ou variáveis que sejam do algum tipo númerico:

| Operação | Descrição | Simbolo em C |
| --- | --- | --- |
| Soma | Executa a soma de dois valores númericos. | $+$ |
| Subtração | Executa a Subtração de dois valores númericos. | $-$ |
| Multiplicação | Executa a multiplicação de dois valores númericos | $*$ |
| Divisão | Executa a divisão de dois valores númericos, veja observação abaixo. | $/$ |
| Módulo da Divisão | Executa a divisão e retorna o resto da divisão, veja observação abaixo | $%$ |

Além dos quatros operadores acima temos o operador de atribuição, quando estudamos o portugol, aprendemos que o simbolo `<-` deveria ser suado para atribuir um valor ou resultado de uma operação para uma variável, já no C, o simbolo que representa tal atribuição é o simbolo `=`.

##### Convertendo tipos nas operações matemáticas

Antes de continuarmos é importante compreendermos o que acontece quando envolvemos tipos de dados diferentes em operações matemáticas, temos dois típos de conversão, a conversão do tipo **Down Casting** onde um tipo mais complexo ou de maior precisão é convertido para um tipo de menor tamanho ou precisão. Já a conversão do tipo **Up Casting** faz exatamente o inverso, tipos menos complexos são convertidos em tipos maiores ou mais complexos.


Quando fazermos operações matematicas entre dois tipos númericos temos o resultado sempre equivalente ao típo mais complexo presente na operação, portanto se fizermos uma operação matemática entre entre dois inteiros seja qual for teremos um inteiro. Porém se usarmos um inteiro e outro do tipo float, teremos o resultado da operação no tipo float. isso é muito importante quando lidamos com divisão, já que uma divisão entre dois inteiros irá retornar um inteiro sem a parte fracionada, e neste caso é que se torna útil o operador módulo da divisão, com ele obtemos o resto de uma divisão entre dois inteiros.

É importante também entender que o tipo de dado que irá receber o resultado deve ser equivalente ao tipo esperado na operação, no caso da divisão mesmo que ao divir dois inteiros e atribuirmos a um tipo float, o resultado será um inteiro, mas se ao dividirmos um inteiro por um float ou vice versa, teremos um float como resulado mesmo que o valor propriamente pareça ser um inteiro, por exemplo:

$$

X = 8.0/2

$$

Não há dúvida que o resultado será `4` mas não um quatro como inteiro, mas como float, e isso pode nos trazer surpresas. a não ser que a variável `x` seja do tipo `inteiro` neste caso o resultado sofrerá um `down casting` de float para inteiro.

Sobre a surpresa que podemos ter, é que quando se trata de float, nem sempre um 4 é realmente um 4, ele pode ser um `4.000000000000000001` isso se dá devido ao problema que se tem na forma que o número do tipo float é armazenado internamente, e como pode ver um 4 float pode não ser realmente o 4, e se comparar as operações matemáticas os resutlados apesar de visivelmente identicos, internamente não são, então muito cuidado ao lidar com tipos de dados floats e com `down casting` para outros tipos.


Outro problemas que podemos ter ao fazermos um `down casting` é a perda de dados, por exemplo ao converter um Long para Short, perdemos 2 bytes de precisão, então um valor em hexa como este `0xFEFAFBFC` o que equivale a `4277861372` em decimal, visivelmente um `long` se for feito um downcast para `inteiro` teremos a perda de dois bytes mais significativo, portanto teremos o valor em hexa `0xFBFC` o que equivale em decimal a `64508`.

Como ser visto facilmente com números em hexa, é perdido os dois bytes mais altos, de maior valor (MSB - Most significant Bytes) e isso é uma falha comum quando se lida com sistemas escritos em C, e futuramente quando formos lidar com o Arduino e transmissão de dados, precisamos cuidar atentamente disso.




---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
