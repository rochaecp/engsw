# Projeto: Store Manager - Sistema de Gestão de Lojas

#### Descrição

- O Store Manager é um sistema para gerenciamento de lojas dentro de um Shopping Center. 
- O sistema permite cadastro e gerenciamento de lojas, produtos, endereços e datas associadas, além de funcionalidades como controle de estoque, emissão de relatórios e categorizção de lojas por segmento.
- Cada loja pode ser de um segmento específico (vestuário, alimentação, lazer, cinema, serviços etc.), e cada espaço do Shopping pode ou não estar ocupado.
- O sistema deve possibilitar operações como adição, modificação e remoção de lojas e produtos, além da consulta de dados.
- O sistema deve implementar herança, polimorfismo, interfaces, classes abstratas, exceções personalizadas, métodos estáticos e enumerações para exercitar diversos conceitos de Orientação a Objetos (OO).
- A imagem abaixo ilustra a estrutura de um Shopping para a finalidade do sistema a ser desenvolvido. 

#### Requisitos

##### Classe Abstrata Loja

- Atributos:
    - `nome` (string)
    - `quantidadeFuncionarios` (inteiro)
    - `salarioBaseFuncionario` (double)
    - `endereco` (Endereco)
    - `dataFundacao` (Data)
    - `estoqueProdutos` (array de Produto) 
- Métodos:
    - Construtores: um que recebe todos os atributos e outro que inicializa `nome` e `quantidadeFuncionarios`, atribuindo `-1` para `salarioBaseFuncionario`.
    - Getters e Setters.
    - toString(): retorna uma string formatada com os dados da loja.
    - gastosComSalario(): retorna o gasto total com salários (se `salarioBaseFuncionario` for `-1`, retorna `-1`).
    - tamanhoDaLoja(): retorna `'P'`, `'M'` ou `'G'` conforme o número de funcionários.
    - insereProduto(Produto p): adiciona um produto ao estoque.
    - removeProduto(String nome): remove um produto pelo nome.
    - imprimeProdutos(): exibe os produtos da loja.
    - calcularImposto() retorna Double (método abstrato - obrigatório para as subclasses).

##### Enum TipoLoja

- A Enum TipoLoja contém os seguintes valores:
    - Cosmetico: Representa lojas especializadas em produtos de beleza e cosméticos.
    - Vestuario: Representa lojas de roupas e acessórios.
    - Bijuteria: Representa lojas que comercializam bijuterias e acessórios.
    - Alimentacao: Representa lojas e restaurantes que vendem alimentos e bebidas.
    - Informatica: Representa lojas especializadas em produtos de tecnologia e informática.

##### Interfaces

- `IImprimivel`
    - Define um contrato para classes que precisam ser exibidas no sistema.
    - Método:
        - `Imprimir() As String` → Retorna uma string formatada contendo os detalhes da classe.
    - Classes que devem implementar:  
        - `Loja`
        - `Produto`
        - `Endereco`
        - `Shopping`
- `ITributavel`
    - Define um contrato para cálculo de impostos sobre lojas.
    - Método:
        - `CalcularImposto() As Double` → Retorna o valor do imposto da loja.
    - Classes que devem implementar:  
        - `Cosmetico`
        - `Vestuario`
        - `Alimentacao`
        - `Informatica`
- `IPersistente`
    - Define um contrato para operações de persistência com banco de dados.
    - Métodos:
        - `Salvar() As Boolean` → Salva os dados da entidade no banco.
        - `Carregar(id As Integer) As Boolean` → Carrega os dados pelo ID.
        - `Excluir() As Boolean` → Remove os dados do banco.
    - Classes que devem implementar:  
        - `Loja`
        - `Produto`
        - `Shopping`
        - `Endereco`

##### Exceções Personalizadas

- `DataInvalidaException`: Para datas inválidas.
- `EstoqueCheioException`: Para quando tenta adicionar um produto a um estoque já cheio.
- `LojaNaoEncontradaException`: Quando uma loja pesquisada não é encontrada.

##### Subclasses de Loja

