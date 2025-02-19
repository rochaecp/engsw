# Projeto: PetManager - Sistema de Gestão para PetShops

#### Descrição

- O PetManager é um sistema desenvolvido para gerenciar um PetShop, permitindo o cadastro, gerenciamento e exclusão de clientes, pets, funcionários e produtos. 
- O sistema conta com funcionalidades avançadas de busca, categorização e relacionamento entre entidades, garantindo uma administração eficiente do negócio.
- Gerenciamento de Pets: 
    - Os pets são categorizados em mamíferos, aves e peixes, cada um com atributos e comportamentos distintos.
- Gerenciamento de Funcionários: 
    - Há dois tipos de funcionários, gestores e veterinários, com funções e características específicas.
- Controle de Produtos e Estoque: O sistema permite o registro e gerenciamento de produtos utilizados no PetShop.
- Relacionamentos entre Entidades:
    - Clientes podem possuir vários pets e comprar produtos.
    - O PetShop gerencia clientes, funcionários e produtos.
    - Funcionários incluem gestores e veterinários, com funções distintas.

#### Requisitos

- O sistema deve permitir:
    - Cadastro e gerenciamento de dados:
        - Cadastro de pets com raça, nome e idade.
        - Cadastro de clientes com informações pessoais e seus respectivos pets.
        - Cadastro de funcionários, diferenciando gestores e veterinários.
        - Cadastro de produtos com controle de estoque.
    - Relacionamentos entre entidades:
        - Um cliente pode ter vários pets cadastrados.
        - Clientes podem comprar produtos, criando uma relação de associação.
        - O PetShop deve possuir uma lista de funcionários e produtos disponíveis.
    - Funcionalidades básicas:
        - Cadastro de clientes, pets, funcionários e produtos.
        - Associação de pets aos clientes.
        - Busca eficiente de informações armazenadas.
        - Exclusão de registros conforme necessário.

#### O programa deve

- Cadastrar e associar entidades:
    - Permitir o cadastro de um cliente e vincular a ele seus pets.
    - Cadastrar funcionários, diferenciando gestores e veterinários.
    - Registrar produtos e gerenciar o estoque.
- Realizar buscas eficientes:
    - Buscar pets por nome, raça ou tipo (mamífero, peixe, ave).
    - Consultar o endereço de um cliente específico.
    - Buscar funcionários pelo nome e verificar seus cargos.
    - Localizar produtos cadastrados pelo nome.
- Excluir registros:
    - Remover clientes e seus pets associados.
    - Excluir funcionários ou produtos quando necessário.

#### Bônus

- Relatórios:
    - Gerar um relatório detalhado dos pets cadastrados.
    - Exibir a quantidade de produtos em estoque.
    - Mostrar um resumo com todos os clientes e seus respectivos pets.
- Interface aprimorada:
    - Criar um menu interativo para facilitar a navegação.
    - Adicionar filtros avançados na busca de informações.
- Persistência de dados em banco de dados:
    - Implementar um banco de dados relacional para armazenar as informações do sistema de forma segura e estruturada.
    - Criar tabelas para clientes, pets, funcionários, produtos e suas relações.
    - Utilizar ORM (Object-Relational Mapping) para facilitar a manipulação dos dados.
    - Permitir operações CRUD (Create, Read, Update, Delete) para todas as entidades do sistema.
    - Garantir integridade referencial, assegurando que pets, clientes e funcionários sejam corretamente associados.
    - Implementar backups automáticos para evitar perda de informações.
