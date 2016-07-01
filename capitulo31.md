Para começarmos a estudar o Portugol propriamente precisamos entender o que é um código estruturado, e para isso é importante destacar que:

 * Cada comando deve ocupar uma linha;
 * Todas as palavras chaves são implementadas sem acentos e cedilha;
 * Não há diferenciação entre maúsculas e minúsculas, veja a observação abaixo sobre a notação CamelCase;
 * Palavras não reconhecidas serão tratadas como nomes de variáveis;
 * Qualquer texto precedido de // é ignorado, até se atingir o final da linha;

A seguir apresentamos o primeiro exemplode pseudo código em Portugol:

```
algoritmo "MeuPrimeiroPseudoCodigo"
// Função: Demonstrar como se escreve um código estruturado
// Autor: Carlos Delfino <consultoria@carlosdelfino.eti.br>
// Data: 01/07/2016

//Seção de Declarações Variáveis Globais
Var

//Seção de Declaração de Procedimentos e Funções

// Inico do código principal
inicio
// Seção de Comandos

Fimalgoritmo
```

Como podemos ver a cima, o código é separado em seções, tendo na primeira linha o nome do algoritmo que é o mesmo nome usado no arquivo, posto entre aspas.

Em seguida temos alguns comentários que nos ajudam a entender o código, procure sempre descrever seu código, documento o melhor que puder e procure dedicar bom tempo a isso, lembra de quando fizemos a prática de escrever de forma textual nosso algoritmo? faça isso na descrição de seu código, isso irá ajudar a resolver falhas (bugs)

Idenfique claramente o autor, e não deixe de colocar pelo menos o e-mail de contato, e se possível o telefone também, assim em caso de dúvida o proximo programador poderá consultar trejos de códigos inteligiveis.

Feito isso, faça agora a declaração de suas variáveis globais, veremos a frente o que são variáveis globais e locais, por hora declare aqui todas as variáveis que julgar necessário em seu algoritmo.

Dependendo da complexidade de seu código após as variáveis globais, é possível declarar funções e procedimentos, o que não iremos ver ainda.

Finalmente damos inicio ao nosso algortimo, usando a palavra reservada "inicio", este código será executado primeiro, e terminará quando encontrar algum comando que interropa a execução ou ao chegar até a palavra "fimalgoritmo"

Um grande erro cometido pelos programadores inciantes, é a não identação do código formando, assim, blocos de códigos ficam ilegiveis e de dificil correção. No Portugol, a delimitação de bloos se dá sempre pelo uso da palavra chave de inicio do respectivo ao tipo de bloco de controle e finalizado pela palavra chave de finalização, veremos em detalhes em momento oportuno.

### O que é Indentação?
Identação é o ato de organizar cara linha em níveis, inserindo espaços no inicio da linha para que a linha que é subordinada, ou seja, pertence ao bloco esteja mais a dentro na estrutura.

No Portugol usaremos três espaços, as linguagens não obrigam uma quantidade especifica de espaço, sendo sempre acordado entre os programadores antes de inciar o projeto, porém já se tornou uma conveção de boa prática o uso de três espaço, em alguns casos quadro (4) espaços.

veja o exemplo abaixo:

'''
inicio
   escrever("entre seu nome"
   leia(nome)
   se nome == "" entao
      escreva("é preciso um nome para identifica-lo")
      interrompa
   fimse
fimalgoritmo
'''


Como podem ver o código estruturado é indentado, e de fácil leitura, e rápidamente identificamos o inicio e fim de cada bloco de códigos, independente do seu objetivo.


