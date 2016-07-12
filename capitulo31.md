Para começarmos a estudar o **Portugol**, propriamente, precisamos entender o que é um código estruturado, e para isso é importante destacar que para se ter um bom código estruturado é preciso **seguir algumas regras**:
 * Cada comando deve ocupar uma linha;
 * Todas as palavras chaves são implementadas sem acentos e cedilha;
 * Não há diferenciação entre maúsculas e minúsculas, veja a observação abaixo sobre a notação CamelCase;
 * Palavras não reconhecidas serão tratadas como nomes de variáveis;
 * Qualquer texto precedido de // é ignorado, até se atingir o final da linha;

A seguir apresentamos o primeiro exemplo de pseudo código em Portugol:

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

Como podemos ver, o código é separado em seções, tendo na primeira linha o nome do "'algoritmo'" que é o mesmo nome usado no arquivo, posto entre aspas.

Em seguida temos alguns comentários que nos ajudam a entender o código, procure sempre descrever seu código com uma boa documentação, o melhor que puder e procure dedicar bom tempo a isso, você se lembra de quando fizemos a prática de escrever de forma textual nosso algoritmo? faça isso na descrição de seu código, isso irá ajudar a resolver falhas (bugs).

Idenfique claramente o autor e não deixe de colocar pelo menos o e-mail de contato, se possível o telefone também, assim em caso de dúvida o proximo programador poderá consultar trechos de códigos de difícil entendimento, e se basear na documentação para optimiza-lo.

Feito isso, faça a seguir a declaração de suas variáveis globais, veremos a frente o que são variáveis globais e locais, por hora declare após a documentação inicial todas as variáveis que julgar necessário em seu algoritmo, a seção de declaração das variáveis é precido pela diretiva "'Var'". Esta seção termina quando a próxima seção de código iniciar, existindo uma diretiva para finaliza-la.

Dependendo da complexidade de seu código após as variáveis globais, é possível declarar funções e procedimentos, o que não iremos ver ainda. Somente veremos estes conceitos, após dominarmos os conceitos básicos de controle e viáveis e em especial **Funções**.

Finalmente damos inicio ao nosso algoritmo, usando a palavra reservada "'inicio'", este código será executado primeiro, e terminará quando encontrar algum comando que interropa a execução ou ao chegar até a palavra "'fimalgoritmo'"

Um grande erro cometido pelos programadores inciantes, é a não identação do código, assim, blocos de códigos ficam ilegíveis e de difícil correção. No Portugol, a delimitação de bloos se dá sempre pelo uso da palavra chave respectiva ao tipo de bloco de controle e finalizado pela palavra chave de finalização, veremos em detalhes mais a frente quando formos tratar cada bloco de código.

### O que é Indentação?


Identação é o ato de organizar cada linha em níveis, inserindo espaços no inicio da linha para que esta linha fique subordina a anterior, ou seja, pertence ao bloco que esteja mais a dentro na estrutura.

No **Portugol** usaremos ***três espaços***, as linguagens não obrigam uma quantidade especifica de espaço, sendo a quantidade, sempre acordado entre os programadores antes de inciar o projeto, porém já se tornou uma convenção de boa prática o uso de três (3) espaço, em alguns casos quadro (4) espaços, podendo neste caso ser substituido por uma tabulação para cada intentação.

veja o exemplo abaixo:

'''
inicio
   escrever("entre seu nome"
   leia(nome)
   se nome == "" entao
      escreva("é preciso um nome para identifica-lo")
      interrompa
   fimse
   escreval("Obrigado por informar seu nome: ",nome)
fimalgoritmo
'''

Como podem ver o código estruturado é indentado, e de fácil leitura, e rápidamente identificamos o inicio e fim de cada bloco de códigos, independente do seu objetivo.

## Próximo passo 

Veremos a seguir como dar nomes as variáveis e funções no Portugol, porém usaremos a prática de CamelCase, que não é obrigatória no Portugol, muito menos no VisuAlg, mas é uma boa prática importante para o amadurecimento como desenvolvedor.

---
Atualizado: 09/07/2016 - 16:25 | Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