- Cosmetico: Possui `taxaComercializacao` (double) e implementa `calcularImposto()`.
- Vestuario: Possui `produtosImportados` (booleano).
- Bijuteria: Possui `metaVendas` (double).
- Alimentacao: Possui `dataAlvara` (Data).
- Informatica: Possui `seguroEletronicos` (double).

##### Classe Produto

- Atributos:
    - `nome` (string)
    - `preco` (double)   
    - `dataValidade` (data) 
- Métodos:
    - Construtor para inicializar os atributos.    
    - Getters e Setters.    
    - toString para exibição formatada.
    - estaVencido(Data d) - retorna `true` se estiver vencido na data passada por parâmetro.

##### Classe Endereco

- Atributos:
    - `nomeDaRua`, `cidade`, `estado`, `pais`, `cep`, `numero`, `complemento` (todos string).    
- Métodos:
    - Construtor para inicializar os atributos.    
    - Getters e Setters.    
    - toString para exibição formatada.    

##### Classe Data

- Atributos:
    - `dia`, `mes`, `ano` (inteiros).    
- Métodos:
    - Construtor que valida a data (corrige para `01/01/2000` se for inválida).    
    - Getters e Setters.    
    - toString no formato `dd/mm/aaaa`.    
    - verificaAnoBissexto() retorna `true` se o ano for bissexto, `false` caso contrário.    

##### Classe Estoque

- Atributos:
    - `Loja`, `Produto`, `Quantidade`.
- Relacionamento: 
    - "muitos para muitos" entre lojas e produtos.

##### Classe Shopping     

- Atributos:
    - `nome` (string)  
    - `endereco` (`Endereco`)  
    - `lojas` (array de Loja)  
- Métodos:
    - `insereLoja(Loja l)`: adiciona uma loja ao Shopping.  
    - `removeLoja(String nome)`: remove uma loja pelo nome.  
    - `quantidadeLojasPorTipo(String tipo)`: retorna a quantidade de lojas do tipo informado (`Cosmetico`, `Vestuario`, etc.).  
    - `lojaSeguroMaisCaro()`: retorna a loja de informática com maior seguro.  

##### Classe Main

- Criar a classe Main com o método `main`, exibindo um menu interativo:    
    - (1) Criar uma loja
    - (2) Criar um produto
    - (3) Sair
- Caso o usuário escolha `2`, exibir se o produto está vencido ou não em relação a `20/10/2023`.  
- Caso ele informe um valor inválido, imprima a mensagem “Opção inválida” e mostre o menu novamente, solicitando uma nova opção.
- Depois de criados os 2 objetos corretamente, seu programa deve:
    - Imprimir a mensagem "PRODUTO VENCIDO" ou "PRODUTO NÃO VENCIDO" caso o produto criado esteja vencido na data de 20/10/2023 (utilizando o método criado anteriormente para isso) o imprimir as informações da loja criada. 

#### O programa deve

- Permitir o cadastro e associação de entidades (lojas, produtos, clientes, etc.).  
- Realizar buscas por nome, categoria e outros critérios.  
- Excluir registros quando necessário.  
- Gerenciar estoque de produtos dentro das lojas.  
- Emitir relatórios detalhados sobre as lojas e seus produtos.  

#### Bônus

- Interface Gráfica
    - Criar um menu interativo.
    - Implementar formulários para inserção de dados.
    - Adicionar botões e filtros avançados para busca de informações.
- Persistência de Dados
    - Implementar um banco de dados relacional.
    - Criar tabelas para lojas, produtos, clientes e funcionários.
    - Utilizar um ORM (Object-Relational Mapping).
    - Implementar operações CRUD (Create, Read, Update, Delete).
    - Implementar backups automáticos.

#### Exemplo de Entrada Esperada

~~~yaml
Informe o nome da loja: Tech Store  
Informe o número de funcionários: 15  
Informe o salário base dos funcionários: 2500.00  
Informe o endereço da loja: Rua Central, 123  
Informe a data de fundação: 15/08/2010  
Informe o estoque máximo de produtos: 10 
~~~

#### Exemplo de Saída Esperada

~~~yaml
===== Loja Cadastrada =====  
Nome: Tech Store  
Número de Funcionários: 15  
Salário Base: R$ 2500.00  
Endereço: Rua Central, 123  
Data de Fundação: 15/08/2010  
Estoque Máximo: 10 Produtos  
============================  
~~~

