A linguagem C tem alguns tipos de dados extras, além do que vimos no Portugol. Veremos os tipos de dados úteis para quem programa para microcontroladores. Veremos também um pouco sobre Array e como usa-los no C, seu impacto na segurança, e como manipula-los aprendendo assim um pouco sobre ponteiros, mas só o necessário.


## Tipos Númericos

A definição para tipos númericos é bem vasta na linguagem em C, veremos alguns tipos muito importantes mas não veremos em detalhes seus limites, já que variam de plataforma para plataforma.

> **Note** 
> Cada tipo de dado númerico tem seus limites tanto para números possitivos como para valores negativos, no arquivo ``stdint.h`` é possível ter acesso a constantes que nos ajudam a lidar com estes limites, no link http://www.nongnu.org/avr-libc/user-manual/group__avr__stdint.html é possível tomar conhecimento dos limites conforme a plataforma AVR. A mesma usada no Arduino UNO.

### Inteiros

Para lidar com inteiros trabalharemos apenas com um tipo, o tipo `int` que nos permite trabalhar típicamente com números de tamanho equivalentes a 16 bits, sejam positivos ou negativos, com ou sem sinal.

### Frações e ponto flutuante.

Os números fracionados e números usados em engenhária como os de ponto flutuantes, são representados especialmente no C/C++ e temos 3 tipos, porém somente veremos dois deles `float` e `double`, estes tipos são como os tipos `real` portugol.

### Valores Lógicos

Para valores lógicos como verdadeiro e falso, temos o tipo `bool` que pode ser usado para identificar variáveis que irão guardar resultados de expressões lógicas e relacionais.

## Ponteiros
Como já sabemos cada variável ocupa um espaço de momória, este espaço tem o tamanho do tipo de dado utilizado, como vimos no portugol, um tipo inteiro pode ocupar 2 bytes, no C isso pode ser diferente, um tipo como `caracter` é variável no portugol porque guarda sequências que representam texto ou sejam strings de caracteres.

No C, não temos o conceito de string, mas como veremos a frente temos o tipo `char` que pode ser um array e assim representar uma string.

Para manipular as variávels de forma mais eficiente, em especial arreis é preciso enteder pelo menos superficlamente o conceito de ponteiro.

Ponteiro é um tipo de variável que armazena o endereço de mémoria onde está armazenado a variável então referenciada, o tamanho desta variável é compátivel com o espaço de endereçamento de memória. Ou seja se temos um computador que é 16bits teremos um ponteiro de 2 bytes, se for 32bits no ambiente windows comum teremos 4 bytes, e se for 64 bits como nos computadores modernos e windows 64Bits teremos um ponteiro de 8 bytes.

A variável que irá armazenar um ponteiro, deverá ser do mesmo tipo que a variável que será referência do ponteiro, portanto um ponteiro para uma variável do tipo `double` deve ser do mesmo tipo. Abaixo segue uma declaração para um ponteiro do tipo `int`.

```
int *ponteiro;
```

Como vê o simbolo `*` (asterisco) quando antecede uma variável, está informando que ela é um ponteiro para uma posição de memória.

Para se obter a referência para uma variável, devemos usar o simbolo `&` (apersante) que retorna quando usado com a variável que se deseja obtero endereõ, sua posição na memória.

Veremos um caso especial que é quando tratamos de arrays, logo a seguir.



## Tipos para Caracter e Strings

Em C não existe strings, porém no C++ temos um tipo especial de nome `string`, não o veremos aqui, mas veremos como trabalhar com strings no C puro.

Para lidar com caracteres em C, temos o tipo `char`, este tipo permite armazenar representações números dos caracteres da tabela ASCII. Ou seja valores de 0 a 255, existem outros representações de caracteres muito úteis, porém não entraremos neste tipo neste curso.

Então como lidar com strings de texto na linguagem C pura? para isso usamos um vetor terminado com o valor nulo, tal valor é presentado por \0 que na tabela ASCII é representado por `null`, assim toda string automáticamente recebe o código \0 em seu final.

Assim no código abaixo:

```
char umaString[] = "Um texto qualquer]
```

Temos um vetor de 18 posições do tipo char, sendo a ultima posição preenchida com \0.

Se declararmos um vector assim:

```
char umaStringGrande[400];
```

Este será capaz de armazenar uma string com até 399 caracteres, já que o último espaço do vetor deverá conter um \0 (null) para indicar o fim da string.

Veremos em momento oportuno como manipular este tipo de vetor que armazena strings, no C e C++ há cuidados muito importantes para se manipular strings, que se não forem observados, causaram mau funcionamento e até perda de dados importantes.

---
Referências: http://www.cplusplus.com/doc/tutorial/variables/

---
Atualizado: 10/07/2016 - 12:42 | Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
