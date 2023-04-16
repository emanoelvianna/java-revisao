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
  System.out.println(“Não pode entrar”);
} else {
  System.out.println(“Pode entrar”);
}
````
Você pode também concatenar expressões booleanas através dos operadores lógicos!

### Operador if-then-else ternário

Uma outra forma de declaração do condicional é a utilização do operador ternário. A estrutura de um operador ternário é compreendida da seguinte forma: ``expressão ? declaração1 : declaração2``

Sua utilização faz todo o sentido quando estmaos trabalhando sobre uma operação simples que irá retornar um valor para apenas duas possibilidades. Por exemplo:

````java
double salario = 1000; 
double bonus = salario * (salario > 1000 ? 0.10 : 0.15); 
System.out.println(bonus);
````

# O while

### O do-while

# O for
