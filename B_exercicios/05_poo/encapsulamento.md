# Exercícios - Encapsulamento

## 1) **Sistema de Conta Bancária com Encapsulamento**

#### Descrição:

- Crie um programa para simular o gerenciamento de uma conta bancária, aplicando o conceito de encapsulamento. 
- O objetivo é proteger os dados da conta, controlando o acesso às informações sensíveis e permitindo apenas operações seguras através de métodos públicos.

#### Requisitos:

- Definir uma classe ContaBancaria com as seguintes propriedades privadas:
    - NumeroConta (texto ou número)
    - Titular (texto)
    - Saldo (número decimal) - propriedade privada
Criar métodos públicos para:
    - Obter o saldo atual (método getter)
    - Realizar depósitos (método setter controlado para adicionar saldo)
    - Realizar saques (método que verifica se há saldo suficiente antes de sacar)
    - Exibir as informações da conta, exceto detalhes sensíveis (como o saldo, que só será mostrado por meio do getter)

#### O programa deve:

- Criar uma nova conta bancária solicitando o nome do titular e o número da conta.
- Permitir depósitos e saques, verificando se o saldo é suficiente para o saque.
- Proteger o saldo, impedindo que ele seja alterado diretamente de fora da classe.
- Exibir o saldo atual apenas usando o método getter.
- Continuar executando até o usuário escolher a opção de sair.

#### Bônus (opcional):

- Adicionar uma funcionalidade de limite de crédito para permitir saques mesmo com saldo insuficiente, até um valor pré-definido.
- Implementar uma verificação para impedir depósitos negativos.
- Criar um histórico de transações para registrar depósitos e saques.
- Permitir a criação de múltiplas contas bancárias e gerenciá-las em uma lista.

#### Exemplo de Entrada Esperada:

~~~yaml
===== SISTEMA DE CONTA BANCÁRIA =====
1. Criar Conta
2. Depositar
3. Sacar
4. Ver Saldo
5. Sair
Escolha uma opção: 1

Digite o número da conta: 12345
Digite o nome do titular: João Silva
Conta criada com sucesso!
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== DEPÓSITO =====
Digite o valor para depositar: 500
Depósito realizado com sucesso!

===== SAQUE =====
Digite o valor para sacar: 200
Saque realizado com sucesso!

===== SALDO ATUAL =====
Saldo disponível: 300
~~~

#### Exemplo de Erro Controlado:

~~~yaml
===== SAQUE =====
Digite o valor para sacar: 400
Saldo insuficiente! Operação não realizada.

===== DEPÓSITO =====
Digite o valor para depositar: -50
Valor inválido! O depósito deve ser um valor positivo.
~~~
