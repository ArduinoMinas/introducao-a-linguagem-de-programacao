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
| Divisão | / ou \div ÷ | / |
| Soma | + | + |
| Subtração | - | -|
| Abre chaves ou colchetes | { ou [ | ( |
| Fecha chaves ou colchetes | } ou ] | ) | 
| Raiz Quadrada	| {% math %}\sqrt{x}{% endmath %} | sqrt(x) |
| Ponteciação | x^y | x |


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