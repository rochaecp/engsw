# Exercícios - Herança

## 1) Sistema de Cadastro de Funcionários com Herança

#### Descrição:

- Crie um programa para gerenciar o cadastro de diferentes tipos de funcionários em uma empresa, utilizando o conceito de herança. 
- O objetivo é demonstrar como uma classe base pode ser estendida por subclasses que herdam atributos e métodos, além de adicionar suas próprias características.

#### Requisitos:

- Criar uma classe base Funcionario com os seguintes atributos:
    - Nome (texto)
    - Idade (número)
    - SalarioBase (número decimal)
- Definir um método na classe base chamado ExibirInformacoes(), que exibe os dados do funcionário.
- Criar duas subclasses que herdam de Funcionario:
    - Gerente:
        - Atributo adicional: BonusGerencial (número decimal)
        - Método sobrescrito ExibirInformacoes() que mostra o salário total (salário base + bônus).
    - Desenvolvedor:
        - Atributo adicional: LinguagemDeProgramacao (texto)
        - Método sobrescrito ExibirInformacoes() que inclui a linguagem de programação na exibição.

#### O programa deve:

- Permitir o cadastro de novos funcionários, solicitando se o usuário deseja cadastrar um Gerente ou um Desenvolvedor.
- Armazenar os funcionários em uma lista.
- Exibir uma lista de todos os funcionários cadastrados, mostrando suas informações específicas (incluindo bônus para gerentes e linguagem de  programação para desenvolvedores).
- Demonstrar o uso de herança e polimorfismo, permitindo que o método ExibirInformacoes() funcione de forma diferente em cada classe derivada.

#### Bônus (opcional):

- Adicionar um terceiro tipo de funcionário, como Estagiário, com um atributo de CargaHorariaSemanal.
- Calcular o salário de estagiários com base em uma taxa horária fixa.
- Implementar uma opção para buscar funcionários pelo nome.
- Permitir a edição de dados de funcionários já cadastrados.
- Implementar uma função para calcular a média salarial da empresa.

#### Exemplo de Entrada Esperada:

~~~yaml
===== SISTEMA DE CADASTRO DE FUNCIONÁRIOS =====
1. Cadastrar Funcionário
2. Listar Funcionários
3. Sair
Escolha uma opção: 1

Qual o tipo de funcionário? (1 - Gerente, 2 - Desenvolvedor): 1
Nome: Maria Silva
Idade: 40
Salário Base: 8000
Bônus Gerencial: 2000
Funcionário cadastrado com sucesso!

Escolha uma opção: 1
Qual o tipo de funcionário? (1 - Gerente, 2 - Desenvolvedor): 2
Nome: João Souza
Idade: 28
Salário Base: 5000
Linguagem de Programação: Python
Funcionário cadastrado com sucesso!
~~~

#### Exemplo de Saída Esperada:

~~~yaml
===== LISTA DE FUNCIONÁRIOS =====
Nome: Maria Silva
Idade: 40
Cargo: Gerente
Salário Total: 10000

Nome: João Souza
Idade: 28
Cargo: Desenvolvedor
Salário Base: 5000
Linguagem de Programação: Python
~~~

#### Exemplo de Erro Controlado:

~~~yaml
Escolha uma opção: 1
Qual o tipo de funcionário? (1 - Gerente, 2 - Desenvolvedor): 3
Opção inválida! Por favor, selecione 1 para Gerente ou 2 para Desenvolvedor.
~~~
