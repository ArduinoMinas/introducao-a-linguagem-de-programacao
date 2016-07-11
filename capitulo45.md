Em C temos as mesmas estruturas de controle que aprendemos no **Portugol** do **VisuAlg**.

## IF ELSE

A estrutura de controle `if` é a mesma estrutura `se` do portugol, e `else`é como `senao`em portugol, e deve ser escrita em C como apresentada abaixo:

```
if (x < y) 
{
  printf("X é menor que Y");
}
else
{
  printf("X é maior que Y");
}
```

Veja que no C, uma estrutura de controle se asssemelha a funções, mas não são, no caso entre parenteses se encontra a operação lógica desejada.

É importante observar que os blocos de códigos escolhidos a executar nas estrutura de controle são delimitados por pares **{** e **}**.

É também importante saber, que as variáveis que forem declaradas internamente nestes blocos são vistas apenas localmente, e são recriadas sempre que os blocos são executados, portanto tenha cautela ao criar variáveis dentro de blocos de controle.

## FOR

A a operação de controle `for` é o mesmo que o `para` em portugol, tendo 