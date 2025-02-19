# Projeto: Sistema de Gestão de Zoológico

#### Descrição

- Você foi contratado para desenvolver um sistema de gestão para um zoológico. 
- O sistema deve permitir o cadastro de diferentes tipos de animais, gerenciar funcionários responsáveis pelo cuidado dos animais e permitir a realização de atividades diárias, como alimentação e tratamento veterinário. 
- O sistema deve utilizar conceitos de orientação a objetos, garantindo o uso adequado de encapsulamento, herança, polimorfismo e abstração.

#### Requisitos

- O sistema deve ter uma classe abstrata chamada Animal, que representa qualquer animal no zoológico.
- Devem existir classes concretas que herdam de Animal, como Mamifero, Ave, Reptil, e subclasses mais específicas como Leao, Elefante, Papagaio e Cobra.
- A classe Funcionario deve ter subclasses específicas como Veterinario e Cuidador, cada uma com métodos distintos.
- Cada animal deve ter um método polimórfico chamado EmitirSom(), que será implementado de forma diferente para cada tipo de animal.
- Os funcionários devem poder executar ações específicas de acordo com seu tipo, como alimentar os animais ou realizar tratamentos.
- Os dados dos animais e funcionários devem ser encapsulados usando modificadores de acesso adequados.
- Deve haver uma classe Zoologico que gerencie os registros de animais e funcionários.

#### O programa deve

- Permitir o cadastro de novos animais no zoológico, especificando seu nome, idade e tipo.
- Permitir o cadastro de funcionários, especificando o nome, cargo e especialidade.
- Permitir que os funcionários realizem suas atividades:
    - O Cuidador pode alimentar os animais.
    - O Veterinario pode realizar tratamentos nos animais.
- Exibir um relatório contendo:
    - Lista de animais e seus respectivos sons.
    - Lista de funcionários e suas funções.
    - Registro das atividades realizadas.

#### Bônus

- Implementar um sistema de alimentação, onde cada animal tem um tipo específico de comida.
- Criar um histórico de tratamentos, armazenando os registros das visitas veterinárias de cada animal.
- Permitir a remoção de animais do zoológico quando necessário.

#### Exemplo de Entrada Esperada

~~~yaml
1. Adicionar Animal
2. Adicionar Funcionário
3. Listar Animais
4. Listar Funcionários
5. Executar Ação de Funcionário
6. Sair

Escolha uma opção: 1
Digite o tipo de animal (Mamífero, Ave, Réptil): Mamífero
Digite o nome do animal: Simba
Digite a idade do animal: 5
Animal adicionado com sucesso!

Escolha uma opção: 2
Digite o cargo (Veterinario ou Cuidador): Veterinario
Digite o nome do funcionário: Dr. João
Digite a especialidade: Animais Selvagens
Funcionário adicionado com sucesso!

Escolha uma opção: 5
Digite o nome do funcionário: Dr. João
Digite o nome do animal: Simba
Ação realizada: Dr. João tratou Simba.
~~~

#### Exemplo de Saída Esperada

~~~yaml
Lista de Animais:
- Simba (Mamífero) - Som: Rugido
- Kaa (Réptil) - Som: Sssss

Lista de Funcionários:
- Dr. João (Veterinário) - Especialidade: Animais Selvagens
- Ana (Cuidadora) - Responsável por alimentação

Registro de Atividades:
- Dr. João tratou Simba.
- Ana alimentou Kaa.
~~~

- Este exercício cobre os quatro pilares da orientação a objetos:
    - Encapsulamento: Uso de atributos privados e métodos de acesso.
    - Herança: Classes que estendem Animal e Funcionario.
    - Polimorfismo: Método EmitirSom() sendo sobrescrito por diferentes tipos de animais.
    - Abstração: Uso de uma classe abstrata Animal para definir um modelo genérico.
- Este sistema pode ser expandido com novos tipos de animais, ações e funcionários, incentivando a compreensão profunda de orientação a objetos.

#### Diagrama de Classes

~~~mermaid
classDiagram
    class Animal {
        +nome: String
        +idade: int
        +EmitirSom(): void
    }
    
    class Mamifero {
        +EmitirSom(): void
    }
    
    class Ave {
        +EmitirSom(): void
    }
    
    class Reptil {
        +EmitirSom(): void
    }

    class Leao {
        +EmitirSom(): void
    }

    class Elefante {
        +EmitirSom(): void
    }

    class Papagaio {
        +EmitirSom(): void
    }

    class Cobra {
        +EmitirSom(): void
    }

    class Funcionario {
        +nome: String
        +ExecutarAcao(Animal): void
    }

    class Veterinario {
        +especialidade: String
        +ExecutarAcao(Animal): void
    }

    class Cuidador {
        +ExecutarAcao(Animal): void
    }

    class Zoologico {
        +animais: List<Animal>
        +funcionarios: List<Funcionario>
        +AdicionarAnimal(animal: Animal): void
        +AdicionarFuncionario(funcionario: Funcionario): void
        +ListarAnimais(): void
        +ListarFuncionarios(): void
    }

    Animal <|-- Mamifero
    Animal <|-- Ave
    Animal <|-- Reptil

    Mamifero <|-- Leao
    Mamifero <|-- Elefante

    Ave <|-- Papagaio
    Reptil <|-- Cobra

    Funcionario <|-- Veterinario
    Funcionario <|-- Cuidador

    Zoologico o-- Animal
    Zoologico o-- Funcionario
~~~