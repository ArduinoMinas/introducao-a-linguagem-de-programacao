Vamos agora trabalhar com Operações e Funções Matemáticas e para isso é preciso antes de tudo aprendermos como convertermos as formulas matemáticas presentes nos algoritmos testuais e teses acadêmicas que teremos acesso para construir o comportamento de nossos sistemas.

Para convertermos uma formula matemática como esta:

$$
\left\{\left[\frac{2}3-(5-3)+1\right]\right\}.5
$$
em um Algoritmo computacional é preciso linearizar as expressões, ou seja transforma-la em uma sequências simples de operações, veja:

$$
\{[(2 \div 3) - ( 5 - 3) + 1 ] \} .5 
$$

E posteriormente substituir os operadores matemáticos pelos equivalentes na linguagem escolhida:

$$
( ( ( 2 \; / \; 3) - (5-3) + 1 ) ) * 5 
$$

Abaixo apresentamos uma tabela de substituição:

| Descrição | Comum | computacional |
| --- | --- | --- |
| Multiplicação | . ou X | * |
| Divisão | / ou  ÷ | / |
| Soma | + | + |
| Subtração | - | -|
| Abre chaves ou colchetes | { ou [ | ( |
| Fecha chaves ou colchetes | } ou ] | ) | 
| Raiz Quadrada	| {% math %}\sqrt{x}{% endmath %} | sqrt(x) |
| Ponteciação | {% math %}X^Y{ endmath %} | x^y  |


## Prioridades

Como na matemática comum precisamos construir nossas formulas sejam matemáticas ou para operações lógicas observando as precedências dos operadores, e alterando com o uso de parenteses como é comum ser feito.
Abaixo uma tabela de prioridades para os operadores:

| Operador Aritmético | Prioridade |
| --- | --- | 
| Exponênciação	| 3 (maior) |
| Multiplicação | 2 |
| Divisão | 2 |
| Adição | 1 |
| Subtração | 1 (menor) |

Exemplo:

$$
(2 + 2) / 2 = 2
$$

Porém já a formula:

$$
2 + 2 / 2 = 3 
$$

Uma amiga me enviou estes dias uma questão que tem circulado na internet, vamos usa-la para comprender a precedência de um jeito diferente, veja a imagem abaixo:

![Dizem que caiu no concurso da PF](/assets/dizem-que-caiu-no-concurso-da-pf.jpg)

O exercício parece complicado, mas não é, ele é pura matemática vamos resolve-lo e assim praticar um pouco o raciocino lógico e matemático:

Temos primeiro 3 Rosas (`R`) que são igual a 60, então:

$$
R + R + R = 60 \\
3\,\start\,R\,=\,60 \\
R\,=\,60\,/\,3 \\
R\,=\,20
$$

Pronto já sabemos que `R = 20`;

Em seguida temos uma Rosa (R), somada a dois Girassóes (`G`) que é igual a 30:

$$
R \, + G \, + G \, = \, 30\\
20 \, + \, 2G \, = \, 30\\
2G \, = \, 30 \, - \, 20\\
2G \, = \, 10\\
G \, = \, 5
$$

Então o Girassol (`G`) vale 5.

Estemos chegando lá, você vai entender facilmente a precedência daqui a pouco, aprender a prograrm é isso, desmembrar um problema passo a passo e ficar atendo a detalhes.

Agora temos 3 Trevos (`T`) e um Girassol (`G`) que é igual a 41.

$$
T \, + T \, + T \, + G \, = \, 41\\
3T \, + \, 5 \, = \, 41\\
3T \, = \,  36\\
T \, = \, 12
$$

Agora já temos práticamente tudo que precisamos para dar a resposta certa, mas mesmo assim muitos erram e por dois motivos, o primeiro é por total falta de atenção a detalhes, o segundo é simplesmente porque a precedência dos operadores deve ser observada neste desafio, como não nenhum parenteses que muda esta precedência o resultado é totalmente influênciado pela ordem correta usada:

Vejamos então a ultima fórmula, já reduziada e reflita se está certa antes de continuar:

$$ 
5 \, + 20 \, + 9 \, = \, ?
$$

