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

Em alguns casos pode ser necessário converter, por exemplo, um double em um inteiro. Toda
conversão numérica em Java é possível, mas informações podem ser perdidas. Estas conversões podem ser
realizadas com o uso de **cast**. A sintaxe do casting é colocar o tipo desejado entre parênteses antes do nome da
variável. Por exemplo:

````java
int tres = 3;
char um = '1';
char quatro = (char) (tres + um);
````

Java permite ainda que certas conversões sejam feitas pela atribuição de valores de um tipo para outro
sem que seja necessário o uso de cast. Por exemplo:

````java
int itres = 3;
double dtres = itres;
````
