# Orientação a Objetos

A orientação a objetos é uma tecnologia de desenvolvimento composta por metodologias e linguagens usada na análise, no projeto e na implementação de programas (Albuquerque, 1999). Para entendermos os conceitos de orientação a objetos é necessário entendermos o que é um objeto. Por exemplo, consideremos objetos do mundo real: seu cachorro, seu computador, sua bicicleta. Os objetos do mundo real têm duas características: eles tem estado e comportamento. Considerando os cachorros, podemos definir os seguintes estados: nome, cor, tamanho, com os seguintes comportamentos: latir, andar, correr.

Objetos de software, assim como objetos do mundo real, possuem estado (variáveis) e comportamento (métodos). Podemos representar objetos do mundo real através de objetos de software (por exemplo, um livro), assim como também podemos modelar conceitos abstratos (por exemplo, uma ação do usuário em uma interface gráfica).

Vamos imaginar um programa para um banco, é bem fácil perceber que uma entidade extremamente importante para o nosso sistema é a conta. Nossa idéia aqui é generalizarmos alguma informação, juntamente com funcionalidades que toda conta deve ter. Pensando nisso poderiamos modelar a conta da seguinte maneira:

````java
public class Conta {
 //TODO: Definição dos métodos e atributos
} 
````

As classes descrevem as informações armazenadas e os serviços providos por um objeto. Em outras palavras, são padrões a partir dos quais os objetos são criados (código).

**Em um programa orientado a objetos, um objeto é uma instância de uma classe**. Os objetos que são instâncias de uma mesma classe armazenam os mesmos tipos de informações e apresentam o mesmo comportamento.

## Variáveis

Cada variável tem um nome e um tipo que define o comportamento estático do objeto. Em Java para cada variável são especificados: um modificador (opcional), o nome, o tipo e o valor inicial (opcional) do atributo. Por exemplo, a classe ContaCorrente possui as variáveis saldo (saldo da conta corrente) e nome (nome do dono da conta). As variáveis de uma classe podem ser de instância ou de classe. Cada classe possui as suas próprias cópias das variáveis de instância, enquanto que as variáveis de classe são compartilhadas.

Pensando na nossa declaração da classe Conta anterior poderiamos adicionar as seguintes variáveis:

````java
public class Conta {
    String documento;
    double saldo;
    
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
public class Conta {
    String documento;
    double saldo;

    double getSaldo() {
        return saldo;
    }

    void depositar(double valor) {
        saldo = saldo + valor;
    }

    void sacar(double valor) {
        if (saldo >= valor) {
            saldo = saldo - valor;
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

A passagem de parâmetros em Java é por valor e não por referência. Por exemplo, não é possível alterar o valor de um parâmetro recebido do tipo primitivo dentro de um método, pois os dados primitivos são passados por valor. Isso significa que o método não tem acesso a variável que foi usada para passar o valor. Um exemplo simples desse comportamento é apresentado no código abaixo:

````java
public static int sucessor(int numero) {
    numero = numero + 1;
    return numero;
}

public static void main(String[] args) {
    int numero = 10;
    System.out.println(sucessor(numero));
    System.out.println(numero);
}
````

Quanto aos objetos, as referências aos objetos também são passadas por valor. Desta maneira, você não pode alterar a variável que referência um objeto, ou seja, não pode fazer com que a variável que referencia o objeto aponte para outro objeto. Mas, pode-se alterar o conteúdo do objeto a qual essa variável referencia, alterando o valor de um de seus atributos. Para entender melhor, veja o exemplo a seguir:

````java
public static void trocarConta(Conta conta) {
    conta = new Conta();
    conta.depositar(200);
}

public static void modificarSaldo(Conta conta) {
    conta.depositar(200);
}

public static void main(String[] args) {
    Conta conta = new Conta();
    conta.depositar(100);
    System.out.println(conta.getSaldo());

    trocarConta(conta);
    System.out.println(conta.getSaldo());

    modificarSaldo(conta);
    System.out.println(conta.getSaldo());
}
````

## Visibilidade

Em Java existem modificadores para determinar a visibilidade das variáveis e métodos. Por exemplo, uma variável ou método public pode ser acessada por outros objetos, porém se for private somente pode ser chamada dentro do próprio objeto. Um bom hábito de programação consiste em deixar privado (private) tudo aquilo que não precisa ser acessado por um método de outro objeto. Veja na tabela abaixo, os modificadores existentes em Java:

|     Encapsulamento        |                                                   Visibilidade                                                          |
| ------------------------  | ----------------------------------------------------------------------------------------------------------------------- |
| _private_                 | Podem ser acessados somente por métodos da mesma classe                                                                 |
| _protected_               | Podem ser acessados pelas classes do mesmo pacote, como também pelas subclasses do mesmo pacote e de outros pacotes.    |
| sem modificador           | Podem ser acessados por subclasses do mesmo pacote ou por outras classes do mesmo pacote.                               |
| _public_                  | Podem ser acessados de qualquer classe.                                                                                 |