horas, mas o trevo não seria 12 (doze)? porque está o 9 (nove) ali? volte na imagem a cima e certifique do que vê nas duas últimas fórmulas. 

![Recorte da imagem do desafio](/assets/dizem-que-caiu-no-concurso-da-pf-recorte.jpg)

Decobriram? Ok, vou contar então, o trevo na ultima fórmula está com uma folha a menos, portanto das 4 folhas restam apenas 3, ou seja $$\frac{3}{4}$$ do valor do Trevo $$T \star \frac{3}{4}$$.

Sendo assim agora fica apenas a precedência como o último cuidado a se tomado, como a multiplicação tem maior precedência sobre os demais operadores, ela deve ser feito primeiro ficando por tanto:

$$
5 \, + 20 \, + 9 \, = \, X\\
5 \, + \, 180 \, = \, X\\
X \, = \, 185
$$

Sendo assim a respota é a letra "C".

Então fica este desafio para verem como á matemática é importante e o raciocinio lógico também nos ajuda a perceber detalhes queantes passariam desapercebidos.

Vamos continuar agora vendo a precedência dos operadores Lógicos.

| Operador Lógico | Prioridade |
| --- | --- |
| e | 3 |
| ou | 2 |
| nao | 1 |


Resultado falso:

$$
(2 \gt 3) \; ou \; (3 \lt 2) \; e \; (2 \lt 3) = Falso 
$$

Resultado verdadeiro:

$$
(2 \gt 3) \; e \; (3 \lt 2) \; ou \; (2 \lt 3) = Verdadeiro 
$$

Apesar do VisuAlg não aceitar relacionamento entre tipos de operadores, como matemáticos com Lógicos e Relacionamento, é possível usa-los em uma operação observando o uso correto.

| Operador | Prioridade |
| --- | --- |
| Aritméticos | 3 |
| Relacionais | 2 |
| Lógicos | 1 |

O uso abaixo está errado:

$$
2 * 5 \gt 3 \; ou \; 5 + 1 \lt 2 \; e \; 2 \lt 7 - 2 
$$

Para que a fórmula acima fique correta deve ser escrita da seguinte forma:+

$$
(2 * 5 \gt 3) \; ou \; (5 + 1 \lt 2) \; e \; (2 \lt 7 -2) 
$$

## Funções matemáticas

As funções matemáticas são muitas delas ligadas a trignometria, como seno, coseno, e tangente, mas há diversas outras que auxiliam nos cálculos matemáticos como funções que retornam valor avsoluto de um número, o resto da divisão ou a raiz ou logaritmo. Veja a lista abaixo e funções matemáticas disponíveis.



#####Abs( )

##### Div( )

#####  Mod 

##### Quad( )


usado para achar o módulo de um número em comparações (o mesmo que ' % ' )

### Funções trigonométricas

#####Tan( )

#####Sen( )

#####Cos( )

##### Cotan( )

##### ArcCos( )

##### ArcSen( )

### Números randomicos 

##### Rand()

Gera um valor aleatório do tipo Real. Não precisa argumento, o valor aleatório gerado é entre 0 e 1, sendo a precisão de de 15 casas após a virgula, como no exemplo abaixo:

```
0.454236520919949
```

##### Randi(x)

Gera um número aleatório do tipo Inteiro, entre 0 e o valor de x informado como parâmetro.

### Exponenciação e Logarimos

##### Log( )

##### Exp( )

##### Pot( )

##### Raizq( )




## Próximo Passo

Aqui concluimos nosso estudo sobre Algortimo, deste ponto cabe a nós práticarmos, existe ainda um subcapítulo a seguir meramente como referência geral as palavras chaves, comandos e funções proprietárias do Portugol para VisuAlg. 

Continuaremos agora na segunda parte onde iremos aprender a Linguagem C, com alguns ganchos para a Linguagem C++, uma extenção que permite programar orientado a objetos com a a Linguagem C e ainda outros recursos avançados, porém não iremos estudar nada que não seja necessário para uso com o Arduino e seu dialeto Wiring (também conhecido como Linguagem do Arduino)

---
Revisado: {{ file.mtime }}  | Compilado: {{ gitbook.time }}