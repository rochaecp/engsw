# Mermaid

- Linguagem que permite criar diagramas por meio de código.
- Pode ser usado diretamente no GitHub, Notion e outras plataformas Markdown
- Renderizar Mermaid
    - [GitHub Markdown] (o GitHub já renderiza Mermaid nativamente)
    - https://mermaid.live/

#### Exemplo

~~~mermaid
classDiagram
    class Pessoa {
        +nome: String
        +idade: Int
        +falar(): void
    }
    class Aluno {
        +matricula: String
        +estudar(): void
    }
    Pessoa <|-- Aluno
~~~