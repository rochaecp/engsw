# Especificação de Projeto: Sistema de Gestão de Cidade Inteligente (SmartCity)

## 1. Visão Geral
O **Sistema de Gestão de Cidade Inteligente (SmartCity)** é um software orientado a objetos que gerencia diferentes setores de uma cidade, como transporte, segurança, iluminação pública, saneamento, energia, saúde e serviços administrativos. O objetivo do sistema é integrar informações e otimizar a administração urbana, melhorando a qualidade de vida dos cidadãos.

Este projeto explora **todos os principais conceitos da orientação a objetos**, como **encapsulamento, abstração, herança e polimorfismo**, garantindo modularidade e escalabilidade.

## 2. Escopo do Sistema
O sistema será dividido em **módulos independentes**, mas integrados, permitindo que diferentes departamentos da cidade interajam de maneira eficiente.

### Principais módulos:
1. **Gerenciamento de Transporte Público**  
   - Cadastro e rastreamento de ônibus e metrôs.  
   - Monitoramento de fluxo de passageiros.  
   - Controle de bilhetagem eletrônica.  

2. **Segurança e Monitoramento**  
   - Cadastro de câmeras de vigilância e reconhecimento facial.  
   - Integração com delegacias e patrulhas policiais.  
   - Alerta automático de eventos suspeitos.  

3. **Iluminação Pública e Energia**  
   - Monitoramento de postes de luz e consumo de energia.  
   - Automatização de acendimento e desligamento.  

4. **Saúde e Emergências**  
   - Cadastro de hospitais, clínicas e ambulâncias.  
   - Monitoramento de pacientes em tempo real.  
   - Controle de estoque de medicamentos.  

5. **Saneamento e Coleta de Lixo**  
   - Roteirização de caminhões de lixo.  
   - Sensores para alertar sobre acúmulo de resíduos.  

6. **Serviços Administrativos e Cidadãos**  
   - Portal do cidadão para solicitações de serviços.  
   - Agendamento de consultas e atendimentos públicos.  

## 3. Modelagem Orientada a Objetos
O sistema será desenvolvido utilizando **Programação Orientada a Objetos (POO)**, garantindo modularidade, reuso de código e organização.

### 3.1 Classes Abstratas e Interfaces
- `EntidadeCidade`: Classe abstrata que representa qualquer elemento da cidade (veículos, prédios, cidadãos).  
- `ISensor`: Interface para sensores integrados ao sistema (câmeras, detectores de presença, medidores de qualidade do ar).  

### 3.2 Herança e Especialização
- `Veiculo` (superclasse) → `Onibus`, `Metro`, `Ambulancia`, `ViaturaPolicial`.  
- `FuncionarioPublico` (superclasse) → `Policial`, `Medico`, `Motorista`.  

### 3.3 Encapsulamento
Cada classe possui **atributos privados** e métodos de acesso (`getters` e `setters`), garantindo a segurança e integridade dos dados.

### 3.4 Polimorfismo
Os sensores implementam a interface `ISensor`, permitindo que diferentes tipos de sensores (câmeras, sensores de tráfego, detectores de fumaça) sejam manipulados de forma uniforme.

## 4. Requisitos Funcionais
1. **Cadastro e Gerenciamento**  
   - O sistema deve permitir o cadastro de veículos, sensores, funcionários e cidadãos.  

2. **Monitoramento em Tempo Real**  
   - O sistema deve atualizar o status dos serviços públicos em tempo real.  

3. **Gerenciamento de Eventos e Alertas**  
   - O sistema deve gerar alertas automáticos para emergências, como incêndios e assaltos.  

4. **Relatórios e Análises**  
   - O sistema deve gerar relatórios sobre eficiência dos transportes, segurança pública e consumo de energia.  

## 5. Exemplo de Cenário de Uso
1. Um ônibus equipado com GPS é registrado no sistema como um `Veiculo` do tipo `Onibus`.  
2. Sensores de tráfego verificam congestionamentos e ajustam rotas automaticamente.  
3. Um cidadão faz uma solicitação de poda de árvores através do portal da cidade.  
4. A central de segurança recebe um alerta de comportamento suspeito captado por uma câmera.  

## 6. Conclusão
Este **sistema de cidade inteligente** demonstra um projeto amplo de **orientação a objetos**, cobrindo:
- **Encapsulamento:** Proteção de dados internos das classes.
- **Abstração:** Classes genéricas (`EntidadeCidade`) que representam elementos da cidade.
- **Herança:** Especialização de classes (`Veiculo` → `Onibus`).
- **Polimorfismo:** Uso de interfaces para manipulação de sensores diversos.

Com essa abordagem, o sistema pode ser facilmente expandido para novas funcionalidades, garantindo **escalabilidade e eficiência** para a gestão de cidades inteligentes.

#### Diagrama de Classes

~~~mermaid
classDiagram
    %% Classes Abstratas e Interfaces
    class EntidadeCidade {
        <<abstract>>
        +id: int
        +nome: String
    }

    class ISensor {
        <<interface>>
        +lerDados(): void
    }

    %% Classes Concretas
    class Veiculo {
        +placa: String
        +modelo: String
        +localizacao: String
        +atualizarLocalizacao(): void
    }

    class Onibus {
        +rota: String
        +capacidade: int
        +registrarPassageiros(): void
    }

    class Metro {
        +linha: String
        +numeroVagoes: int
        +registrarPassageiros(): void
    }

    class Ambulancia {
        +hospitalAssociado: String
        +emEmergencia: bool
        +atenderChamada(): void
    }

    class ViaturaPolicial {
        +delegaciaAssociada: String
        +emPatrulha: bool
        +responderOcorrencia(): void
    }

    class FuncionarioPublico {
        +cpf: String
        +cargo: String
        +executarTarefa(): void
    }

    class Policial {
        +patente: String
        +areaAtuacao: String
        +realizarPatrulha(): void
    }

    class Medico {
        +crm: String
        +especialidade: String
        +realizarConsulta(): void
    }

    class Motorista {
        +cnh: String
        +tipoVeiculo: String
        +conduzirVeiculo(): void
    }

    class SensorCamera {
        +resolucao: String
        +ativarReconhecimentoFacial(): void
    }

    class SensorPresenca {
        +sensibilidade: String
        +detectarMovimento(): void
    }

    class SensorQualidadeAr {
        +indiceQualidade: int
        +medirQualidadeAr(): void
    }

    class Cidadao {
        +cpf: String
        +endereco: String
        +solicitarServico(): void
    }

    class PortalCidadao {
        +registrarSolicitacao(): void
        +agendarAtendimento(): void
    }

    class Zoologico {
        +animais: List~Animal~
        +funcionarios: List~Funcionario~
        +adicionarAnimal(animal: Animal): void
        +adicionarFuncionario(funcionario: Funcionario): void
        +listarAnimais(): void
        +listarFuncionarios(): void
    }

    %% Relacionamentos
    EntidadeCidade <|-- Veiculo
    EntidadeCidade <|-- FuncionarioPublico
    EntidadeCidade <|-- Cidadao
    Veiculo <|-- Onibus
    Veiculo <|-- Metro
    Veiculo <|-- Ambulancia
    Veiculo <|-- ViaturaPolicial
    FuncionarioPublico <|-- Policial
    FuncionarioPublico <|-- Medico
    FuncionarioPublico <|-- Motorista
    ISensor <|.. SensorCamera
    ISensor <|.. SensorPresenca
    ISensor <|.. SensorQualidadeAr
    PortalCidadao o-- Cidadao
    Zoologico o-- Animal
    Zoologico o-- Funcionario
~~~