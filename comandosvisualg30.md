
Este material foi retirado na integra do arquivo "RELAÇÃO DE COMANDOS DO VISUALG 3.0.txt", e no decorrer do desenvolvimento desta apostila será amadurecido para melhorar a fluência e consolidação com o restante do texto.

Dentro do VISUALG 3.0 tem uma CTRL+J mas acho que também está incompleta, é que são tantas coisas, que eu estou ainda me organizando.

A maioria deles estão dentro do HELP.CHM 

A relação dos comandos, funções, variáveis, constantes e dados  :

####Funções pré definidas no visualg 3.0 (pseudo-linguagem em portugol) 

#####Abs( ) 

#####Log( )

#####Div( )

#####Tan( )

#####Sen( )

#####Cos( )

#####Rand( )

#####Randi( )

#####Quad( )

#####Exp( )

#####Pot( )

#####Cotan( )

#####ArcCos( )

#####ArcSen( )

#####Raizq( )

#####Mod 
usado para achar o módulo de um número em comparações (o mesmo que ' % ' )  

#### teclado

##### Leia( variável_nome ) 
Lê do teclado e coloca em uma variável 'variável_nome'
 

####Funções especiais de conversões

#####Pos( )

#####Asc( )

#####Carac( )

#####Copia ( )

#####Int( )

#####Compr( )

#####Maiusc( )

#####Minusc( )

#####NumPCarac( )

#####CaracPNum( )


#### Funções especiais que não retornam valores pra variáveis só com os PERIFÉRICO (MONITOR)

#####Escreva   
Escreve na tela do monitor do computador fica na linha

```escreva("texto entre aspas, ou variável que terá o conteudo impresso na tela")```

```escreva(variavel)```


#####Escreval
Escreve na tela do monitor do computador mas pulando um linha.

```
escreval("texto entre aspas, ou variável que terá o conteudo impresso na tela com um salto de linha")
```

```
escreval(variavel)
```


##### MudaCor
Muda a cor dos caracteres(letras) e do fundo (tela) 

```
mudacor("nome da cor")
```

Nome de cores possíveis:
* Amarelo
* Branco
* Preto
* Azul
* Verde
* Vermelho



#####Mudacor(Cor, posição) 
Muda a cor dos caracteres (letras) ou do fundo (tela) conforme a posição informada

```
mudacor("nome da cor","posição")
```

Nome de cores possíveis:
* Amarelo
* Branco
* Preto
* Azul
* Verde
* Vermelho

Posição pode ser entre "aspas" ou:
* FRENTE
* FUNDOS

Posição=> Entre "aspas" também: FRENTE, FUNDOS   

#### Extras (ainda não criadas)

##### Posicionar

##### Tecla

##### Etrim

##### Dtrim

##### Esquerda

##### Direita

##### Replicar


#### Comandos do Visualg 3.0 (pseudo-linguagem em portugol) 

##### Limpatela
Limpa a tela do monitor do computador

##### Pausa

##### Arquivo

#### Desvios multiplos condicionais 
só use variáveis e controles do tipo caracter

```
Escolha  xvar(caracter)
Caso "texto"
   Outrocaso 
Fimescolha (FIMESCOLHA)
```

#### Desvios simples e compostos

```
Se (condição) então 
     comandos
senão 
     comandos
FimSe
```

```
SE Entao Então (ENTÃO) 
Senao, Senão (SENÃO)
FimSe
```

####C ontrole de Laços sequenciais e finitos 

```
PARA variável(inteira) DE inicio ATÉ fim FAÇA
     comandos
FIMPARA
```

``` 
Para De (DE) Ate (ATE) Até (ATÉ) Passo Faca (FACA) Faça (FAÇA)
FimPara (FIMPARA)
```

#### Controle de Laços sequenciais e infinitos 
Controla quando um bloco de código deve ser executado.

##### Enquanto 
"Enquanto" uma determinada condição for verdadeira executa o bloco de código.

```
Enquanto condição FAÇA
        comandos
FimEnquanto
```
##### Repita
Repete o bloco de código infinitamente;

```
Repita
Fimrepita (FIMREPITA)
```

##### Interrompa
Quando usado dentro de um bloco de código dentro de laço (loop)

```Interrompa```

##### Retorne
Retorna ao inicio do laço, começando novamente o bloco.

``` Retorne ```

##### Pausa
Interrompe a execução do bloco;

``` Pausa ```

#### Operadores lógicos

##### e
Conjunção logica, verdadeiro apenas se ambos as condições forem verdadeiras.

``` e (E) ```

##### ou
Conjunção logica, verdadeiro  se uma das condições forem verdadeiras.

``` ou (OU) ```


##### não
Inversor lógico, inverte a condição, se verdadeira passa a ser falsa e vice versa.

``` Não (NÃO) ```

