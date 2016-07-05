Se você perguntar ao google "define algorito" ele irá lhe responder o que é, e nos adiantamos publicando aqui a resposta que ele nos dá com base no dicionário:

> substantivo masculino
> 1. *mat.* sequência finita de regras, raciocínios ou operações que, aplicada a um número finito de dados, permite solucionar classes semelhantes de problemas.
> 2. *inf.* conjunto das regras e procedimentos lógicos perfeitamente definidos que levam à solução de um problema em um número finito de etapas.

Bem tanto a definição para a matemática (mat.) como para a informática (inf.), ela nos ajuda a enteder perfeitamente o que é um Algoritmo, são sequências de comandos, operações matemáticas que quando ordenadas lógicamente atingem nosso objetivo que é instruir o computador para uma determinada atividade finita, mesmo que infinitamente repetitiva.

Ou seja, mesmo que o computador seja instruido a esperar um comando, sequência finita, ele poderá ser instruido que o faça infinitamente, repetindo esta sequência enquanto ouver energia para seu funcionamento. Diante desta atividade concluida ele irá executar novas atividades que serão decididas em sequência.

Veja com isso percebemos que a melhor forma de programar um Algoritimo não importa a linguagem é través de blocos de sequência de comandos, assim fica inclusive fácil para diagnosticar problemas. Cada linguagem adota uma nomenclatura para estes blocos de código, usaremos aqui a nomeclatura do C/C++, cada bloco de código pode ser identificado e acionado como função, recebendo ou não uma lista de dados que é chamado parâmetros.

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
* Ações auxiliares podem ser descritas por frases curtas, como "verificar se há pães quentes", ou "pegar a chave de boca", estas ações auxiliares serão outros algoritimos que podem ser reutilizados;
* Use os verbos os verbos no infinitivo e iperativo, "pegar", "andar", "corra";
* Procure identificar parametros que auxiliem a tomada de decisão "exist~encia de pães", "Quentes ou não", "Pneu furado";
* Procure identificar com exatidão e em forma quantitativa, "existe ou não existe", ou seja 0 ou maior que zero, "20 unidades";
* Evite muitas informações, e dados a serem guardados.

## O Próximo Capítulo
Iremos agora partir para o estudo da ferramenta VisualAlg, com ela iremos aprender a escrever Algoritmos utiliznado o Portugol, uma forma mais estruturada para descrever nossas atividades, ainda não usaremos o Portugol em detalhes, apenas tereos este capítulo como fonte de referência da interface para nos ajudar a lembrar onde é encontrado cada coisa.




