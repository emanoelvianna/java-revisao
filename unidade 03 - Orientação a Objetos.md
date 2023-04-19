# Orientação a Objetos

A orientação a objetos é uma tecnologia de desenvolvimento composta por metodologias e linguagens usada na análise, no projeto e na implementação de programas (Albuquerque, 1999). Para entendermos os conceitos de orientação a objetos é necessário entendermos o que é um objeto. Por exemplo, consideremos objetos do mundo real: seu cachorro, seu computador, sua bicicleta. Os objetos do mundo real têm duas características: eles tem estado e comportamento. Considerando os cachorros, podemos definir os seguintes estados: nome, cor, tamanho, com os seguintes comportamentos: latir, andar, correr.

Objetos de software, assim como objetos do mundo real, possuem estado (variáveis) e comportamento (métodos). Podemos representar objetos do mundo real através de objetos de software (por exemplo, um livro), assim como também podemos modelar conceitos abstratos (por exemplo, uma ação do usuário em uma interface gráfica).

Vamos imaginar um programa para um banco, é bem fácil perceber que uma entidade extremamente importante para o nosso sistema é a conta. Nossa idéia aqui é generalizarmos alguma informação, juntamente com funcionalidades que toda conta deve ter. Pensando nisso poderiamos modelar a conta da seguinte maneira:

````java
class Conta {
 //TODO: Definição dos métodos e atributos
} 
````

As classes descrevem as informações armazenadas e os serviços providos por um objeto. Em outras palavras, são padrões a partir dos quais os objetos são criados (código).

**Em um programa orientado a objetos, um objeto é uma instância de uma classe**. Os objetos que são instâncias de uma mesma classe armazenam os mesmos tipos de informações e apresentam o mesmo comportamento.

## Variáveis

Cada variável tem um nome e um tipo que define o comportamento estático do objeto. Em Java para cada variável são especificados: um modificador (opcional), o nome, o tipo e o valor inicial (opcional) do atributo. Por exemplo, a classe ContaCorrente possui as variáveis saldo (saldo da conta corrente) e nome (nome do dono da conta). As variáveis de uma classe podem ser de instância ou de classe. Cada classe possui as suas próprias cópias das variáveis de instância, enquanto que as variáveis de classe são compartilhadas.

Pensando na nossa declaração da classe Conta anterior poderiamos adicionar as seguintes variáveis:

````java
class Conta {
 static float dinheiroTotal;
 float saldo;
 String nome;
 
 //TODO: adicionar os métodos relacionados 
} 
````

## Métodos

Os métodos definem os serviços que podem ser solicitados a uma instância (objeto), ou seja, o comportamento dinâmico de um objeto. A definição de um método em Java inclui um modificador (opcional), o tipo do dado retornado após a execução do método, o nome do método, o nome e tipo dos parâmetros e o código delimitado por chaves ( { } ).

Por exemplo, na classe ContaCorrente podem ser definidos os métodos:

````
verificaSaldo: retorna o saldo da conta corrente;
depositaValor: deposita um valor especificado x na conta;
retiraValor: retira um valor especificado x da conta;
````

A definição da classe Conta anteriomemnte definida com as variáveis e métodos é a seguinte:

````java
class ContaCorrente {
 static float dinheiroTotal;
 float saldo;
 String nome;

 float verificaSaldo ( ) {
  return saldo;
 }

 void depositaValor (float valor) {
  saldo = saldo + valor;
  dinheiroTotal += valor;
 }

 void retiraValor (float valor) {
  if (saldo>=valor) {
   saldo = saldo – valor;
   dinheiroTotal -= valor;
  }
 }
}
````


### Métodos Construtores

## Instanciando uma classe

## Operador _this_

## Acessando métodos e variáveis de um objeto

## Sobrecarga de Métodos (Overloading)

## Passagem de Parâmetros em Java

## Visibilidade

Em Java existem modificadores para determinar a visibilidade das variáveis e métodos. Por exemplo, uma variável ou método public pode ser acessada por outros objetos, porém se for private somente pode ser chamada dentro do próprio objeto. Um bom hábito de programação consiste em deixar privado (private) tudo aquilo que não precisa ser acessado por um método de outro objeto. Veja na tabela abaixo, os modificadores existentes em Java:

|     Encapsulamento        |                                                   Visibilidade                                                          |
| ------------------------  | ----------------------------------------------------------------------------------------------------------------------- |
| _private_                 | Podem ser acessados somente por métodos da mesma classe                                                                 |
| _protected_               | Podem ser acessados pelas classes do mesmo pacote, como também pelas subclasses do mesmo pacote e de outros pacotes.    |
| sem modificador           | Podem ser acessados por subclasses do mesmo pacote ou por outras classes do mesmo pacote.                               |
| _public_                  | Podem ser acessados de qualquer classe.                                                                                 |


