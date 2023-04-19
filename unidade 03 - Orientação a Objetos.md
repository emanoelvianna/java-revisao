# Orientação a Objetos

A orientação a objetos é uma tecnologia de desenvolvimento composta por metodologias e linguagens usada na análise, no projeto e na implementação de programas (Albuquerque, 1999). Para entendermos os conceitos de orientação a objetos é necessário entendermos o que é um objeto. Por exemplo, consideremos objetos do mundo real: seu cachorro, seu computador, sua bicicleta. Os objetos do mundo real têm duas características: eles tem estado e comportamento. Considerando os cachorros, podemos definir os seguintes estados: nome, cor, tamanho, com os seguintes comportamentos: latir, andar, correr.

Objetos de software, assim como objetos do mundo real, possuem estado (variáveis) e comportamento (métodos). Podemos representar objetos do mundo real através de objetos de software (por exemplo, um livro), assim como também podemos modelar conceitos abstratos (por exemplo, uma ação do usuário em uma interface gráfica).

Vamos imaginar um programa para um banco, é bem fácil perceber que uma entidade extremamente importante para o nosso sistema é a conta. Nossa idéia aqui é generalizarmos alguma informação, juntamente com funcionalidades que toda conta deve ter. Pensando nisso poderiamos modelar a conta da seguinte maneira:

````java
class Conta {
 // Definição dos métodos e atributos
} 
````

As classes descrevem as informações armazenadas e os serviços providos por um objeto. Em outras palavras, são padrões a partir dos quais os objetos são criados (código).

**Em um programa orientado a objetos, um objeto é uma instância de uma classe**. Os objetos que são instâncias de uma mesma classe armazenam os mesmos tipos de informações e apresentam o mesmo comportamento.

## Variáveis 

## Métodos

### Métodos Construtores

## Instanciando uma classe

## Operador _this_

## Acessando métodos e variáveis de um objeto

## Sobrecarga de Métodos (Overloading)

## Passagem de Parâmetros em Java

## Visibilidade

|     Encapsulamento        |                                                   Visibilidade                                                          |
| ------------------------  | ----------------------------------------------------------------------------------------------------------------------- |
| _private_                 | Podem ser acessados somente por métodos da mesma classe                                                                 |
| _protected_               | Podem ser acessados pelas classes do mesmo pacote, como também pelas subclasses do mesmo pacote e de outros pacotes.    |
| sem modificador           | Podem ser acessados por subclasses do mesmo pacote ou por outras classes do mesmo pacote.                               |
| _public_                  | Podem ser acessados de qualquer classe.                                                                                 |


