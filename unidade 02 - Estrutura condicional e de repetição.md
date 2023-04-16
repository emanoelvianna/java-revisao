# Estrutura condicional e de repetição

Nos exemplos vistos até aqui o fluxo do programa era linear, ou seja, a execução tinha que passar por todas as linhas de comando. Os programas, muitas vezes, vão exigir que certas partes do código sejam ou não executados de acordo com algumas condições. Para isto são usadas declarações de desvio, tais como, if-else, while, for, switch, que serão estudados neste capítulo.

# O if-else

A sintaxe do _if_ no Java é a seguinte:

````java
if (condicaoBooleana) {
  codigo;
}
````

Onde a **condição booleana** é qualquer expressão que retorne _true_ ou _false_. Para isso, você pode usar os operadores <, >, <=, >= e outros. Um exemplo:

````java
int idade = 15;
if (idade < 18) {
  System.out.println("Proibida a entrada de menores de 18.");
}
````

Além disso, você pode usar a cláusula _else_ para indicar o comportamento que deve ser executado no caso da expressão booleana ser falsa:

````java
int idade = 15;
if (idade < 18) {
  System.out.println("Não pode entrar");
} else {
  System.out.println("Pode entrar");
}
````
Você pode também concatenar expressões booleanas através dos operadores lógicos!

````java
int idade = 15;
boolean amigoDoDono = true;
if (idade < 18 & amigoDoDono == false) {
  System.out.println("Não pode entrar");
} else {
  System.out.println("Pode entrar");
}
````

Esse código poderia ainda ficar mais legível, utilizando-se o operador de negação, o !. Esse operador transforma uma expressão booleana de _false_ para _true_ e vice versa.

````java
int idade = 15;
boolean amigoDoDono = true;
if (idade < 18 & !amigoDoDono) {
  System.out.println("Não pode entrar");
} else {
  System.out.println("Pode entrar");
}
````

Para comparar se uma variável tem o mesmo valor que outra variável ou valor, utilizamos o operador ==. Repare que utilizar o operador = vai retornar um erro de compilação, já que o operador = é o de atribuição.

````java
int mes = 1;
if (mes == 1) {
  System.out.println(“Você deveria estar de férias”);
}
````

### Operador if-then-else ternário

Uma outra forma de declaração do condicional é a utilização do operador ternário. A estrutura de um operador ternário é compreendida da seguinte forma: ``expressão ? declaração1 : declaração2``

Sua utilização faz todo o sentido quando estmaos trabalhando sobre uma operação simples que irá retornar um valor para apenas duas possibilidades. Por exemplo:

````java
double salario = 1000; 
double bonus = salario * (salario > 1000 ? 0.10 : 0.15); 
System.out.println(bonus);
````

# O while

O _while_ é um comando usado para fazer um laço (_loop_), isto é, repetir um trecho de código algumas vezes. A idéia é que esse trecho de código seja repetido enquanto uma determinada condição permanecer verdadeira.

````java
int idade = 15;
while(idade < 18) {
  // espera ele crescer
  idade = idade + 1;
}
````

O trecho dentro do bloco do _while_ será executado até o momento em que a condição idade < 18 passe a ser falsa. E isso ocorrerá exatamente no momento em que idade == 18, o que fará imprimir 18.

### O do-while

Às vezes, é desejável executar o corpo de um laço while pelo menos uma vez, quando se quer testar a expressão de encerramento no final do laço ao invés do início (como acontece no while). Para isso, usamos o laço do-while.

````java
int n = 5;
do {
  System.out.println ("tick " + n);
} while (--n > 0);
````

# O for

Outro comando de loop extremamente utilizado é o _for_. A idéia é a mesma do _while_, fazer um trecho de código ser repetido enquanto uma condição continuar verdadeira. Mas além disso, o for isola também um espaço para inicialização de variáveis e o modificador dessas variáveis. Isso faz com que fique mais legível as variáveis que são relacionadas ao loop: ``for (inicializacao; condicao; incremento) { codigo; }``

Um exemplo é o a seguir:

````java
for (int i = 0; i < 10; i = i + 1) {
  System.out.println(“olá!”);
}
````

Repare que esse for poderia ser trocado por:

````java
int i = 0;
while (i < 10) {
  i = i + 1;
  System.out.println(“olá!”);
}
````

Porém, o código do for indica claramente que a variável i serve em especial para controlar a quantidade de laços executados. Quando usar o _for_? Quando usar o _while_? Depende do gosto e da ocasião.


# Controlando loops

Apesar de termos condições booleanas nos nossos laços, em algum momento podemos decidir parar o loop por algum motivo especial, sem que o resto do laço seja executado.

````java
for (int i = x; i < y; i++) {
  if (i % 19 == 0) {
    System.out.println(“Achei um número divisível por 19 entre x e y”);
    break;
   }
}
````

O código acima vai percorrer os números de x a y e parar quando encontrar um número divisível por 19, uma vez que foi utilizada a palavra chave _break_.

Da mesma maneira, é possível obrigar o loop a executar o próximo laço. Para isso usamos a palavra chave _continue_.

````java
for (int i = 0; i < 100; i++) {
  if(i > 50 && i < 60) {
    continue;
  }
  System.out.println(i);
}
````
