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

Em Java, toda variável tem um tipo que não pode ser mudado uma vez que declarado.

As variáveis do tipo byte, short, int, long, float, double, char e boolean podem ser declaradas de acordo com uma das formas exibidas abaixo:

|         Declaração        |                         Descrição                         |
| ------------------------  | --------------------------------------------------------- |
| _int_ a, b, c;            | Declarando as variáveis a, b e c.                         |
| _int_ d = 3, e, f=5;      | Declarando d, e, f e inicializando d com 3 e f com 5.     |
| _double_ pi = 3.14159;    | Declarando e inicializando pi com o valor 3.14159;        |
| _char_ x = 'x';           | Declarando e inicializando x com o caractere 'x';         |

### Escopo das variáveis

O escopo da variável é o nome dado ao trecho de código em que aquela variável existe e que é possível acessá-la. 

Quando abrimos um novo bloco com as chaves, as variáveis declaradas ali dentro só valem até o fim daquele bloco.

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

### Operadores Aritméticos

| Operador |                      Operação                      |     Exemplo     |   Resultado   |
| -------- | -------------------------------------------------- | --------------- | ------------- |
|     +    | adição                                             |    x=1+2;       |   x=3         |
|     -    | subtração                                          |    x=3-1;       |   x=2         |
|     *    | multiplicação                                      |    x=2\*3       |   x=6         |
|     /    | divisão                                            |    x=6/2;       |   x=3         |
|     %    | módulo (resto da divisão inteira)                  |    x=7%2;       |   x=1         |
|    ++    | incremento (equivale a x=x+1)                      |    x=1; x++;    |   x=2         |
|    --    | decremento (equivale a x=x-1)                      |    x=1; x--;    |   x=0         |
|    +=    | Soma e atribui (equivale a i=i+2)                  |    i=1; i+=2;   |   i=3         |
|    -=    | Subtrai e atribui (equivale a i=i-2)               |    i=1; i-=2;   |   i=-1        |
|    \*=   | Multiplica e atribui (equivale a i=i\*2)           |    i=1; i*=2;   |   i=2         |
|    /=    | Divide e atribui (equivale a i=i/2)                |    i=2; i/=2;   |   i=1         |
|    %=    | ódulo e atribui (equivale a i=i%2)                 |    i=1; i%=2;   |   i=1         |

### Operadores Relacionais

Para comparar valores são usados os seguintes operadores relacionais:

| Operador |                      Operação                      |
| -------- | -------------------------------------------------- |
|    ==    | Igual a                                            |
|    !=    | Diferente de                                       |
|    >     | Maior que                                          |
|    <     | Menor que                                          |
|    >=    | Maior ou igual que                                 |
|    <=    | Menor ou igual que                                 |

Os operadores relacionais sempre retornam um valor boolean (true ou false) como resultado.

### Operadores Lógicos

Os operadores lógicos operam apenas com operandos (variáveis) do tipo boolean. Esses operadores servem para combinar expressões relacionais e devolvem como resultado um valor boolean (true ou false).

| Operador |                      Operação                      |
| -------- | -------------------------------------------------- |
|    &&    | AND lógico                                         |
|   \|\|   | OR lógico                                          |
|    !     | Negação                                            |

# Vetores Primitivos

Um _array_ é um grupo de variável (elementos ou componentes) que contém valores que são todos do mesmo tipo. Os _arrays_ são objetos, portanto são considerados tipos por referência. Os elementos de um _array_ podem ser de tipos primitivos ou tipos por referência. Para referenciar um elemento particular em um _array_, especificamos o nome da referência para o _array_ e o número de posição do elemento do _array_. O número de posição do elemento é chamado de índice ou subscrito do elemento.

Os objetos de _array_ ocupam espaço na memória. Os _arrays_ são criados com a palavra chave _new_. Para criar um objeto _array_ o programador especifica o tipo dos elementos do _array_ e o número de elementos como para de uma expressão de criação de _array_. Por exemplo:

````java
int v[] = new int[12];
````

Um programa pode criar vários arrays em uma única declaração. Por exemplo:

````java
String b[] = new String[100], x[] = new String[27];
````

É possível inicializar um array com valores literais:

````java
int[] valores = {1,2,3,4,5};
String[] nomes = {"eu","tu"};
````

# Vetores Primitivos Multidimensionais

Um vetor multidimensionais é descrito como uma matriz. Enquanto um vetor tem apenas uma linha com vários valores, uma matriz pode, por exemplo, ter várias linhas com vários valores, que comumente chamamos de linhas e colunas. Para criarmos uma matriz, procedemos da mesma forma que um vetor normal, porém com mais um dimensionador (os colchetes).

Então, se quisermos criar uma matriz bidimensional com 3 linha e 5 colunas, faríamos:

````java
int minhaMatriz [][] = new int [3][5];
````

Podemos inicializar uma matriz diretamente, sem a necessidade de instanciá-lo com new.

````java
int matriz[][] = {{1, 2, 7}, {3, 4, 7}, {8, 9, 7}};
````


