Vamos agora trabalhar com Operações e Funções Matemáticas e para isso é preciso antes de tudo aprendermos como convertermos as formulas matemáticas presentes nos algoritmos testuais e teses acadêmicas que teremos acesso para construir o comportamento de nossos sistemas.

Para convertermos uma formula matemática como esta:

{% math %}
\left\{\left[\frac{2}3-(5-3)+1\right]\right\}.5
{% endmath %}

em um Algoritmo computacional é preciso linearizar as expressões, ou seja transforma-la em uma sequências simples de operações, veja:

{% math %}
{[(2 \div 3) - ( 5 - 3) + 1 ] } .5 [(2÷3)−(5−3)+1].5
{% endmath %}

E posteriormente substituir os operadores matemáticos pelos equivalentes na linguagem escolhida:

{% math %}
( ( ( 2 \; / \; 3) - (5-3) + 1 ) ) * 5 (((2/3)−(5−3)+1))∗5
{% endmath %}

Abaixo apresentamos uma tabela de substituição:

| Descrição | Comum | computacional |
| -- | -- | -- |
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
| Exponênciação	| 3 (maior) |
| Multiplicação | 2 |
| Divisão | 2 |
| Adição | 1 |
| Subtração | 1 (menor) |

Exemplo:

{% math %}
(2 + 2) / 2 = 2 (2+2)/2=2
{% endmath %}

Porém já a formulá:

{% math %}
2 + 2 / 2 = 3 2+2/2=3
{% endmath %}

| Operador Lógico | Prioridade |
| e | 3 |
| ou | 2 |
| nao | 1 |

Resultado falso:

{% math %}
(2 \gt 3) \; ou \; (3 \lt 2) \; e \; (2 \lt 3) = Falso 
{% endmath %}

Resultado verdaeiro:

{% math %}
(2 \gt 3) \; e \; (3 \lt 2) \; ou \; (2 \lt 3) = Verdadeiro 
{% endmath %}

Apesar do VisuAlg não aceitar relacionamento entre tipos de operadores, como matemáticos com Lógicos e Relacionamento, é possível usa-los em uma operação observando o uso correto.

| Operador | Prioridade |
| Aritméticos | 3 |
| Relacionais | 2 |
| Lógicos | 1 |

O uso abaixo está errado:

{% math %}
2 * 5 \gt 3 \; ou \; 5 + 1 \lt 2 \; e \; 2 \lt 7 - 2 
{% endmath %}

Para que a fórmula acima fique correta deve ser escrita da seguinte forma:+

{% math %}
(2 * 5 \gt 3) \; ou \; (5 + 1 \lt 2) \; e \; (2 \lt 7 -2) 
{% endmath %}

## Próximo Passo

Aqui concluimos nosso estudo sobre Algortimo, deste ponto cabe a nós práticarmos, existe ainda um subcapítulo a seguir meramente como referência geral as palavras chaves, comandos e funções proprietárias do Portugol para VisuAlg. 

Continuaremos agora na segunda parte onde iremos aprender a Linguagem C, com alguns ganchos para a Linguagem C++, uma extenção que permite programar orientado a objetos com a a Linguagem C e ainda outros recursos avançados, porém não iremos estudar nada que não seja necessário para uso com o Arduino e seu dialeto Wiring (também conhecido como Linguagem do Arduino)

---
Revisado: 07/07/2016 - 13:00 | Atualizado: 07/07/2016 - 13:00 | Compilado: {{ gitbook.time }}