##### Xou
Conjunção lógica, equivalente a ``` ou ``` porém apenas retorna verdadeiro se uma das condições forem verdaeiras, se ambas forem verdadeiras ou falsas retorna falso.
``` Xou (XOU) ```


#### Declaração de UDFs (FUNÇÕES DEFINIDAS PELOS USUÁRIOS)


##### Funcao
```
Função (FUNÇÃO) 
Fimfuncao (FIMFUNÇÃO)
```

##### Mensagem 
```
Procedimento (PROCEDIMENTO)
Fimprocedimento (FIMPROCEDIMENTO)
```

#### Palavras reservadas Especiais

##### Algoritmo
Começo de todos os algoritmos 

##### var
declaração dos tipos das variáveis   

##### Inicio
inicio do programa(Algoritmo) ou função ou procedimento

##### FimAlgoritmo
termino do algoritmo e fim do programa

#### Cronometro

```Timer```


```On```


```Off```


```Eco (ECO)```


```Aleatorio (ALEATÓRIO)```


```Perfil```


```Dos (DOS)```


```Debug (DEBUG)```


```Tipo (TIPO)```


```var (VAR)```


```const (CONST)```

 
#### Declaração de constantes padrão
const (CONST)
Lista
Pi (PI)
 
#### Declaradores de Variáveis no cabeçalho do programa (área de declarações)
Var (VAR) 
Variável  (VARIÁVEL)
Variavel  (VARIAVEL)

É eu sei, estou montando ainda, mas me falta tempo!
Dentro do VISUALG 3.0 tem uma CTRL+J mas acho que também está incompleta, é que são tantas coisas, que eu estou ainda me organizando.
A maioria deles estão dentro do HELP.CHM 


A relação dos comandos, funções, variáveis, constantes e dados  :

Funções pré definidas no visualg 3.0 (pseudo-linguagem em portugol) 
Abs( ) 
Log
Div
Tan(
Sen
Cos
Rand
Randi
Quad
Exp
Pot
Cotan
ArcCos
ArcSen
Raizq

Mod ==> usado para achar o módulo de um número em comparações (o mesmo que ' % ' )  
------------------------------------------- teclado ------------------------------------------------------
Leia( variável_nome ) ==> Lê do teclado e coloca em uma variável 'variável_nome'
--------------------------------------------------------------------------------------------------------------
Funções especiais de conversões
Pos
Asc( )
Carac( )
Copia ( )
Int
Compr ( 
Maiusc
Minusc
NumPCarac
CaracPNum

Funções especiais que não retornam valores pra variáveis só com os PERIFÉRICO (MONITOR)
Escreva( )   ==> Escreve na tela do monitor do computador
Escreval( )  ==> Escreve na tela do monitor do computador mas pulando um linha.
MudaCor( ) Mudacor(Cor, posição) Cores =>   Entre "aspas": Amarelo, Branco, Preto, Azul, Verde, Vermelho
                                                   Posição=> Entre "aspas" também: FRENTE, FUNDOS   


Extras (ainda não criadas)
*Posicionar
*Tecla
*Etrim
*Dtrim
*Esquerda
*Direita
*Replicar

Comandos do Visualg 3.0 (pseudo-linguagem em portugol) 
Limpatela  ==> Limpa a tela do monitor do computador
Pausa
Arquivo

Escolha de 
Caso

Outrocaso
Fimescolha (FIMESCOLHA)

Se Entao Então (ENTÃO) 
Senao, Senão (SENÃO)
FimSe

Para De (DE) Ate (ATE) Até (ATÉ) Passo Faca (FACA) Faça (FAÇA)
FimPara (FIMPARA)


Enquanto
FimEnquanto (FIMENQUANTO)

Repita
Fimrepita (FIMREPITA)

Interrompa
Retorne

Pausa

Operadores lógicos
e (E)
ou (OU)
Nao
Não (NÃO)
Xou (XOU)

Declaração de UDFs (FUNÇÕES DEFINIDAS PELOS USUÁRIOS)
Funcao
Função (FUNÇÃO) 
Fimfuncao (FIMFUNÇÃO)
Mensagem 
Procedimento (PROCEDIMENTO)
Fimprocedimento (FIMPROCEDIMENTO)


### Palavras reservadas Especiais

Algoritmo     --> Começo de todos os algoritmos 
var              --> declaração dos tipos das variáveis   
Inicio           --> inicio do programa(Algoritmo) ou função ou procedimento
FimAlgoritmo --> termino do algoritmo e fim do programa
=========================================
Cronometro
Timer
On
Off
Eco (ECO)
Aleatorio (ALEATÓRIO)
Perfil 
Dos (DOS)
Debug (DEBUG)
Tipo (TIPO)
var (VAR)
const (CONST)

======================================
Declaração de constantes padrão
const (CONST)
Lista
Pi (PI)

================================================
Declaradores de Variáveis no cabeçalho do programa (área de declarações)
Var (VAR) 
Variável  (VARIÁVEL)
Variavel  (VARIAVEL)


