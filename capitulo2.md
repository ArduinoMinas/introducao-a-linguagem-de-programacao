# Capítulo 2 - VisuAlg e sua IDE
O VisuAlg não é uma linguagem de programação, mas uma ferramenta que auxilia no aprendizado da linguagem Portugol, VisuAlg tem algumas peculiaridades, que torna seu Portugol, mas adequado ao uso com sua Interface, o que chamaremos deste ponto em diante de IDE (Integrated Development Environment) em português Ambiente de Desenvolvimento Integrado, um software que possui todas ferramentas ou viabiliza a interação com outras ferramentas de desenvolvimento de forma totalmente integrada e transparente.

Com o uso de uma IDE não precisamos nos preocupar com o editor usado para escrever nosso código, não precisamos nos preocupar com a ferramenta usada para nos ajudar a encontrar erros de escritas, muito menos com a ferramenta usada para converter nosso código em um formato mais próximo para o entendimento do computador, e muito menos com a fase final de ligação do nosso código com as instruções e posições de computador que se destina o código.

A IDE é responsável por ter todas as ferramentas que precisamos, totalmente integradas e totalmente de forma transparente.

Abaixo apresentamos a tela inicial do VisuAlg:

![Interface principal do VisualG](/telas/visualg/tela visualg - 3 - 2016-07-01 13.26.28.png)

Como pode ser visto a janela é dividida em 3 seções muito importantes:
* Área de programa
* Áreas das Váriáveis de Mémoria
* Área de Visualização de Resultados

Além destas 3 seções, temos também o "Menu", "Barra de Ferramentas" e a "Barra de estatus", o "Menu" no topo da tela, logo abaixo "Barra de Ferramentas" e na base ou roda-pé da janela principal temos a "Barra de Estatus".

Teremos também uma janela secundária que sempre se abre quando executamos nosso algoritmo para que haja interação do usuário com o programa quando executado, chamaremos de "Console".

A seguir veremos o menu e as barras, cada seção e por último a conole como usa-los para termos o melhor resultado.

## Menu
Como todo software para sistemas operacionais baseados em janela como Windows, MAC ou Linux Gráfico com base em XWindows ou X86, é comum ter um menu que nos dá acesso a ações, agrupados conforme funcionalidades

Abaixo vemos nosso menu do VisuAlg Versão 3.0:
![Menu do VisuAlg V3.0](telas/visualg/tela visualg - 3 - Menu e Barra de Ferramentas.png)

Os dois primeiros menus não há muita novidade, apenas o comum em qualquer editor de texto, no Menu "Arquivo" iremos encontrar ações referentes a abrir, salvar e fechar arquivo, além de fechar o IDE, no menu "Editar" ações relacionadas a edção como copiar, colar, recortar, pesquisar no código por strings de texto.

>**String** de texto, é uma sequência de letras, caracteres, quando formos estudar estar tipos de dados, entenderemos melhor este conceito.

Já o menu "Run (Executar)" é novidade para muitos, com ele iremos testar nosso algoritmo solicitando ao VisuAlg que prepare nosso algoritmo para execução, verificando erros e executando sequêncialmente, ou se desejarmos passo a passo com nosso total controle.

Veremos em detalhes o uso de cada opção do menu durante as praticas de aula, em especial "Executar Algoritmo" e "Executar Passo a Passo".

Não deixe de estudar este menu, e práticar o uso das teclas de atalho, a que mais usaremos é [CTRL]+[S] para salvar e [F9] para executar nosso código.

> O que estas letras entre "colchetes"? usamos esta representação para indicar teclas a serem usadas como atalhos, no caso de [CTRL]+[S] representa o uso em sequencia combinada das teclas "Control" e a tecla "s" ou seja devem ser precionadas em conjunto, sempre na sequência sugerida, assim se aperta a tecla "Control", mantem, e em conjunto aperta a tecla "s", soltando logo em seguida, observe que mesmoestando representada em maiúscula não usaremos a tecla "Shift" muito menos a tecla "Caps Lock" para deixar em maiúscula.

## Menu Run (Executar)
Vamos dar uma atenção especial ao menu **Run (Executar**, sem dúvida ele é o menu mais utilizado em uma IDE, com ele testamos nosso código e corrigimos os erros que possam existir.

![Menu Run (Executar)](Captura de tela 2016-07-01 16.21.57.png)

#Barra de Ferramentas
Nossa barra de ferramentas é um atalho as ações disponíveis no menu, ali se encontra as ações da IDE mais utilizada e estão representadas por icones para facilitar seu uso, veja na imagem abaixo ela está logo abaixo do menu:

![Menu do VisuAlg V3.0](telas/visualg/tela visualg - 3 - Menu e Barra de Ferramentas.png)
Bem não precisamos entrar em detalhes, sobre o uso da barra, durante nossas práticas em aula iremos entede-la.

#Barra de Estatus
A barra de estatus, ou se preferir barra de status, apresenta informações relevantes ao programador durante a codificação.

![Barra de Status](telas/visualg/tela visualg - 3 - Barra de Status.png)

Na barra do VisuAlg temos uma pequena seção que nos mostra a a linha e coluna onde se encontra o curso, informação muito útil para encontrarmos o curso e também formatarmos nosso código. 

Na proxima seção da barra de estatus, vemos o estado do documento, se vazio ele está salvo, se modificado tem a indicação "Modificado", se em pesquisa a indicação "Pesquisando", com o uso da ferramenta irá identificar novos "Status" para seu domento.

Na proxima seção vem um texto que instrui como melhor usar as teclas na seção ativa, e finalmetne a ultima seção que apresenta mensagens relevantes sobre os processos solicitados, por exemplo coloque o mouse sobre cada seção da janela, e veja a mesangem apresentada. Você verá que ele lhe apresenta a seção e como elapode ser útil para você.

## Seção Visualização de Resultados
A Seção de visualização de resultados apresenta mensagens relativas a execução do programa, mantendo um histórico da execução, principalmente inicio e fim, é preciso cuidado pois espera-se que a interação seja pelo console, masno Visuag a intarção ocorre um pouco diferente, sendo do nesta etela apresentada as mensagens do programa, e em janelas especificas as solicitações de dados ao usuário, a console será vista mais a frente..

![](telas/visualg/tela visualg - 3 - Seção Visualização de Resultados.png)

A seguir veja a seção "Área de visualização dos resultados", apos executarmos um simples algortimo conceitual que sugere o funcionamento de um sistema de caixa.
![Área de visualização dos resultados do algoritmo caixa](telas/visualg/tela visualg - 3 - Seção Visualização de Resultados - algoritmo caixa.png)


## Seção das Variáveis de Memória
Nesta seção é possível ver o conteúdo de cada variável de mémoria Global ou Local (entederemos isso mais a frente).
Veja abaixo como esta seção fica ao usarmos o Algoritmo "Caixa".

![Seção de visualização das Variáveis de Memória](telas/visualg/tela visualg - 3 - Seção Variáveis de Memória.png)
Esta seção possui 3 colunas, a primeira contem o nome das variáveis, cada variável em uma linha, a segunda coluna o Tipo de variável (C = Caracter, R = Real, I = Inteiro, Etc). Na terceira coluna o valor que se encontra no exato momento na variável.

Veja que esta caixa durante a execução de seu algortimo tem os valores em contante mudança, e quando seu sistema termina a execução ela guarda os ultimos valores utilizados. Isso é muito util para depurar (buscar defeitos, bugs) em sua aplicação.



