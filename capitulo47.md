Diferente do portugol e algumas outras linguagens como Cobol e Fortram, o C não tem palavras reservadas para executar certas ações como por exemplo ler teclado ("leia") ou escrever na tela ("escreva" ou "escreval"), mas funções que recebem parametros para que execute tais ações.

LIBC é a biblioteca padrão do C é um conjunto de funções padronizadas que permitem que a linguagem "C" faça operações comuns como entrada e saída e manipulação de cadeiras de caracteres.

Abaixo listo as bibliotecas e o cada uma é especializada, veremos em seguida as principais funções. E iremos destacar quais não se aplicam ao Arduino, e veremos no módulo sobre Arduino as opções adequadas.

| Arquivo | Descrição |
| --- | --- |
| stdio.h	| rotinas padrões de entrada e saída definidas pelos criadores da linguagem C. | 
| alloc.h	| funções para gerenciamento de memória |
| float.h	| funções para tratar números de ponto flutuante |
| math.h	| funções matemáticas |
| stddef.h	| vários tipos de dados e macro substituições |
| stdlib.h	| várias rotinas muito usadas, conversão, sort, etc. |
| string.h	| rotinas p/ manipular strings e memória |
| assert.h	| Macro para diagnóstico. |
| ctype.h	| Funções para teste e conversãode caracteres (ex: isalpha, tolower). |
| errno.h	| Mnemônicas para códigos de erro. |
| limits.h	| Constantes relacionadas com inteiros (númerode bits, gama, etc.) |
| locale.h	| Funções para informações sobrepaises e linguagens. |
| setjmp.h	| Alternativa à chamada normal de funções |
| signal.h	| Tratamento de condições excepcionais. |
| stdarg.h	| Tratamento de funções com número e tipo de argumentos desconhecidos. |
| string.h	| Manipulação de cadeia de caracteres. |
| time.h	| Processamento de horas e data. |

Como já vimos quando dsejamos incluir outro arquivo em nosso código fonte precisamos usar a diretiva ```#include``` portando para se usar uma função que receberá entradas pelo teclado e apresentará dados na tela para o C, precisamos executaro o seguinte comando:

```
#include <stdio.h>
``` 
Vamos aproveitar o momento para conhecer que o ```#include``` possui 2 formas diferentes, esta que nos é apresenada agora, e a que está abaixo:

```
#include "minhalib.h"
```

Como sugere o nome do arquivo, quando a diretiva de pré compilação  envolve o nome do arquivo com as aspas '"' significa que o arquivo deve ser procurado no diretório da aplicação e de bibliotecas do usuário e depois na biblioteca de sistema. Já se viver envolvido com o par '<' e '>' a busca deve se dar apenas nas pastas de bibliotecas de sistemas.

### Padronização

Há uma padronização quanto aos nomes das funções, a maioria será encontrada em práticamente todas as distribuições C, ou melhor compiladores C, cada compilador tem uma biblioteca padrão **libc** que deve seguir a norma ANSI para que não haja a quebra de compatibilidade entre elas.

Não precisamos dizer que há fornecedores de compiladores em especila a MicroSoft que querem impor seu próprio formato, o que não tem dado certo.

A distribuição mais fiel no mercado é a GCC, muito utilizada por sinal.

## Próximo Passo

Vamos agora aprender a ler caracteres do teclado e imprimiri nformações na tela.