#### Diagrama de Classes

~~~mermaid
classDiagram

    %% CLASSES BASE
    class Loja {
        <<abstract>>
        - String nome
        - int quantidadeFuncionarios
        - double salarioBaseFuncionario
        - Endereco endereco
        - Data dataFundacao
        - Produto[] estoqueProdutos
        %%+ Loja(nome, quantidadeFuncionarios)
        %%+ Loja(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, estoqueMax)
        + double gastosComSalario()
        + char tamanhoDaLoja()
        + boolean insereProduto(Produto p)
        + boolean removeProduto(String nome)
        + void imprimeProdutos()
        + String toString()
        + abstract double calcularImposto()
    }

    class Produto {
        - String nome
        - double preco
        - Data dataValidade
        + Produto(nome, preco, dataValidade)
        + boolean estaVencido(Data d)
        + String toString()
    }

    class Endereco {
        - String nomeDaRua
        - String cidade
        - String estado
        - String pais
        - String cep
        - String numero
        - String complemento
        %%+ Endereco(nomeDaRua, cidade, estado, pais, cep, numero, complemento)
        + String toString()
    }

    class Data {
        - int dia
        - int mes
        - int ano
        + Data(dia, mes, ano)
        + boolean verificaAnoBissexto()
        + String toString()
    }

    class Estoque {
        - Loja loja
        - Produto produto
        - int quantidade
    }    

    class Shopping {
        - String nome
        - Endereco endereco
        - Loja[] lojas
        + Shopping(nome, endereco, maxLojas)
        + boolean insereLoja(Loja l)
        + boolean removeLoja(String nome)
        + int quantidadeLojasPorTipo(String tipo)
        + Loja lojaSeguroMaisCaro()
        + String toString()
    }

    class Main {
        + void main()
    }

    %% HERANÇA - TIPOS DE LOJAS
    class Cosmetico {
        - double taxaComercializacao
        %%+ Cosmetico(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, taxaComercializacao, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Vestuario {
        - boolean produtosImportados
        %%+ Vestuario(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, produtosImportados, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Bijuteria {
        - double metaVendas
        %%+ Bijuteria(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, metaVendas, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Alimentacao {
        - Data dataAlvara
        %%+ Alimentacao(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, dataAlvara, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Informatica {
        - double seguroEletronicos
        %%+ Informatica(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, seguroEletronicos, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    %% INTERFACES
    class IImprimivel {
        + String Imprimir()
    }

    class ITributavel {
        + double CalcularImposto()
    }

    class IPersistente {
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    %% RELACIONAMENTOS
    Loja "1" -- "n" Produto : possui
    Shopping "1" -- "n" Loja : gerencia
    Loja <|-- Cosmetico
    Loja <|-- Vestuario
    Loja <|-- Bijuteria
    Loja <|-- Alimentacao
    Loja <|-- Informatica
    Loja "1" -- "1" Endereco : possui
    Loja "1" -- "1" Data : fundada_em
    Produto "1" -- "1" Data : tem_validade
    Shopping "1" -- "1" Endereco : localizado_em

    %% IMPLEMENTAÇÃO DAS INTERFACES
    Loja ..|> IImprimivel
    Produto ..|> IImprimivel
    Endereco ..|> IImprimivel
    Shopping ..|> IImprimivel

    Cosmetico ..|> ITributavel
    Vestuario ..|> ITributavel
    Alimentacao ..|> ITributavel
    Informatica ..|> ITributavel

    Loja ..|> IPersistente
    Produto ..|> IPersistente
    Shopping ..|> IPersistente
    Endereco ..|> IPersistente
~~~

#### Diagrama de Classes - versão com banco de dados

~~~mermaid
classDiagram

    %% CLASSES BASE
    class Loja {
        <<abstract>>
        - String nome
        - int quantidadeFuncionarios
        - double salarioBaseFuncionario
        - Endereco endereco
        - Data dataFundacao
        - Produto[] estoqueProdutos
        + Loja(nome, quantidadeFuncionarios)
        + Loja(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, estoqueMax)
        + double gastosComSalario()
        + char tamanhoDaLoja()
        + boolean insereProduto(Produto p)
        + boolean removeProduto(String nome)
        + void imprimeProdutos()
        + String toString()
        + abstract double calcularImposto()
    }

    class Produto {
        - String nome
        - double preco
        - Data dataValidade
        + Produto(nome, preco, dataValidade)
        + boolean estaVencido(Data d)
        + String toString()
    }

    class Endereco {
        - String nomeDaRua
        - String cidade
        - String estado
        - String pais
        - String cep
        - String numero
        - String complemento
        + Endereco(nomeDaRua, cidade, estado, pais, cep, numero, complemento)
        + String toString()
    }

    class Data {
        - int dia
        - int mes
        - int ano
        + Data(dia, mes, ano)
        + boolean verificaAnoBissexto()
        + String toString()
    }

    class Estoque {
        - Loja loja
        - Produto produto
        - int quantidade
    }    

    class Shopping {
        - String nome
        - Endereco endereco
        - Loja[] lojas
        + Shopping(nome, endereco, maxLojas)
        + boolean insereLoja(Loja l)
        + boolean removeLoja(String nome)
        + int quantidadeLojasPorTipo(String tipo)
        + Loja lojaSeguroMaisCaro()
        + String toString()
    }

    class Main {
        + void main()
    }

    %% HERANÇA - TIPOS DE LOJAS
    class Cosmetico {
        - double taxaComercializacao
        %%+ Cosmetico(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, taxaComercializacao, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Vestuario {
        - boolean produtosImportados
        %%+ Vestuario(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, produtosImportados, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Bijuteria {
        - double metaVendas
        %%+ Bijuteria(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, metaVendas, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Alimentacao {
        - Data dataAlvara
        %%+ Alimentacao(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, dataAlvara, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    class Informatica {
        - double seguroEletronicos
        %%+ Informatica(nome, quantidadeFuncionarios, salarioBaseFuncionario, endereco, dataFundacao, seguroEletronicos, estoqueMax)
        + double calcularImposto()
        + String toString()
    }

    %% INTERFACES
    class IImprimivel {
        + String Imprimir()
    }

    class ITributavel {
        + double CalcularImposto()
    }

    class IPersistente {
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    %% RELACIONAMENTOS
    Loja "1" -- "n" Produto : possui
    Shopping "1" -- "n" Loja : gerencia
    Loja <|-- Cosmetico
    Loja <|-- Vestuario
    Loja <|-- Bijuteria
    Loja <|-- Alimentacao
    Loja <|-- Informatica
    Loja "1" -- "1" Endereco : possui
    Loja "1" -- "1" Data : fundada_em
    Produto "1" -- "1" Data : tem_validade
    Shopping "1" -- "1" Endereco : localizado_em

    %% IMPLEMENTAÇÃO DAS INTERFACES
    Loja ..|> IImprimivel
    Produto ..|> IImprimivel
    Endereco ..|> IImprimivel
    Shopping ..|> IImprimivel

    Cosmetico ..|> ITributavel
    Vestuario ..|> ITributavel
    Alimentacao ..|> ITributavel
    Informatica ..|> ITributavel

    Loja ..|> IPersistente
    Produto ..|> IPersistente
    Shopping ..|> IPersistente
    Endereco ..|> IPersistente

    %% NOVAS CLASSES PARA PERSISTÊNCIA
    class IRepository {
        <<interface>>
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    class LojaRepository {
        <<interface>>
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    class ProdutoRepository {
        <<interface>>
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    class ShoppingRepository {
        <<interface>>
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    class EnderecoRepository {
        <<interface>>
        + boolean Salvar()
        + boolean Carregar(int id)
        + boolean Excluir()
    }

    class DatabaseConnection {
        - String connectionString
        + boolean conectar()
        + boolean desconectar()
    }

    %% RELACIONAMENTOS DAS NOVAS CLASSES
    IRepository <|.. LojaRepository
    IRepository <|.. ProdutoRepository
    IRepository <|.. ShoppingRepository
    IRepository <|.. EnderecoRepository
    DatabaseConnection "1" -- "n" IRepository : conecta
~~~
