## conversão de tipos

Antes de continuarmos é importante compreendermos o que acontece quando envolvemos tipos de dados diferentes em operações matemáticas, temos dois típos de conversão, a conversão do tipo **Down Casting** onde um tipo mais complexo ou de maior precisão é convertido para um tipo de menor tamanho ou precisão. Já a conversão do tipo **Up Casting** faz exatamente o inverso, tipos menos complexos são convertidos em tipos maiores ou mais complexos.

Outro problemas que podemos ter ao fazermos um `down casting` é a perda de dados, por exemplo ao converter um Long para Short, perdemos 2 bytes de precisão, então um valor em hexa como este `0xFEFAFBFC` o que equivale a `4277861372` em decimal, visivelmente um `long` se for feito um downcast para `inteiro` teremos a perda de dois bytes mais significativo, portanto teremos o valor em hexa `0xFBFC` o que equivale em decimal a `64508`.Como ser visto facilmente com números em hexa, é perdido os dois bytes mais altos, de maior valor (MSB - Most significant Bytes) e isso é uma falha comum quando se lida com sistemas escritos em C, e futuramente quando formos lidar com o Arduino e transmissão de dados, precisamos cuidar atentamente disso.

---
Revisado: {{ file.mtime }} | Compilado: {{ gitbook.time }}
---
