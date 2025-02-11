# Exercícios - Polimorfismo

## 1) **Sistema de Pagamentos com Polimorfismo**

#### Descrição:

- Crie um programa que simule um sistema de processamento de pagamentos utilizando o conceito de polimorfismo. 
- O objetivo é demonstrar como diferentes métodos de pagamento podem compartilhar a mesma interface ou classe base, mas implementar comportamentos distintos.

#### Requisitos:

- Criar uma classe base chamada Pagamento com um método chamado:
    - ProcessarPagamento(valor) – que representa o processo genérico de pagamento.
- Criar três classes filhas que herdem de Pagamento:
    - CartaoCredito
        - Implementar o método ProcessarPagamento para exibir: "Pagamento de [valor] processado com cartão de crédito."
    - BoletoBancario
        - Implementar o método ProcessarPagamento para exibir: "Pagamento de [valor] gerado com boleto bancário."
    - Pix
        - Implementar o método ProcessarPagamento para exibir: "Pagamento de [valor] realizado via Pix."
- O programa deve permitir o uso de polimorfismo, ou seja, o mesmo método ProcessarPagamento será chamado de forma genérica para diferentes tipos de pagamento.

#### O programa deve:

- Solicitar ao usuário o tipo de pagamento (cartão de crédito, boleto ou Pix).
- Solicitar o valor do pagamento.
- Criar uma instância da classe correspondente ao método de pagamento.
- Chamar o método ProcessarPagamento de forma polimórfica.

#### Bônus (opcional):

- Implementar uma interface IPagamento (ou equivalente na linguagem escolhida) e fazer com que todas as classes de pagamento implementem essa interface.
- Adicionar um método ValidarPagamento() para verificar, por exemplo, se o valor é positivo antes de processar o pagamento.
- Criar uma opção para o usuário visualizar um relatório de todos os pagamentos realizados durante a execução do programa.

#### Exemplo de Entrada Esperada:

~~~yaml
===== SISTEMA DE PAGAMENTOS =====
1. Cartão de Crédito
2. Boleto Bancário
3. Pix
Escolha o método de pagamento: 2
Digite o valor do pagamento: 150.00
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== PROCESSANDO PAGAMENTO =====
Pagamento de 150.00 gerado com boleto bancário.
~~~

#### Exemplo de Entrada e Saída para Cartão de Crédito:

~~~yaml
===== SISTEMA DE PAGAMENTOS =====
1. Cartão de Crédito
2. Boleto Bancário
3. Pix
Escolha o método de pagamento: 1
Digite o valor do pagamento: 250.75
~~~

~~~yaml
===== PROCESSANDO PAGAMENTO =====
Pagamento de 250.75 processado com cartão de crédito.
~~~