- Interface Gráfica do Usuário (GUI):
    - Desenvolver uma interface gráfica intuitiva e responsiva para interação com o sistema.
    - A interface deverá ser baseada em formulários, botões e tabelas, permitindo fácil navegação entre as funcionalidades.
    - Principais telas e funcionalidades:
        - Tela Principal:
            - Menu lateral para acessar diferentes seções do sistema.
            - Painel inicial exibindo estatísticas rápidas, como número de pets cadastrados e clientes ativos.
        - Cadastro de Clientes:
            - Formulário para inserir nome, endereço e lista de pets.
            - Botão para adicionar e remover pets associados ao cliente.
            - Botão para salvar ou cancelar o cadastro.
        - Cadastro de Pets:
            - Formulário para adicionar nome, raça, idade e categoria (mamífero, ave ou peixe).
            - Botão para vincular um pet a um cliente existente.
        - Cadastro de Funcionários:
            - Formulário para adicionar nome, cargo (gestor ou veterinário), endereço e salário.
            - Campo de especialidade para veterinários.
        - Cadastro de Produtos:
            - Formulário para adicionar nome do produto, descrição, preço e quantidade em estoque.
            - Botão para ajustar o estoque e visualizar histórico de movimentação.
        - Tela de Busca e Filtros:
            - Campo de pesquisa para buscar clientes, pets, funcionários ou produtos pelo nome.
            - Filtros para refinar a busca, como tipo de pet, cargo do funcionário e faixa de preço de produtos.
            - Listagem interativa dos resultados da busca, com botões para editar ou excluir registros.
        - Tela de Relatórios:
            - Relatório detalhado de clientes e seus pets.
            - Relatório de produtos cadastrados e estoque disponível.
            - Resumo financeiro de gastos com funcionários e faturamento com produtos vendidos.
        - Gestão de Banco de Dados:
            - Tela para backup manual e restauração de dados.
            - Status do banco de dados e número de registros por entidade.
        - Tela de Configurações:
            - Permitir personalização da interface (tema claro/escuro).
            - Configuração de idioma e permissões de usuários.
    - Tecnologias recomendadas para a GUI:
        - JavaFX ou Swing (para aplicações desktop em Java).
        - WinForms ou WPF (para aplicações desktop em .NET - C#).
        - Electron.js (para aplicações multiplataforma baseadas em JavaScript).
        - Frameworks web como React, Angular ou Vue.js para interfaces modernas com integração via API.
    - Benefícios da Interface Gráfica:
        - Melhora a experiência do usuário e torna o sistema mais acessível.
        - Permite um fluxo intuitivo de navegação entre as funções.
        - Facilita o gerenciamento de dados, evitando erros manuais.
        - Aumenta a produtividade, tornando o uso do sistema mais rápido e eficiente.    

#### Exemplo de Entrada Esperada

~~~yaml
Informe o nome do cliente: João Silva  
Informe o endereço do cliente: Rua das Flores, 123  
Quantos pets deseja cadastrar? 2  

Informe o nome do pet: Rex  
Informe a raça: Labrador  
Informe a idade: 3  

Informe o nome do pet: Nina  
Informe a raça: Gato Persa  
Informe a idade: 2  
~~~

#### Exemplo de Saída Esperada

~~~yaml
===== Cadastro Realizado =====  
Cliente: João Silva  
Endereço: Rua das Flores, 123  

Pets Cadastrados:  
1. Rex - Labrador, 3 anos  
2. Nina - Gato Persa, 2 anos  
=================================
~~~

#### Diagrama de Classes

~~~mermaid
classDiagram
    %% classe abstrata
    class Pessoa { 
        <<abstract>>
        - String nome
        - String endereco
        + Getters e Setters
        + exibirInformacoes() virtual
    }

    class Cliente {
        - List~Pet~ pets
        + Getters e Setters 
        
        %% adiciona um objeto da classe Pet à lista de pets do cliente.        
        + adicionarPet(Pet pet) 
        
        %% remove um objeto da classe Pet da lista de pets do cliente.
        + removerPet(Pet pet)   
        
        %% busca e retorna um objeto da classe Pet com base no nome fornecido.
        + buscarPet(String nome) 

        %% sobrescreve exibirInformacoes() para mostrar dados do cliente.
        + exibirInformacoes() override        
    }

    class Funcionario {
        - Float salario
        + String tipo
        + Getters e Setters

        %% sobrescreve exibirInformacoes() para mostrar dados do funcionário.
        + exibirInformacoes() override        
    }

    class Veterinario {
        - String especialidade
        - List~String~ procedimentosRealizados
        + realizarConsulta(Pet pet)
        + prescreverTratamento(Pet pet, String tratamento)
    }

    class Gestor {
        - List~Funcionario~ equipe
        + gerenciarFuncionarios()
        + definirMetas()
    }

    class Pet {
        <<abstract>>
        - String nome
        - String raca
        - Integer idade
        + Getters e Setters
        + emitirSom() virtual        
    }

    class Mamifero {
        - Boolean possuiPelo
        - String tipoAlimentacao
        + amamentar()

        %% sobrescreve emitirSom() para representar som de mamíferos.
        + emitirSom() override        
    }

    class Peixe {
        - String tipoAgua
        - Boolean aguaDoce
        + nadar()

        %% sobrescreve emitirSom() para representar som de peixes (se aplicável).
        + emitirSom() override        
    }

    class Ave {
        - Boolean voa
        - Double envergaduraAsa
        + voar()

        %% sobrescreve emitirSom() para representar canto de aves.
        + emitirSom() override        
    }

    class Produto {
        - String nome
        - Float valor
        - String descricao
        + Getters e Setters
    }

    class PetShop {
        - List~Funcionario~ funcionarios
        - List~Produto~ produtos
        - List~Cliente~ clientes

        %% adiciona um objeto da classe Cliente à lista de clientes do PetShop.
        + cadastrarCliente(Cliente cliente)

        %% adiciona um objeto da classe Funcionário à lista de funcionários do PetShop.
        + cadastrarFuncionário(Funcionario funcionario)
        
        %% adiciona um objeto da classe Produto à lista de produtos do PetShop.
        + cadastrarProduto(Produto produto)

        %% busca e retorna um objeto da classe Cliente com base no nome fornecido.
        + buscarCliente(String nome)

        %% busca e retorna um objeto da classe Funcionário com base no nome fornecido.
        + buscarFuncionário(String nome)

        %% busca e retorna um objeto da classe Produto com base no nome fornecido.
        + buscarProduto(String nome)

        %% remove um objeto.
        + excluirCliente(Cliente cliente)
        + excluirFuncionario (Funcionario funcionario)
        + excluirProduto(Produto produto)
    }
    
    %% Heranças
    Cliente --|> Pessoa
    Funcionario --|> Pessoa
    Veterinario --|> Funcionario
    Gestor --|> Funcionario
    Mamifero --|> Pet
    Peixe --|> Pet
    Ave --|> Pet

    %% Relacionamentos
    Cliente "1" -- "n" Pet : possui
    Cliente "1" -- "n" Produto : pode_comprar
    PetShop "1" -- "n" Cliente : gerencia
    PetShop "1" -- "n" Funcionario : emprega
    PetShop "1" -- "n" Produto : vende
~~~

#### Diagrama de Classes - versão com banco de dados

~~~mermaid
classDiagram
    class Pessoa {
        - String nome
        - String endereco
        + Getters e Setters
        + exibirInformacoes() virtual        
    }

    class Cliente {
        - List~Pet~ pets
        + Getters e Setters 
        
        %% adiciona um objeto da classe Pet à lista de pets do cliente.        
        + adicionarPet(Pet pet) 
        
        %% remove um objeto da classe Pet da lista de pets do cliente.
        + removerPet(Pet pet)   
        
        %% busca e retorna um objeto da classe Pet com base no nome fornecido.
        + buscarPet(String nome) 

        %% sobrescreve exibirInformacoes() para mostrar dados do cliente.
        + exibirInformacoes() override        
    }

    class Funcionario {
        - Float salario
        + String tipo
        + Getters e Setters

        %% sobrescreve exibirInformacoes() para mostrar dados do funcionário.
        + exibirInformacoes() override        
    }

    class Veterinario {
        - String especialidade
        - List~String~ procedimentosRealizados
        + realizarConsulta(Pet pet)
        + prescreverTratamento(Pet pet, String tratamento)
    }

    class Gestor {
        - List~Funcionario~ equipe
        + gerenciarFuncionarios()
        + definirMetas()
    }

    class Pet {
        <<abstract>>
        - String nome
        - String raca
        - Integer idade
        + Getters e Setters
        + emitirSom() virtual        
    }

    class Mamifero {
        - Boolean possuiPelo
        - String tipoAlimentacao
        + amamentar()

        %% sobrescreve emitirSom() para representar som de mamíferos.
        + emitirSom() override        
    }

    class Peixe {
        - String tipoAgua
        - Boolean aguaDoce
        + nadar()

        %% sobrescreve emitirSom() para representar som de peixes (se aplicável).
        + emitirSom() override        
    }

    class Ave {
        - Boolean voa
        - Double envergaduraAsa
        + voar()

        %% sobrescreve emitirSom() para representar canto de aves.
        + emitirSom() override        
    }

    class Produto {
        - String nome
        - Float valor
        - String descricao
        + Getters e Setters
    }

    class PetShop {
        - List~Funcionario~ funcionarios
        - List~Produto~ produtos
        - List~Cliente~ clientes

        %% adiciona um objeto da classe Cliente à lista de clientes do PetShop.
        + cadastrarCliente(Cliente cliente)

        %% adiciona um objeto da classe Funcionário à lista de funcionários do PetShop.
        + cadastrarFuncionário(Funcionario funcionario)
        
        %% adiciona um objeto da classe Produto à lista de produtos do PetShop.
        + cadastrarProduto(Produto produto)

        %% busca e retorna um objeto da classe Cliente com base no nome fornecido.
        + buscarCliente(String nome)

        %% busca e retorna um objeto da classe Funcionário com base no nome fornecido.
        + buscarFuncionário(String nome)

        %% busca e retorna um objeto da classe Produto com base no nome fornecido.
        + buscarProduto(String nome)

        %% remove um objeto.
        + excluirCliente(Cliente cliente)
        + excluirFuncionario(Funcionario funcionario)
        + excluirProduto(Produto produto)
    }

    %% Interface para persistência de dados
    class IRepository {
        <<interface>>
        + salvar(obj: T)
        + atualizar(obj: T)
        + excluir(obj: T)
        + buscarPorId(id: Integer) T
        + buscarTodos() List~T~
    }

    class ClienteRepository {
        + salvar(Cliente cliente)
        + atualizar(Cliente cliente)
        + excluir(Cliente cliente)
        + buscarPorId(Integer id) Cliente
        + buscarTodos() List~Cliente~
    }

    class PetRepository {
        + salvar(Pet pet)
        + atualizar(Pet pet)
        + excluir(Pet pet)
        + buscarPorId(Integer id) Pet
        + buscarTodos() List~Pet~
    }

    class FuncionarioRepository {
        + salvar(Funcionario funcionario)
        + atualizar(Funcionario funcionario)
        + excluir(Funcionario funcionario)
        + buscarPorId(Integer id) Funcionario
        + buscarTodos() List~Funcionario~
    }

    class ProdutoRepository {
        + salvar(Produto produto)
        + atualizar(Produto produto)
        + excluir(Produto produto)
        + buscarPorId(Integer id) Produto
        + buscarTodos() List~Produto~
    }

    class DatabaseConnection {
        + abrirConexao()
        + fecharConexao()
        + executarQuery(String query)
    }

    %% Heranças
    Cliente --|> Pessoa
    Funcionario --|> Pessoa
    Veterinario --|> Funcionario
    Gestor --|> Funcionario
    Mamifero --|> Pet
    Peixe --|> Pet
    Ave --|> Pet

    %% Relacionamentos
    Cliente "1" -- "n" Pet : possui
    Cliente "1" -- "n" Produto : pode_comprar
    PetShop "1" -- "n" Cliente : gerencia
    PetShop "1" -- "n" Funcionario : emprega
    PetShop "1" -- "n" Produto : vende

    %% Implementação da interface Repository
    ClienteRepository --|> IRepository
    PetRepository --|> IRepository
    FuncionarioRepository --|> IRepository
    ProdutoRepository --|> IRepository

    %% DatabaseConnection será utilizado pelos repositórios
    ClienteRepository --o DatabaseConnection
    PetRepository --o DatabaseConnection
    FuncionarioRepository --o DatabaseConnection
    ProdutoRepository --o DatabaseConnection
~~~
