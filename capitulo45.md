A linguagem C tem alguns tipos de dados extras, além do que vimos no Portugol. Veremos os tipos de dados úteis para quem programa para microcontroladores. Veremos também um pouco sobre Array e como usa-los no C, seu impacto na segurança, e como manipula-los aprendendo assim um pouco sobre ponteiros, mas só o necessário.

## Um pouco mais sobre a manipulação de dados

Como já vimos o computador lida com bits, 8 bits são 1 byte, e 2 bytes um word, 4 bytes um double word e finalmente um quad word são 16 bytes.

Portanto quando armazenamos dados na mémoria o computador estará manipulando tipicamente bytes, seja um byte ou grupos, veremos abaixo que cada tipo de dado na linguagem C tem uma representação típica em bytes, é importantissimo compreendermos como estes dados são armazenados e como são manipulados, veremos para isso os tipos de dados e veremos também os ponteiros para estes típos de dados.

Para entendermos bem como o C manipula os dados na memória e como podemos acelerar este acesso pelo nosso programa, em especial quando lidamos com sequências tipo string, ou até mesmo estruturas de dados é preciso entender a aritmética de ponteiros, porém esta apostila não iremos aprofundar neste assunto por se tratar de um tema avançado.



## Ponteiros
Como já sabemos cada variável ocupa um espaço de momória, este espaço tem o tamanho do tipo de dado utilizado, como vimos no portugol, um tipo inteiro pode ocupar 2 bytes, no C isso pode ser diferente, um tipo como `caracter` é variável no portugol porque guarda sequências que representam texto ou sejam strings de caracteres.

No C, não temos o conceito de string, mas como veremos a frente temos o tipo `char` pode ser um array e assim representar uma string.

Para manipular as variávels de forma mais eficiente, em especial arrays é preciso enteder pelo menos superficialmente o conceito de ponteiro.

Ponteiro é uma referência ao endereço de memória onde está armazenado a variável então referenciada, uma variável do tipo ponteiro pode ser declarada usando o asterisco antes do nome da variável que irá armazenar o endereço, e o tamanho desta variável é compátivel com o espaço de endereçamento de memória. Ou seja se temos um computador que é 16bits teremos um ponteiro de 2 bytes, se for 32bits no ambiente windows comum teremos 4 bytes, e se for 64 bits como nos computadores modernos e windows 64Bits teremos um ponteiro de 8 bytes.

A variável que irá armazenar um ponteiro, deverá ser do mesmo tipo que a variável que será referência do ponteiro, portanto um ponteiro para uma variável do tipo `double` deve ser do mesmo tipo. Abaixo segue uma declaração para um ponteiro do tipo `int`.

```
int *ponteiro;
```

Como vê o simbolo `*` (asterisco) quando antecede uma variável, está informando que ela é um ponteiro para uma posição de memória.

Para se obter a referência para uma variável, devemos usar o simbolo `&` (ampersand) que retorna a posição na memória onde esta variável está sendo armazenada.

Veremos um caso especial que é quando tratamos de arrays, logo a seguir.


---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}

---

Referências: http://www.cplusplus.com/doc/tutorial/variables/
