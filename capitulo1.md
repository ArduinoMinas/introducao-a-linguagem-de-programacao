Se você perguntar ao google "define algorito" ele irá lhe responder o que é, e nos adiantamos publicando aqui a resposta que ele nos dá com base no dicionário:

> substantivo masculino
> 1. *mat.* sequência finita de regras, raciocínios ou operações que, aplicada a um número finito de dados, permite solucionar classes semelhantes de problemas.
> 2. *inf.* conjunto das regras e procedimentos lógicos perfeitamente definidos que levam à solução de um problema em um número finito de etapas.

Bem tanto a definição para a matemática (mat.) como para a informática (inf.), ela nos ajuda a enteder perfeitamente o que é um Algoritmo, são sequências de comandos, operações matemáticas que quando ordenadas lógicamente atingem nosso objetivo que é instruir o computador para uma determinada atividade finita, mesmo que infinitamente repetitiva.

Ou seja, mesmo que o computador seja instruido a esperar um comando, sequência finita, ele poderá ser instruido que o faça infinitamente, repetindo esta sequência enquanto ouver energia para seu funcionamento. Diante desta atividade concluida ele irá executar novas atividades que serão decididas em sequência.

Veja com isso percebemos que a melhor forma de programar um Algoritimo não importa a linguagem é través de blocos de sequência de comandos, assim fica inclusive fácil para diagnosticar problemas. Cada linguagem adota uma nomenclatura para estes blocos de código, usaremos aqui a nomeclatura do C/C++, cada bloco de código pode ser identificado e acionado como função, recebendo ou não uma lista de dados que é chamado parâmetros.

## E o que é Linguagem de Programação?

Bem antes de continuarmos temos que entender bem ó que é  uma linguagem de programação.

Linguagem de Programação é um método padronizado de se inscrever instruções para um microcomputador, através da linguagem de programação escolhida, conseguimos informar ao computador o que deve ser feito.

Temos linguagens de baixo nível, que são aquelas linguagens que são escritas em um formato, uma sintaxe bem próxima das operações de manipulação de bytes e bits dos computadores, como por exemplo o **Assembly**, e temos linguagens de programação de alto nível como por exemplo o **Cobol** que usa textos declarativos, e uma estrutura muito bem estabelecida para ser escrita e altamente legível até por um leigo com boa capacidade de interpretação.

Outras linguagens que podemos sitar neste mesmo contextos são:
* Basic
* Fotran
* Pascal
* C#
* Java
* C e C++
* JavaScript
* Python

No nosso curso iremos estudar linguagens de alto nível, mas não tal alto nível assim, inicialmente o Portugol, e posteriormente uma linguagem meio termo entre alto nível e baixo nível, mas ainda assim alto nível, pois será bem legível por um especialista, como você será depois desta dissiplina.

### Linguagens Especializadas
Em cada setor de atuação pode haver linguagens especializadas ao contexto do setor, por exemplo para o Arduino apesar de termos a linguagem C/C++ temos o Wire que é um dialeto do C/C++ na verdade é um framework que nos traz diversas funções, constantes e macros que permite ao programador programar o Arduino de uma forma mais amigável.

Também temos linguagens especializadas em Robôtica, podemos dizer que para cada fabricante de grandes robôs temos uma linguagem, listamos algumas abaixo:

* Unimation&#8482;
* VAL&#174;
* Adept V&#43;&#174;
* AML&#174; da IBM
* Milacron T3

### Compilado vs Interpretado
As linguagens de computador podem ser tanto compiladas ou seja transformadas primeiramente em um código que o computador entenda diretamente, ou podem ser Interpretadas, assim sendo um programa lê o arquivo onde está seu algortimo e interpreta cada linha e cada comando em tempo real, analisano a sintaxe e apontando em tempo de execução os erros encontrados.

Há linguagens que são pré compiladas como o Java e C#, estas linguagens, geram um pseudo-código seja em tempo real, ou num processo separado e em seguida este pseudo-código é interpretado para se obter o resultado desejado com o computador.

As linguagens compiladas tendem ser bem mais rápidas pois geram primeiro um código que é interpretado diretamente pelo microcontrolador, este código ainda pode ser otimizado para se obter um resultado muito mais eficiênte. 

Já as linguagnes interpretadas, mesmo que pré compiladas, dificilmente serão tão rápídas quanto as compiladas, mas semdúvida poderão oferecer recursos dinâmicos muito mais avançados que as compiladas, algumas linguagens compiladas tem desepenho próximo as compiladas quando a compilada não é uma linguagem naturalmente eficiente, como por exemplo linguagem BASIC, pois tem muitos procedimentos de proteção do código para vitar danos inadivertidos causados pelo erro do programador, linguagens como o C e C++ são muito eficientes porque não tem estruturas de proteção, sendo de responsabilidade integral do programador providênciar todas as proteções necessárias, e dando a eles recursos singulares como ponteiros e referências que dão acesso direto a mémoria.

