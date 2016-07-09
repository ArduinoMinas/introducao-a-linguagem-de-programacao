Iremos neste capítulo entender como se deve estruturar um código em C, e o que é cada parte. Iremos aprender dois novos conceitos muito importantes, "Bibliotecas" e "Funções", com estes dois conceitos tornamos nosso algortimos bem mais simples.

Vejamos então o nosso primeiro código em C que já vimos no capítulo anterior, o "Hello World", abaixo temos o fonte que copiamos da interface do **Pelles C**.

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

#include <stdio.h>

/* entry point */
int main(void)
{
    printf("Hello, world!\n");
    return 0;
}
```

Acima podemos identificar três seções em nosso código, Comentários principais e relativos a documentação do projeto e arquivo, Diretivas da Aplicação, como inclusão de outros arquivos e finalmente nosso código.

### Comentários do Projeto e Documentação do Arquivo

A primeira seção de nosso código, se trata apenas de comentários onde vemos que existe umanova forma de se fazer comantários além do uso apenas de duas barras **//**, podemos no C/C++ e em outras linguagens usar comentários de multiplas linhas com o par **/\*** e **\*/** ou seja na primeira linha iniciamos o comentário multilinha com **/\*** no inicio da linha e na última linha finalizamos no final da linha com **\*/**.

Na primeira seção é fundamental, que documentemos nosso código como já aprendemos com o VisuAlg para a linguagem Portugol, como podem ver esta é uma prática muito saudável para o programador e o sucesso do projeto, permitindo que os futuros mantenedores entendam tudo que aconteceu em seu código.

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

`Filename:` por negociação com a equipe fica então determinado que na primeira linha do comentário será o nome do arquivo, podemos também colocar ai o nome do projeto como um todo, se este tiver muitos arquivos.

Na terceira linha podemos ter o proposito, a descrição, do projeto ou especificamente do arquivo caso ele faça parte de um projeto maior e não seja o arquivo principal, o ponto de entrada de nosso projeto. Esta linha pode se estender por diversas linhas, lembrando-se de indentar sempre o texto para melhorar a formatação do comentário e assim não haver dificuldades de leitura, lembre-se também de evitar ultrapassar o limite de 80 colunas em cada linha.

E para finalizar faça uma seção de histórico (History) em sua documentação, apresentando a data (Date) e o motivo (Reason) da edição de seu arquivo. O que ajudará a encontrar erros e retornar seu código a um estado anterior para testes, e justificar seu trabalho na esquipe.

Os asteriscos usados de forma extra no comentário acima, são apenas para melhorar a formatação, você pode usar também outros simbolos dentro de seu comentário de multiplas linhas desde que inicie e finalize o bloco corretamente com os pares: **/\*** e **\*/**.

### Seção de Inclussão e diretivas de programa.

Na linguagem C e C++ temos diretivas de compilação que ajudam a automatizar alguns processos e orientar o compilador a entender o que deve ser feito para se ter sucesso na montagem de seu projeto, ainda mais quando este tiver multiplos arquivos.

Iremos por hora aprender apenas uma diretiva de compilação, **#include**.

`#include`, diz ao compilador que inclua um outro arquivo ao presente, para que quando este for compilado seja encontrado todas as informações necessárias para sua construção.

No caso de nosso programa, é incluido o arquivo "stdio.h", que é um cabeçalho que define funções básicas para entrada e saida em C, arquivos de cabeçalho são sempre criados com extenção `.h` e contem apenas a descrição das funções (iremos aprender mais um pouco a frente sobre funções, e entenderemos melhor como este arquivo funciona).

A frente veremos que usamos uma função chamada `printf` ela é definida neste aquivo que é o ponto de entrada para a biblioteca de mesmo nome, **STDIO**, neste biblioteca há diversas funções que ajudam tanto na escrita de arquivos e tela como sua leitura.

> **Note**: Note
> 
> Tudo no C e C++ é tratado como arquivo, isso é uma erança do Unix, procurem pesquisar como o Unix trata dispositivos e recursos do Sistema Operacional.

### Seção de Código

Como no C/C++ podemos ter arquivos apenas com código de apoio (bibliotecas de funções e parametros) que serão usados para serem incluidos (`#include`) em outros arquivos, e finalmente no arquivo principal para que nosso aplicativo seja construido e se torne funcional, a seção de código abrange tanto a seção de definição de variáveis quando a seçaão de códigos propriamente.

No C/C++ temos uma função principal que deve ser escrita e será o nosso ponto de entrada para o programa,veremos a seguir o que é uma função, mas por hora iremos entender como é este ponto de entrada no código escrito em C/C++.

No portugol vimos que precisamos definir uma seção chamada **Inicio** onde conterá o código principal que será chmado para dar partida em nossa aplicação, já no C/C++ precisamos definir uma função de nome `main`vamos então entender o que é uma função, e então em seguida voltar e vermos como definirmos variáveis globais, locais e a ordem que isso deve ser feito no C/C++.

### Entendo o conceito de Funções

A função é um dos conceitos mais importantes da programação, é através da função que estruturamos ainda mais nosso código, pois podemos através delas, agrupar um conjunto de comandos, uma função em programa funciona de forma bem similar a funções matemáticas, passamos um grupo de parametros, um calculo é feito e se retorna o resultado.

Em C/C++ funções podem retornar ou não valores, vejamos como é a função principal que devemos definir seu conteúdo para que tenhamos um programa funcional:

```
int main(void)
```

Temos quatro partes importantes em uma função, acima vemos 3 delas, o que se retorna, o nome da função, e o que ela recebe como parametro para aferir sua execução, no C/C+++ `int` é o tipo de dados inteiro, e é exatamente como em Portugol. portanto a função **main** deve retornar ao seu final um inteiro.

`void` é um tipo de dado que não vale nada, é como ***nulo***, mas em C este conceito `void` pode se tornar bem complexo, e por hora iremos trata-lo como nenhuma informação.

Portanto **main**, não precisa receber parametros, quando for chamada não recebe nada.

O nome da função deve seguir o que já foi ensinado sobre nomeação de variáveis, o mesmo é valido para funções, portanto ela deve iniciar sempre com pelo menos um caracter do tipo *\_* (traço baixo), *a* até *z* ou *A* até *Z* (ou seja todas as letras do alfamento sejam maíusculas ou mínusculas) e em seguida podem conter números, traços baixos e mais letras.

Por exemplo nomes como `int \_andar(int)`, ou `bool AtivarSistema()`, `void UseAlgortimoC45()`, são nomes válidos. 

> **Note**:Note
> Veja que ao citarmos uma função escrevemos o nome incluindo o retorno e o que ela recebe de parametro, chamos isso de assinatura da função.

