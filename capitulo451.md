Estudaremos neste capítulo sobre o tempo de vida dentro da linguagem C de suas variáveis. O que é escopo e como isso interfere em seu uso nos blocos de controle, blocos de decisão, e dentro de funções.

## Escopo da variável e Ciclo de vida 

O escopo de uma declaração é o espaço do programa no qual uma declaração tem efeito, qual a visibilidade desta declaração, até onde esta declaração pode ser manipulada pelas partes do programa.

O escopo de uma declaração é a parte do programa no qual a declaração tem efeito, sendo assim podemos ter declarações similares em diversas parte do programa desde que o efeito de uma não interfira na existência de outra.

Sendo assim podemos usar blocos de códigos delimitados por pares de chaves `{}` para que tenhamos declarações limitadas ao bloco fechado pela chaves. este tipo de declaração é conhecido como local, ou seja, somente visivel no local onde a variável é declarada. Naquele bloco. 

### Lifetime (tempo de vida)

O tempo de vida de uma variável também pode ser chamado de "Método de Alocação" ou "Duração do Armazenamento", pois define até quando apartir do momento que é criada, que ela existirá em seu programa.

Uma variável pode ter seu tempo de vida definido de forma automática, ou seja desde que foi declarada ela será gerida pelo próprio ambiente, não sendo necessário nos preocuparmos com sua existência, isso se dá com variáveis que não são alocadas através do uso de alocadores especializados como veremos a frente. Estas variáveis são armazenadas típicamente no stack das funções, portanto as variávies definidas como local são variáveis "Automáticas" seu tempo de vida são alto geridos.

Já as variáveis dinâmicas tem um tempo de vida definido pelo programador quando este usa um alocador especifico como a função "malloc()" e termina quando o programador deseja ou quando o programa finaliza todas os processos e threads que iniciou. O programador normalmente descarta uma variável alocada dinâmicamente com o uso do da função "free()", os objetos dinâmicos são todos armazenados no Heap, devido a isso é importante ter muito cuidado com seu uso, pois a fragmentação do "heap" pelo uso de variáveis de diferentes tamanhos pode vir a consumir toda a memória.

Tudo isso no íncio parece ser muita coisa a se preocupar, mas não se preocupe faça seus primeiros programas declarando suas variávies da forma que acha mais adequado, com o decorrer da experiência adquirida irá buscar soluções mais profissionais e entenderá cada vez mais profundamente tais conceitos e os usará adequadamente.

Apenas evite criar muitas variáveis globais e quando for usar variáveis locais procure também cuidar adequadamene delas para evitar uma sobrecarga do código deixando o lento, veja que também muitos parametros não é bom.

### Escopo

Como vimos, O escopo de uma declaração é o espaço do programa no qual uma declaração tem efeito, qual a visibilidade desta declaração, até onde esta declaração pode ser manipulada pelas partes do programa.

Sendo assim temos no C os seguintes escopos e suas definições

#### Local

O escopo local é a visibilidade apenas dentro do bloco onde a variável foi definida, ou seja dentro das chaves `{}`, sendo assim ao termino de execução deste bloco a variável deixa de existir, veja a baixo como mudar isso.

Não veremos detalhes de programação orientado a objeto com C++, mas temos também o escopo da classe, onde uma variável é vista apenas dentro de sua classe por seus membros, sendo assim privado.

Também no C++ temos o escopo de nome de espaço ou seja "Namespace scope", onde a visibilidade se limita ao nome de espaço onde a classe e função está sendo definido, seu funcionamento é similar a declaração de variáveis de escopo local, já que são delimitadas pelas chaves `{}`.

O próximo escopo é o que se refere ao arquivo onde está sendo declaro, uma vez a variável definida sem nenhum parametro extra ela será global, mas como veremos a frente, se usarmos o parametro `static` ela se torna visível apenas no arquivo.


