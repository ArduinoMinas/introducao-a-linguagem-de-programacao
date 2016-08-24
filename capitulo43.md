Iremos neste capítulo entender como se deve escrever um código em C, e o que é cada parte. Iremos aprender dois novos conceitos muito importantes, "Bibliotecas" e "Funções", com estes dois conceitos tornamos nosso algoritmos mais simples e mais estruturados.

---

Vejamos então o nosso primeiro código em C já vimos este algoritmo no capítulo anterior, o "Hello World", abaixo temos o fonte que copiamos do **Pelles C**.

```
/****************************************************************************
 *                                                                          *
 * Filename: hello.c                                                        *
 *                                                                          *
 * Purpose : Standard C sample for Pelles C for Windows.                    *
 *                                                                          *
 * History : Date      Reason                                               *
 *           02-09-10  Created                                              *
 *                                                                          *
 ****************************************************************************/

// Inclusão de bibliotecas e diretivas macro
#include <stdio.h>

// Declaração de variáveis globais e estáticas

// Declaração de funções

// Ponto de entrada de nossa aplicação
int main(void)
{
    printf("Hello, world!\n"); // imprimimos na tela
    return 0; // finalizamos nosso aplicativos adequadamente
}
// Final do código
```

Acima podemos identificar três seções em nosso código:
* Comentários principais, relativos a documentação do projeto e ao arquivo, 
* Diretivas de compilação da Aplicação, como inclusão de outros arquivos ou bibliotecas e 
* Finalmente nosso código, que é dividido em três seções também:
  * Declaração de variáveis
  * Declaração de funções
  * Ponto de entrada (se necessário)

### Comentários do Projeto e Documentação do Arquivo

A primeira seção de nosso código, se trata apenas de comentários onde vemos que existe uma nova forma de se fazer comantários, além do uso apenas de duas barras **//**, podemos no C/C++ e em outras linguagens usar comentários de multiplas linhas com o par **/\*** e **\*/** ou seja na primeira linha iniciamos o comentário multilinha com **/\*** no inicio da linha e na última linha finalizamos no final da linha com **\*/**.

Nessa seção, é fundamental que documentemos nosso código, como já aprendemos com o VisuAlg para a linguagem Portugol. Como podem ver, esta é uma prática muito saudável para o programador e o sucesso do projeto, permitindo que os futuros mantenedores entendam tudo que aconteceu em seu código.

Vejamos em detalhes uma sugestão muito válida para construirmos o comentário que será usado como documentação de nosso projeto:

```
/****************************************************************************
 *                                                                          *
 * Filename: hello.c                                                        *
 *                                                                          *
 * Purpose : Standard C sample for Pelles C for Windows.                    *
 *                                                                          *
 * History : Date      Reason                                               *
 *           02-09-10  Created                                              *
 *                                                                          *
 ****************************************************************************/
```

`Filename:`, por negociação com a equipe fica então determinado que na primeira linha do comentário será o nome do arquivo, podemos também colocar ai o nome do projeto como um todo, se este tiver muitos arquivos.

Na terceira linha podemos ter o proposito, a descrição do projeto ou especificamente do arquivo caso ele faça parte de um projeto maior e não seja o arquivo principal, o ponto de entrada de nosso projeto. Esta linha pode se estender por diversas outras, lembrando-se de indentar sempre o texto para melhorar a formatação do comentário e assim não haver dificuldades de leitura, lembre-se também de evitar ultrapassar o limite de 80 colunas em cada linha.

E para finalizar faça uma seção de histórico (History) em sua documentação, apresentando a data (Date) e o motivo (Reason) da edição de seu arquivo. O que ajudará a encontrar erros e retornar seu código a um estado anterior para testes, e justificar seu trabalho na esquipe. Esto poderá lhe ajudar também quando estiver usando sistema de versionamento como GIT, CVS e outros.

