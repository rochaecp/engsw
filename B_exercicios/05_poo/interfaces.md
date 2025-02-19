# Exercícios - Interfaces

## 1) **Sistema de Pagamentos com Interfaces**

#### Descrição

- Crie um programa que simule um sistema de pagamentos para diferentes métodos, utilizando o conceito de interfaces. 
- O objetivo é demonstrar como interfaces permitem definir contratos que garantem a implementação de métodos específicos em diferentes classes.

#### Requisitos

- Criar uma interface chamada IPagamento com o seguinte método:
    - RealizarPagamento(valor) – responsável por processar o pagamento de um determinado valor.
- Criar duas classes que implementem a interface IPagamento:
    - CartaoCredito
        - Deve implementar o método RealizarPagamento, exibindo uma mensagem de que o pagamento foi feito com cartão de crédito.
        - Ter um atributo adicional: NumeroCartao para simular o número do cartão.
    - BoletoBancario
        - Deve implementar o método RealizarPagamento, exibindo uma mensagem de que o pagamento foi feito por boleto.
        - Ter um atributo adicional: CodigoBarras para simular o código do boleto.

#### O programa deve

- Permitir que o usuário escolha o método de pagamento (cartão de crédito ou boleto bancário).
- Solicitar as informações necessárias (número do cartão ou código de barras) e o valor do pagamento.
- Processar o pagamento chamando o método RealizarPagamento da classe correspondente.
- Demonstrar o uso de polimorfismo, já que o mesmo método (RealizarPagamento) funciona de forma diferente em cada classe.

#### Bônus

- Implementar uma terceira forma de pagamento, como Pix, com um atributo de ChavePix.
- Criar uma interface adicional ICancelamento, com o método CancelarPagamento(), e implementar esse recurso nas classes de pagamento.
- Adicionar validação de dados, como verificar se o número do cartão ou o código de barras tem o formato correto.
- Criar um histórico de pagamentos realizados, armazenando as transações em uma lista e permitindo exibir todas as operações.

#### Exemplo de Entrada Esperada

~~~yaml
===== SISTEMA DE PAGAMENTOS =====
1. Pagar com Cartão de Crédito
2. Pagar com Boleto Bancário
Escolha uma opção: 1

Digite o número do cartão: 1234-5678-9012-3456
Digite o valor do pagamento: 150.75
Pagamento realizado com sucesso usando Cartão de Crédito!
Valor: R$ 150.75
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== PAGAMENTO CONCLUÍDO =====
Método: Cartão de Crédito
Número do Cartão: 1234-5678-9012-3456
Valor: R$ 150.75
-------------------------------
~~~

#### Exemplo de Pagamento com Boleto:

~~~yaml
===== SISTEMA DE PAGAMENTOS =====
1. Pagar com Cartão de Crédito
2. Pagar com Boleto Bancário
Escolha uma opção: 2

Digite o código de barras do boleto: 00190500954014481606906809350314337370000000100
Digite o valor do pagamento: 500.00
Pagamento realizado com sucesso usando Boleto Bancário!
Valor: R$ 500.00
~~~