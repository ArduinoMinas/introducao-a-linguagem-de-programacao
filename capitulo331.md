## Como tudo é manipulado no computador.

Você já deve ter ouvido falar de **Byte** e **Bit**, e já deve saber que o computador se comunica atráves de eletricidade, com sinais ligados ou desligados, em especial em barramentos de memória, onde isso trafega em uma alta taxa de velocidade, temos processadores ultrapassando a taxa do Ghz, ou seja 1 bilhão de alterações de estados entre 1 e 0 (ligado e desligado) em um dos fios do barramento. Imagine agora que podemos ter barramentos com, 16, 32 e 64bits, portanto trafegando 0s e 1s em 64 vias simultâneas.

Além disso, vemos hoje processadores cada vez maiores sendo capazes de lidar com uma quantidade de Bits simultâneos cada vez maior. O primeiro processador era capaz de lidar com os incríveis 8 bits ou seja um byte por ciclo de clock, hoje temos computadores com 64bits seja 8 bytes o que permite capacidades absurdas de endereçamento de mémoria, a incrível capacidade de 18.446.744.073.709.551.616 (18.446 Teras) posições de memória de tamnhos típicos de um byte. Não chegamos a usar toda esta memória.

Então como podem ver o bit é a menor unidade que um computador consegue lidar hoje, é representado por 0 e 1, já um conjunto de 8 bits é chamado de Byte, e será a unidade que mais usaremos, há também o niple que representa metade de 1 byte, ou seja 4 bits.

Temos também `world` que representam 2 bytes, e `double world` para 4 bytes e `quad world` para 8 bytes.

No universo dos microcontroladores isso não muda, são as mesmas medidas, porém microcontroladores tipo PIC e AVR são normalmente de 16 bits de endereçamento apesar de lidar com 8 bits por vez, há microcontroladores como o ARM que lidam com 32bits e barramentas de endereço do mesmo tamanho, mesmo que não tenham toda a mémoria disponível realmente, parte dela é usada como dispositivos de entrada e saída, e como barramentos de comunicação com ouors dispositivos internos. Veremos isso na [apostila de micro controladores](http://mcu.ed.carlosdelfino.eti.br).

Quando formos estudar a linguagem C, iremos rever os conceitos ligados a unidades de médida de mémoria, por hora, iremos apenas lidar com os tipos de dados aqui presentes e buscar compreende-los de forma simples. Isso se deve ao fato de ser de responsábilidade de outra disciplina tal aprendizado, ou seja "**Introdução a Informática**" ou "**[Introdução a Microcontroladores](http://mcu.ed.carlosdelfino.eti.br)**".

---

Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
