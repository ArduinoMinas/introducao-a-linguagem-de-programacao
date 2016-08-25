Vimos no portugol os três tipos principais de operadores, lógicos, relacionais e matemáticos, no C eles apresentam pequena diferença em alguns operadores, mas nada muito complicado.

No C também temos um novo tipo de Operador o operador de ponteiros e referências, que nos ajudam a manipular os dados diretamente na memória, acelerando assim seu tratamento, mas não iremos nos aprofundar muito neste tópico, mas precisamos de certa forma nos colocar a pár de seu funcionamento para entender algumas funções do C.

## Operadores Matemáticos

Os operadores matemáticos no C são identicos aos operadores do Portugol, com excessão da potenciação que pode ser expressa usando o simbolo `^`.

Há muitas funções também que podem nos auxiliar nas operações matemáticas, em especial ligadas a trignometria, veremos nos próximos passos algumas bibliotecas de função que irá nos ajudar com procedimentos corriqueiros no C, e neste caso a biblioteca ***Math*** que tem como ponto de entrada o cabeçalho `math.h` veja detalhes no capítulo [Funções Matemáticas no C](funcoesmatematicasnoc.md).

Para relembrarmos segue abaixo a lista dos peradores matemáticos, os valores númericos abaixo podem ser literais (os próprios números), constantes, ou variáveis que sejam do algum tipo númerico:

| Operação | Descrição | Simbolo em C |
| --- | --- | --- |
| Soma | Executa a soma de dois valores númericos. | $$+$$ |
| Subtração | Executa a Subtração de dois valores numéricos. | $$-$$ |
| Multiplicação | Executa a multiplicação de dois valores numéricos | $$*$$ |
| Divisão | Executa a divisão de dois valores numéricos, veja observação abaixo. | $$/$$ |
| Módulo da Divisão | Executa a divisão e retorna o resto da divisão, veja observação abaixo | $$%$$ |

Além dos quatros operadores acima temos o operador de atribuição, quando estudamos o portugol, aprendemos que o simbolo `<-` deveria ser suado para atribuir um valor ou resultado de uma operação para uma variável, já no C, o simbolo que representa tal atribuição é o simbolo `=`.

### Convertendo tipos nas operações matemáticas


Quando fazermos operações matematicas entre dois tipos númericos temos o resultado sempre equivalente ao típo mais complexo presente na operação, portanto se fizermos uma operação matemática entre entre dois inteiros seja qual for teremos um inteiro. Porém se usarmos um inteiro e outro do tipo float, teremos o resultado da operação no tipo float. isso é muito importante quando lidamos com divisão, já que uma divisão entre dois inteiros irá retornar um inteiro sem a parte fracionada, e neste caso é que se torna útil o operador módulo da divisão, com ele obtemos o resto de uma divisão entre dois inteiros.

É importante também entender que o tipo de dado que irá receber o resultado deve ser equivalente ao tipo esperado na operação, no caso da divisão mesmo que ao divir dois inteiros e atribuirmos a um tipo float, o resultado será um inteiro, mas se ao dividirmos um inteiro por um float ou vice versa, teremos um float como resulado mesmo que o valor propriamente pareça ser um inteiro, por exemplo:

$$

X = 8.0/2

$$

Não há dúvida que o resultado será `4` mas não um quatro como inteiro, mas como float, e isso pode nos trazer surpresas, como foi explicado no capítulo anterior sobre a representação do tipos floats um `4.0` pode não ser exatamente o que vemos, mas por exemplo um `4.0000000000001`. a não ser que a variável `x` seja do tipo `inteiro` neste caso o resultado sofrerá um `down casting` de float para inteiro sobrando apenas o valor inteiro da fração, parece obvio quando escrito, mas há muitos programadores que perdem horas tentando descobrir onde está o problema de seu robo que não funciona com certa precisão no arduino porque não teve este cuidado.






---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
