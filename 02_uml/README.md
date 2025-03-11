# UML (Unified Modeling Language - Linguagem de Modelagem Unificada)

- É uma linguagem gráfica de modelagem de sistemas orientados a objetos.
- É um padrão mundialmente aceito
- Link: https://www.uml.org/

## Diagrama de Classes

- Cria-se uma caixa (diagrama UML) com 3 seções: nome da classe, atributos e métodos.

### Associação Simples

#### Exemplo Associação Simples Bidirecional

~~~mermaid
classDiagram
    class Empresa {
        - String nome
        - String cnpj
        + ContratarFuncionario()
    }

    class Funcionario {
        - String nome
        - String cargo
        + Trabalhar()
    }

    Empresa "1" -- "1..*" Funcionario : emprega
~~~

Outra forma:

~~~mermaid
classDiagram
    class Empresa {
        - String nome
        - List<Funcionario> funcionarios
        + void contratar(Funcionario funcionario)
        + void listarFuncionarios()
    }

    class Funcionario {
        - String nome
        - Empresa empresa
        + void trabalhar()
    }

    Empresa "1" --> "many" Funcionario : contrata
    Funcionario "1" --> "1" Empresa : trabalha para
~~~

#### Exemplo Associação Simples Unidirecional

~~~mermaid
classDiagram
    class Carro {
        - Modelo: String
        - Ano: Integer
        - Radio: Radio
        + TocarMusica()
    }

    class Radio {
        - Marca: String
        - Frequencia: Double
        + Ligar()
        + AjustarFrequencia()
    }

    Carro "1" --> "0..*" Radio : pode ter
~~~

### Agregação

#### Exemplo Agregação Unidirecional

~~~mermaid
classDiagram
    class Time {
        - String nome
        - List<Jogador> jogadores
        + adicionarJogador(Jogador j)
    }

    class Jogador {
        - String nome
        + void jogar()
    }

    Time "1" o--> "0..*" Jogador : contém
~~~

### Composição

#### Exemplo Composição Unidirecional

~~~mermaid
classDiagram
    class Casa {
        +String endereco
        +List<Quarto> quartos
        +Casa(endereco: String)
        +adicionarQuarto(quarto: Quarto): void
    }

    class Quarto {
        +String tipo
        +Quarto(tipo: String)
    }

    Casa "1" *-- "1..n" Quarto : contém

~~~

### Dependência

#### Exemplo de Dependência Unidirecional

~~~mermaid
classDiagram
    class Relatorio {
        +gerarRelatorio(impressora: Impressora): void
    }
    class Impressora {
        +imprimir(dados: String): void
    }
    Relatorio ..> Impressora : utiliza
~~~
