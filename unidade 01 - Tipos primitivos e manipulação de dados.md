# Tipos primitivos e manipulação de dados

## Tipos Primitivos de Dados (Tipos Nativos de Dados)

Java tem oito tipos simples de dados que podem ser classificados em quatro grupos:

- **Inteiros**: _byte_, _short_, _int_ e _long_ que são usados para números inteiros.
- **Números de Ponto flutuante**: _float_ e _double_ que correspondem aos números com precisão de fração.
- **Caracteres**: _char_.
- **Valores lógicos**: _boolean_ que é um tipo especial usado para representar valores lógicos.

Qualquer operação numérica em variáveis de tipos diferentes será realizada da seguinte maneira:

- Se um dos operandos é do tipo double, o outro será tratado como um double no escopo da operação;
- Senão, se um dos operandos for float, o outro será tratado como float;
- Senão, se um dos operandos é do tipo long, o outro será tratado como long.
- Senão, os operandos serão tratados como inteiros

Em alguns casos pode ser necessário converter, por exemplo, um double em um inteiro. Toda conversão numérica em Java é possível, mas informações podem ser perdidas. Estas conversões podem ser realizadas com o uso de **cast**. A sintaxe do casting é colocar o tipo desejado entre parênteses antes do nome da variável. Por exemplo:

````java
int tres = 3;
char um = '1';
char quatro = (char) (tres + um);
````

Java permite ainda que certas conversões sejam feitas pela atribuição de valores de um tipo para outro sem que seja necessário o uso de cast. Por exemplo:

````java
int itres = 3;
double dtres = itres;
````

As conversões permitidas de forma automática pelo compilador são: ````byte -> short -> int -> long -> float -> double````.

## Declaração e Inicialização de Valores

As variáveis do tipo byte, short, int, long, float, double, char e boolean podem ser declaradas de acordo com uma das formas exibidas abaixo:

|         Declaração        |                         Descrição                         |
| ------------------------  | --------------------------------------------------------- |
| _int_ a, b, c;            | Declarando as variáveis a, b e c.                         |
| _int_ d = 3, e, f=5;      | Declarando d, e, f e inicializando d com 3 e f com 5.     |
| _double_ pi = 3.14159;    | Declarando e inicializando pi com o valor 3.14159;        |
| _char_ x = 'x';           | Declarando e inicializando x com o caractere 'x';         |

## Constantes

Em Java não podem ser definidas constantes locais para um determinado método como, por exemplo, o main. Ao invés disso, pode haver somente constantes para todos os métodos na classe. Elas são chamadas usualmente de constantes de classe. As constantes são sempre definidas através dos modificadores static final. Por exemplo:

````java
public class Application {
    public static double PI = 3.14;
    public static void main(String[] args) {
        System.out.println(PI);
    }
}
````

## Operadores

Existem quatro tipos de operadores em Java: aritméticos, bit-a-bit, relacional e lógico.

| Operador |    Operação    |   Exemplo   |   Resultado   |
| -------- | -------------- | ----------- | ------------- |
|     +    | adição                                 | x=1+2; | x=3 |
|     -    | subtração                              | x=3-1; | x=2 |
|     *    | multiplicação                          | x=2\*3 | x=6 |
|     /    | divisão                                | x=6/2; | x=3 |
|     %    | módulo (resto da divisão inteira)      | x=7%2; | x=1 |
|    ++    | incremento (equivale a x=x+1)          | x=1; x++; | x=2 |
|    --    | decremento (equivale a x=x-1)              | x=1; x--; | x=0 |
|    +=    | Soma e atribui (equivale a i=i+2)          | i=1; i+=2; | i=3 |
|    -=    | Subtrai e atribui (equivale a i=i-2)       | i=1; i-=2; | i=-1 |
|    \*=   | Multiplica e atribui (equivale a i=i\*2)   | i=1; i*=2; | i=2 |
|    /=    | Divide e atribui (equivale a i=i/2) | i=2; i/=2; | i=1 |
|    %=    | ódulo e atribui (equivale a i=i%2) | i=1; i%=2; | i=1 |