E para o nosso estudo teremos finalmene o escopo global (não terminamos aqui, porém para nosso foco é o suficinete, já que não iremos aprofundar na programação orientada a objetos com C++)

O Escopo global dá visibilidade em toda a aplicação e deve ser usado com muita cautela para não haver conflitos e assim surpresas no comportamento de seu programa, use as variáveis globais apenas quando for realmente necessária e cuidado com sua incialização e inversões em seus valores já que uma vez tendo seu valor alterado em um local todos os demais verão este novo valor.

Não poderão haver mais de uma variável global com o mesmo nome em seu aplicátivo mesmo que declarada em arquivos diferentes, e cuidado com o uso da diretiva static como veremos a seguir, já que pode haver conflitos de nomes de forma indesejada.

### Declarações Estáticas no C

A declaração de uma variável ou função como estática tem comportamentos bem diferentes conforme o local onde é feito. Vejamos cada caso.

### C/C++ usa Escopo Lexico

O escopo lexico é a definião do escopo conforme sua declaração, sendo assim indica que a variável tem o escopo conforme o local que é criado, não sendo permitida sua manipulação em camadas superiores.

O outro escopo que está em desuso é o escopo dinâmico que define o escopo conforme a variável é usada, podendo causar muita confusão, já que uma variável quando usada em uma funão mesmo que declarada em outra função pode ter valores imprevisíveis se perdemos a linha de raciociono de onde foi usado a variável com o mesmo nome.

#### Variáveis com delcaração "static" em blocos de código

Considerando que a declaração está sendo usada em um bloco de código qualquer, seja no inicio da definição da função ou seja mais internamente em um bloco de controle, o tempo de vida de uma variável declarada como `static` passa a ser bem diferente, a variável é alocada normalmente na memória (mas não no stack e sim no heap) e passa a existir quanto a função ainda for chamada em outras partes do programa, com isso ela não perde seu valor e não deixa de existir quando a função é finalizada e retorna ao ponto onde foi chamada, numa próxima interação com a função a variável não é criada novamente, mas sim reutilizada com seu último valor, e se ela foi inicializada durante a criação, não é inicializada novamente.

Veja no exemplo:

```c
void umaFuncao(){
    static int contador = 1;
    // faz qualquer coisa
    // interfere no contador
    contador++;
}
```
Neste exemplo a variável contador será inicializada quando a função for chamada a primeira vez e conterá o valor um (1), então será, na quarta linha, acrescido de um ( contador = contador + 1), e finalmente a função retorna, em tese, por ser uma variável definida dentro da função em seu bloco de código, ela somente irá existir ali e quando a função sair, a variável seria descartada e o espaço de memória poderia ser reutilizado (veremos mais sobre stack e heap a seguir).  

Mas como ela foi declarada como sendo static, ela será criada na primeira chamada da função e perpetuada por todo o programa, mantendo assim seu valor em cada nova chamada da função, não sendo mais inicializada. 

Portanto na terceira chamada da função ela terá o valor 4, já que foi inicializada com na primeira chamada, e a cada chamada somada em um em seu valor através do operador unário `++`.


#### Variáveis e funções declaradas como stática no contexto do arquivo.

Quando uma variável é declarada como "statica" fora de um bloco de comandos `{}` ou seja fora de uma função, ela está sendo declarada que pertence a aquele arquivo apenas, ou seja, é uma variável global mas de scopo reduzido e limitado ao arquivo em questão.

Isso é muito útil quando precisamos de uma variável que é compartilhada entre as funções que são definidas em uma aquivo, não sendo necessária fora deste contexto.

Assim podemos escrever:

```c
static int variavel1;

void funcao1(){
    // interage com  variavel1;
    funcao2();
    // interage com variavel1;
}

void funcao2(){
    // itnerage com variavel1;
}
```

No exemplo acima a `variável1` é vista apenas dentro do arquivo onde ela é declarada e é global para todas as funções ali também decladas, com isso não precisamos passar como parametro seus valores, nem referências.

---
Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
---