## Mas como posso criar meus próprios Algoritmos?
O que mais nos importa agora é o Algoritmo propriamente, e veremos então como construi-lo, não usaremos até este capítulo nenhuma ferramenta que possa nos ajudar, já que queremos desenvolver mentalmente esta habilidade.

Começemos com exercícios simples, vamos descrever como fazemos para ir a padaria quando sentimos vontade de tomar aquele café que já está cheirando na cozinha.

> Sempre quando sentimos o cheiro do café, é disparado uma sequencia de ações, então paramos tudo que estamos fazendo e vamos a cozinha verificamos se já há pães quentes, se não pegamos a chave da casa, verificamos onde está nossa carteira, nos dirigimos a saída da casa mais próxima, seguimos em direção a padaria mais próxima e que temos o costume de ir, entramos em direção ao balcão de pães, solicitamos alguns pãezinhos, então a atendente nos entrega, e dirigimos ao caixa para efetuar o pagamento, voltamos rapidamente para nossa casa, e proseguimos com nosso café, quando satisfeitos ou ao termino de nosso tempo para o café, voltamos a nossa atividade anterior.

Bem vamos fazer uma pequena análise da descrição acima:

Primeiro um programador mais experiente em microcontroladores vai perceber que se trata de uma ação que é disparada por um evento especial identificada por um de nossos sensores, o nariz, este sensor dispara um algoritmo que nos leva a tomar café.

O algortimo acima não está estruturado, está apenas descrito de forma que qualquer ser humano seja capaz de entende-lo, até mesmo porque é uma ação bem humana tomar café, futuramente iremos ver anções similares mais humanoides, que tal?

Continuando nossa análise, vemos que é preciso descrever com o máximo de detalhes, e onde não há detalhes, mas percebemos sua necessidade, precisamos considerar a chamada de um novo bloco de codigo, ou seja uma função. Por exemplo não descrevemos em detalhes como "verificamos se há pães quentes" isso é uma função que nos retorna mentalmente se há pães ou não, (verdadeiro ou falso), em seguida não havendo pães quentes (seja qual o motivo for), "pegamos a chave da casa", "verificamos nossa carteira" está ai dois coamndos que não precisam estar na mesma ordem, e assim continuamos nossas lista de ações até chegar ao balcão da padaria, consideramos assim que já haja pães prontos e quentes na padaria, ai podemos identificar mais uma função: "solicitamos alguns pãezinhos", esta função pode demorar a retornar, já que não havendo pães teremos que esperar ficar prontos, caso contrário ela retorna imediatamente com a quantidade solicitada, veja ai, já temos um valor passado para esta função como parametro, a quantidade de pães. E então assim continuamos nossas ações até que nos tenhamos satisfeito nosso desejo de tomar café.

Vemos com isso que ao estudarmos algortimo já iniciamos o entendimento de diversos conceitos muito importantes para a programação de microcontroladores, e assim amadurecemos o suficiente para desenvolvermos excelentes códigos em qualquer linguagem.

## Então é só isso?

Por hora sim, agora iremos práticar em sala de aula a construção de algoritmos, não trabalharemos ainda com nenhum método estruturado, apenas práticaremos a construção textual de ações seja quais forem para que nosso celebro passe a pensar nos detalhes necessários para executar tarefas corriqueiras.

Que tal tentar seguimentar sua perna e tentar descrever como você anda, ou seus brasos e assim descrever como faria para deslocar um objeto.

Quer algo mais simples que tal descrever como trocar o pneu de seu carro.

## Algumas dicas para escrever seus primeiros Algoritmos 

* Seja sucinto e procure não entrar em detalhes de ações que não seja especificamente ligadas a atividade;
* Use comentários se preciso detalhar a execução e deixar o algoritmo mais claro;
* Ações auxiliares podem ser descritas por frases curtas, como "verificar se há pães quentes", ou "pegar a chave de boca", estas ações auxiliares serão outros algoritimos que podem ser reutilizados;
* Use os verbos os verbos no infinitivo e iperativo, "pegar", "andar", "corra";
* Procure identificar parametros que auxiliem a tomada de decisão "exist~encia de pães", "Quentes ou não", "Pneu furado";
* Procure identificar com exatidão e em forma quantitativa, "existe ou não existe", ou seja 0 ou maior que zero, "20 unidades";
* Evite muitas informações, e dados a serem guardados.

## O Próximo Capítulo
Iremos agora partir para o estudo da ferramenta VisualAlg, com ela iremos aprender a escrever Algoritmos utiliznado o Portugol, uma forma mais estruturada para descrever nossas atividades, ainda não usaremos o Portugol em detalhes, apenas tereos este capítulo como fonte de referência da interface para nos ajudar a lembrar onde é encontrado cada coisa.


---
Atualizado: 09/07/2016 - 16:20 | Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}