Os asteriscos usados de forma extra no comentário acima, são apenas para melhorar a formatação, você pode usar também outros símbolos dentro de seu comentário de multiplas linhas desde que inicie e finalize o bloco corretamente com os pares: **/\*** e **\*/**.

### Seção de Inclussão e Diretivas de programa.

Na linguagem C e C++ temos diretivas de compilação que ajudam a automatizar alguns processos e orientar o compilador a entender o que deve ser feito para se ter sucesso na montagem de seu projeto, ainda mais quando este tiver multiplos arquivos.

Iremos por hora aprender apenas uma diretiva de compilação, **#include**.

`#include`, diz ao compilador que inclua um outro arquivo ao presente, para que quando este for compilado seja encontrado todas as informações necessárias para sua construção. Esta diretiva é normalmente usada para incluir cabeçalhos de bibliotecas onde as assinaturas das funções fornecidas poruma biblioteca estarão descritas.

No caso de nosso programa, é incluido o arquivo "stdio.h", que é um cabeçalho que define funções básicas para entrada e saida em C, arquivos de cabeçalho são sempre criados com extenção `.h` e contém apenas a descrição das funções (iremos aprender mais um pouco a frente sobre funções, e entenderemos melhor como este arquivo funciona).

A frente veremos que usamos uma função chamada `printf` ela é definida neste aquivo que é o ponto de entrada para a biblioteca de mesmo nome, [**STDIO**](http://www.nongnu.org/avr-libc/user-manual/group__avr__stdio.html) (o link irá lhe levar a uma biblioteca especifica para controladores AVR, como pode ver há diversas versões da STDIO, conforme a plataforma se está trabalhando, o compilador cuida de escolher a biblioteca correta), neste biblioteca há diversas funções que ajudam tanto na escrita de arquivos e também com a sua leitura.

> **Note**: Note
> 
> Tudo no C e C++ é tratado como arquivo, isso é uma herança do Unix, procurem pesquisar como o Unix trata dispositivos e recursos do Sistema Operacional. Portanto se estiver programando para um computador esta biblioteca irá escrever no arquivo "tela" e ler do arquivo "teclado", se estiver em um microcontrolador, conforme a estrutura do mesmo poderá estar lendo e escrevendo no arquivo que dá saida para a porta serial.

### Seção de Código

Como no C/C++ podemos ter arquivos apenas com diretivas ou código de apoio (bibliotecas de funções e parametros) que serão usados para serem incluidos (`#include`) em outros arquivos, e finalmente no arquivo principal para que nosso aplicativo seja construido e se torne funcional, a seção de código abrange tanto a seção de definição de variáveis quando a seção de códigos propriamente.

No C/C++ temos uma função principal de nome `int main(void)`, que é o ponto de entrada da aplicação desenvolvida, e deve ser escrita pelo programador no arquivo que será o ponto de entrada do programa **EXE** ou para o inicio de execução no microcontrolador.

No portugol vimos que precisamos definir uma seção chamada **Inicio** onde conterá o código principal que será chmado para dar partida em nossa aplicação, já no C/C++ precisamos definir uma função de nome `int main(void)` vamos então entender o que é uma função, e então em seguida voltar e vermos como definirmos variáveis globais, locais e a ordem que isso deve ser feito no C/C++.

### Entendendo o conceito de Funções

A função é um dos conceitos mais importantes da programação estruturada, é através da função que estruturamos ainda mais nosso código, pois podemos através delas, agrupar um conjunto de comandos. Uma função no programa atua de forma bem similar a funções matemáticas, passamos um grupo de parametros, um cálculo é feito e se retorna o resultado.

Em C/C++ funções podem retornar ou não valores, vejamos primeiro como é a função principal que devemos definir como ponto de entrada, e o que deve existir  para que tenhamos um programa funcional:

```
int main(void)
```

Temos quatro partes importantes em uma função, acima vemos 3 delas, o que se retorna, o nome da função, e o que ela recebe como parametro para aferir sua execução, no C/C+++ `int` é o tipo de dados inteiro, e é exatamente como em Portugol. portanto a função **main** deve retornar ao seu final um inteiro.

`void` é um tipo de dado que não vale nada, é como ***nulo***, mas em C este conceito `void` pode se tornar bem complexo, e por hora iremos trata-lo como nenhuma informação.

Portanto **main**, não precisa receber parametros, quando for chamada não recebe nada.

O nome da função deve seguir o que já foi ensinado sobre nomeação de variáveis, o mesmo é valido para funções, portanto ela deve iniciar sempre com pelo menos um caracter do tipo *\_* (traço baixo), *a* até *z* ou *A* até *Z* (ou seja todas as letras do alfamento sejam maíusculas ou mínusculas) e em seguida podem conter números, traços baixos e mais letras.

Por exemplo nomes como `int \_andar(int)`, ou `bool AtivarSistema()`, `void UseAlgortimoC45()`, são nomes válidos. 

> **Note** 
> 
> Veja que, ao citarmos uma função escrevemos o nome incluindo o retorno e o que ela recebe de parâmetro, chamamos isso de assinatura da função. E assim evitamos enganos sobre qual função estamos falando.

Como foi dito uma declaração de função tem quatro partes importantes, a quarta parte é o bloco de código que será executado quando a função for chamado, todo bloco de código em C/C++ é delimitado por chaves **{** e **}**, isso define o escopo das variáveis e delimita o bloco, ajudando a administrar nosso código em memória.

Portanto nossa função **main** completa fica assim:

```
int main(void)
{
    printf("Hello, world!\n");
    return 0;
}
```

Veja que o bloco de código fica indentado, dentro das chaves, e que o ideal é que a chaves se abra abaixo do nome da função, e na linha a seguir a última linha da função.

É importante também saber que toda função ao terminar deve chamar a função return, principalmente se retorna algum valor, e o comando return deve ter o que será retornado, no caso de nossa função ele retorna 0, um ineiro.

Sendo **main** uma função chamada como ponto de entrada da aplicação, o valor retornado representa o resultado de nossa aplicação, no caso 0 retorna que tudo correu bem no programa, qualquer outro valor retornado representa um código de erro do programa.

Em se tratando de microcontrolador uma função main nunca deve retornar, uma vez que isso aconteça o microcontrolador ficará parado, podendo alguns em casos especiais reinicializar e voltar a execução de seu firmware ao estado zero.

> Note Para mais informações veja códigos de erros dos aplicativos no DOS ou UNIX/Linux.

### Variáveis Globais e Locais

Antes de usar qualquer variável estas devem ser declaradas, iremos ver por hora apenas as funções de escopo Global e Local. Porém no C há uma complexidade maior nas declarações de escopo, o que não afeta nosso estudo pelo que iremos estudar nesta apostila.

As variáveis de escopo global podem ser vistas em qualquer parte do aplicativo, já as variáveis Locais, apenas dentro do bloco de código onde foram declaradas.

Quando declarar uma variável global, declare antes de todas as funções de  seu aplicativo, e depois das diretivas de compilação.

As variáveis locais devem ser declaradas no inicio do bloco de código no qual pertencem.

### Palavras Reservadas

A linguagem C/C++ tem algumas palavras que são reservadas e não podem ser usadas para nomear funções muito menos variáveis, segue abaixo:

alignas, alignof, and, and_eq, asm, auto, bitand, bitor, bool, break, case, catch, char, char16_t, char32_t, class, compl, const, constexpr, const_cast, continue, decltype, default, delete, do, double, dynamic_cast, else, enum, explicit, export, extern, false, float, for, friend, goto, if, inline, int, long, mutable, namespace, new, noexcept, not, not_eq, nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, return, short, signed, sizeof, static, static_assert, static_cast, struct, switch, template, this, thread_local, throw, true, try, typedef, typeid, typename, union, unsigned, using, virtual, void, volatile, wchar_t, while, xor, xor_eq

Veremos a frente que em C, não temos comandos, apenas as instruções de controle que mais se assemelham a funções, mas são palavras reservadas para instruir a linguagem a uma ação.

Isso abre um grande horizonte para esta linguagem, o que será descoberto em cursos avançados.

### Nome de Variáveis e Funções no C

Da mesma forma que no Portugol temos regraspara criar variáveis e funções, definindo assim nomes legíveis e que expressem sua verdadeira função no código, é preciso ter cuido com o uso de caracteres especias.

Em valem as mesmas regras que em portugol:

* Sempre comecem com uma letra ou ```_```
* Do segundo caracter em diante podem usar números, letras e ```_```
* Não se pode usar letras acentuadas
* Há diferenças entre maísculas e minusculas.
* Nâo se pode usar espaço
* Outros simbolos além de ```_``` não é permitido.

## Próximo passo.

Veremos agora no proximo passo quais são os tipos de dados do C, como devem ser usados e seus limites. É fundamental neste capítulo compreender como os dados são armazenados na memória de seu computador e do processador, caso preciso reveja o capítulo de tipos de dados do Portugol onde isso é esclarecido.

---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
