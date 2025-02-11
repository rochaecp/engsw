# Exercícios - Sobrescrita

## 1) **Sistema de Veículos com Sobrescrita de Métodos**

#### Descrição:

- Crie um programa que simule um sistema de veículos para diferentes tipos de transporte, utilizando o conceito de sobrescrita de métodos. 
- O objetivo é demonstrar como uma classe filha pode alterar o comportamento de um método herdado da classe pai.

#### Requisitos:

- Criar uma classe base chamada Veiculo com o seguinte método:
    - ExibirInformacoes() – responsável por exibir informações genéricas de um veículo, como "Este é um veículo."
- Criar duas classes filhas que herdem de Veiculo:
    - Carro
        - Deve sobrescrever o método ExibirInformacoes para exibir: "Este é um carro. Ele possui 4 rodas e é movido a gasolina."
    - Moto
        - Deve sobrescrever o método ExibirInformacoes para exibir: "Esta é uma moto. Ela possui 2 rodas e é movida a gasolina."
- Utilizar o conceito de polimorfismo, permitindo que o mesmo método (ExibirInformacoes) tenha comportamentos diferentes dependendo da classe.

#### O programa deve:

- Permitir que o usuário escolha o tipo de veículo (carro ou moto).
- Criar uma instância da classe correspondente.
- Chamar o método ExibirInformacoes para exibir as informações específicas do veículo.
- Demonstrar a sobrescrita de métodos de forma clara.

#### Bônus (opcional):

- Criar uma terceira classe chamada Caminhao, sobrescrevendo o método para exibir: "Este é um caminhão. Ele possui 6 rodas e é usado para transporte de cargas."
- Implementar um método adicional chamado CalcularAutonomia(distancia, consumo) na classe base e sobrescrever esse método nas classes filhas para simular cálculos de autonomia específicos para cada tipo de veículo.
- Adicionar um menu de repetição, permitindo ao usuário realizar várias consultas sem encerrar o programa.

#### Exemplo de Entrada Esperada:

~~~yaml
===== SISTEMA DE VEÍCULOS =====
1. Carro
2. Moto
Escolha o tipo de veículo: 1
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== INFORMAÇÕES DO VEÍCULO =====
Este é um carro. Ele possui 4 rodas e é movido a gasolina.
~~~

#### Exemplo de Entrada e Saída para Moto:

~~~yaml
===== SISTEMA DE VEÍCULOS =====
1. Carro
2. Moto
Escolha o tipo de veículo: 2
~~~

~~~yaml
===== INFORMAÇÕES DO VEÍCULO =====
Esta é uma moto. Ela possui 2 rodas e é movida a gasolina.
~~~
