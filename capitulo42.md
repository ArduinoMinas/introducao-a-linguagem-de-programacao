Mesmo nos temos atuais (meados de 2016) onde ferramentas visuais nos permite programar fácilmente para o Arduino usando bloquinhos como se brinca com um quebra cabeça, nós como profissionais precisamos aprender como realmente programar um computador e usarmos uma linguagem, no caso C, que expresse realmente nosso desejo. Sabemos que aluns outros sistemas de grande responsabilidade como por exemplo o Ladder para microcontrolador também usa uma linguagem visual para ajudar a gerir grandes sistemas com complexidade muito elevada, mas sempre acabamos em um determinado momento precisando usar a programação através de um forma textual, para que se torne mais clara e melhor expressa do que o que se pode fazer gráficamente.

Além disso com o crescimento de nosso algoritimo, veremos que manter um diagrama se torna um trabalho cansativo, e ainda é mais fácil manter nosso código através de meios tradicionais como a escrita em uma determinada Linguagem.

Para aprendermos C, precisamos de uma ferramenta similar ao que aprendemos o **Portugol**, algo como o ***VisuAlg***, e descobrimos enão que existe uma ferramenta que leva o nome de seu autor: [PELLEs C](http://pellesc.de), uma ferramenta criada da mesma forma que todas as boas ferramentas foram, um profissional que percebeu uma demanda e foi atrás da solução ideal, não achando ele a desenvolveu.

Porém, Pelles C não é a solução definitiva, haverão no decorrer do nosso amadurecimento como programadores a possiblidade de usarmos outras ferramentas.

#### Opções de IDE Avançadas

Não é preciso se limitar ao uso do Pelles C se você se sente confortável em usar uma ferramena mais avançada, por exemplo o Eclipse com o Plugin CDT que permite programar em C, ou mesmo usando o Visual C++ da Microsoft, ou se preferir ainda há outras educaçionais muito boas que podem ser bem interessante experimentar.

Uma caracteristica do programador é ser objetivo, porém objetividade de mais sem curiosidade se torna uma limitação e prejudica o crescimento, então busque somar a curiosidade, experimente outras ferramentas e veja a diferença entre elas, veja qual você se sente mais confortável.

Mas lembre-se para o objetivo deste curso apenas a Pelles C será considerada como ferramenta de estudo e todo suporte solicitado será considerado sobre ela.

### Baixando e Instalando o PELLES C

O procedimento é simples, visite o site [http://pellesc.de/index.php?page=download&lang=en](http://pellesc.de/index.php?page=download&lang=en), apesar de ser um site alemão está em inglês, o que facilita bastante o entendimento, como pode ver apartir de agora o inglês será nosso segundo idioma. Caso tenha dificuldades use um tradutor como o [Google Translator](http://translator.google.com), você também pode estudar o inglês no site [Duolingo](http://duolingo.com).

Vamos então fazer o Download do Pelles C para o computador, Escolha a versão 32Bits, que rodará bem em qualquer computador.

Após fazer o Download do Pelles C, execute o arquivo `setup.exe`, e prossiga com a instalação padrão, sem alterar nenhum parametro, seguindo clicando no botão **next**, **next** até o fim.

Agora execute o **Pelles C** a seguir veremos como é nossa interface.

### A Interface

A Interface da IDE Peles C é um pouco diferente da IDE VisuAlg 3.0, quando abrimos a aplicação, é apresetnado a janela, como pode ser visto abaixo, temos por padrão o menu, a barra de tarefas, a área principal que no caso do Pelles C permite a abertura de diversas abas com conteúdos diferentes, sendo a primeira a aba com o nome "Start Page",  muito útil para quem está aprendendo.

Nesta aba, são apresentadas ações mais comuns (Common Actions), Projetos recentemente usados (Recent Projects) e sugestões de links para aprendizado e aperfeiçoamento (Links):

![Janela principal da IDE Peles C](telas/pellesc/Pelles C for Windows - 2016-07-09 13.01.48.png)

Vamos começar usando o primeiro programa que todo programador C faz quando está dando seus primeiros passos, o **Hello World**, para isso clique no link `hello PPJ`.

Veremos então uma nova aba sendo aberta como abaixo:

![Abrindo o primeiro programa, Hello World, no Pelles C](telas/pellesc/Pelles C for Windows - Hello World - 2016-07-09 13.21.57.png)

Não iremos entrar em detalhes como é a linguagem C agora, vamos apenas nos atentar para a interface de programação e como usa-la.

#### Conhecendo os Menus

Os menus "File" (Arquivo), "Edit" (Editar), são comuns e tem pouca diferença entre outros softwares que lidam com edição de texto, temos também o menu "View" (Visualizar) que nos ajuda a ter acesso a ***Áreas*** da janela que terão informações relevantes aos arquivos e recursos que estamos utilizando em nosso programa.

O menu mais importante para nós agora é o "Project" (Projeto), que nos dá acesso a todas as ações relativas ao nosso código e o projeto que estamos codificiando.

Como podem ver na imagem a seguir, é no menu "Project" que temos acesso as ações de compilação e depuração do programa (veremos a frente o que é compilação, a depuração é o mesmo conceito que vimos em Portugal, com algumas diferenças no C), no Pelles C as teclas de atalho são diferentes das usadas no VisuAlg.

![Menu Project no Pelles C](telas/pellesc/Pelles C for Windows - Menu Project -  2016-07-09 13.24.51.png)

A Linguagem C é uma linguagem compilada, portanto você tem a opção de gerar um código binário compátivel com o computador no qual pretende executar seu aplicativo, então quando usado a sequencia [CTRL]+[B] seu programa é compilado e gerado um arquivo ***Executável*** do tipo **EXE**, se desejar executar seu programa você deve usar a opção "Execute \*.EXE", onde o asterisco é o nome de seu projeto, ou a sequência [CTRL]+[F5], veja que você pode depurar seu projeto usando a tecla [F5]

#### Ativando Breakpoints

E se desejar inserir um "BreakPoint" em seu projeto, deverá parar sobre a linha desejada como ponto de parada, clicar com o botão direito e selecionar "Toggle Breakpoint", outra forma mais rápida para isso é clicar duas vezes ao lado esquerdo da linha na faixa branca, assim irá aparecer o ponto vermelho que indica que a linha está marcada para depuração. Para desativar siga os mesmo passos sobre a linha que já tem "BreakPoint".

![Ativando Break Point no Pelles C](telas/pellesc/Pelles C for Windows - Ativando BreakPoint -  2016-07-09 13.45.05.png)

Abaixo vemos a linha com o breakpoint ativo:

![Linha com BreakPoint Ativo no Pelles C](telas/pellesc/Pelles C for Windows - BreakPoint Ativo - 2016-07-09 14.04.02.png)

## Próximos Passos

 No próximo passo iremos entender a diferença entre Portugol e Linguagem C no que refere sua relação com o processador, o que são linguagens Compiladas e Interpretadas e como o C é processado para se tornar inteligível pelo micro controlador e assim ser executado adequadamente, o que lhe dá tanto desempenho e por que é tão valorizada pelos profissionais. 


---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
