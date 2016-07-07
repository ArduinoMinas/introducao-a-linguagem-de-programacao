Operações e Funções Matemáticas

Para convertermos uma formula matemática como esta:
\left\{\left[\frac{2}3-(5-3)+1\right]\right\}.5{[
​3
​
​2
​​ −(5−3)+1]}.5
em um Algoritmo computacional é preciso linearizar as expressões, ou seja transforma-la em uma sequências simples de operações, veja:
{[(2 \div 3) - ( 5 - 3) + 1 ] } .5 [(2÷3)−(5−3)+1].5
E posteriormente substituir os operadores matemáticos pelos equivalentes na linguagem escolhida:
( ( ( 2 \; / \; 3) - (5-3) + 1 ) ) * 5 (((2/3)−(5−3)+1))∗5
Abaixo apresentamos uma tabela de substituição:
Descrição	Comum	computacional
Multiplicação	. ou X	*
Divisão	/ ou \div ÷	/
Soma	+	+
Subtração	-	-
Abre chaves ou colchetes	{ ou [	(
Fecha chaves ou colchetes	} ou ]	)
Raiz Quadrada	\sqrt{x} √
​x
​
​​ 	sqrt(x)
Ponteciação	x^y x
​y
​​ 	x^y
Prioridades

Como na matemática comum precisamos construir nossas formulas sejam matemáticas ou para operações lógicas observando as precedências dos operadores, e alterando com o uso de parenteses como é comum ser feito.
Abaixo uma tabela de prioridades para os operadores:
Operador Aritmético	Prioridade
Exponênciação	3 (maior)
Multiplicação	2
Divisão	2
Adição	1
Subtração	1 (menor)
Exemplo:
(2 + 2) / 2 = 2 (2+2)/2=2
Porém já a formulá:
2 + 2 / 2 = 3 2+2/2=3
Operador Lógico	Prioridade
e	3
ou	2
nao	1
Resultado falso:
(2 \gt 3) \; ou \; (3 \lt 2) \; e \; (2 \lt 3) = Falso (2>3)ou(3<2)e(2<3)=Falso
Resultado verdaeiro:
(2 \gt 3) \; e \; (3 \lt 2) \; ou \; (2 \lt 3) = Verdadeiro (2>3)e(3<2)ou(2<3)=Verdadeiro
Apesar do VisuAlg não aceitar relacionamento entre tipos de operadores, como matemáticos com Lógicos e Relacionamento, é possível usa-los em uma operação observando o uso correto.
Operador	Prioridade
Aritméticos	3
Relacionais	2
Lógicos	1
O uso abaixo está errado:
2 * 5 \gt 3 \; ou \; 5 + 1 \lt 2 \; e \; 2 \lt 7 - 2 2∗5>3ou5+1<2e2<7−2
Para que a formula acima fique correta deve ser escrita da seguinte forma:+

(2 * 5 \gt 3) \; ou \; (5 + 1 \lt 2) \; e \; (2 \lt 7 -2) (2∗5>3)ou(5+1<2)e(2<7−2)

