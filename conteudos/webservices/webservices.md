# Webservices

## O que são Webservices?

- Um webservice é uma forma de comunicação entre sistemas pela web
- Webservices são componentes de software que permitem a comunicação entre sistemas distintos, possibilitando que aplicações troquem dados e realizem operações de forma interoperável, independentemente das linguagens de programação ou plataformas utilizadas.
- Webservices são interfaces que permitem a comunicação entre sistemas, independentemente de plataformas e linguagens.
- Um webservice é um tipo específico de API que permite a comunicação entre sistemas através de uma rede, geralmente usando protocolos como HTTP, SOAP, ou REST.
- Ele requer que a comunicação ocorra pela web e segue padrões definidos para troca de dados, como XML ou JSON.

## Propósito dos Webservices

- O objetivo principal dos webservices é permitir a integração de diferentes sistemas e aplicações, promovendo a interoperabilidade. 
- Eles facilitam o compartilhamento de dados e funcionalidades, mesmo quando os sistemas envolvidos utilizam tecnologias, linguagens ou arquiteturas distintas.
- Facilitar a integração e o compartilhamento de dados entre aplicações diversas.

## Exemplo: Consumindo um Webservice RESTful

- Vamos criar um exemplo básico de consumo de um webservice RESTful que retorna informações de usuários em formato JSON.
- Passo 1: Webservice de Teste
    - O webservice usado será https://jsonplaceholder.typicode.com/users, que retorna uma lista de usuários.

~~~vb
Imports System.Net.Http 'usada para fazer a requisição HTTP ao webservice.
Imports System.Threading.Tasks

Module WebServiceExample
    Sub Main()
        Dim resultado As String = ConsumirWebService().Result
        Console.WriteLine("Resultado do Webservice:")
        Console.WriteLine(resultado)
    End Sub

    Async Function ConsumirWebService() As Task(Of String)
        Dim url As String = "https://jsonplaceholder.typicode.com/users" ' URL do Webservice
        Using client As New HttpClient()
            Dim response As HttpResponseMessage = Await client.GetAsync(url) ' O método GetAsync realiza uma chamada ao serviço de forma assíncrona.

            If response.IsSuccessStatusCode Then
                ' Obtém o conteúdo da resposta como uma string
                Return Await response.Content.ReadAsStringAsync() ' A resposta é convertida para string com ReadAsStringAsync
            Else
                Return $"Erro: {response.StatusCode}"
            End If
        End Using
    End Function
End Module
~~~

## Diferenças entre webservices e API

- A diferença entre webservice e API está principalmente no escopo, propósito e nas tecnologias utilizadas. 
- Embora os termos sejam frequentemente usados de forma intercambiável, eles têm distinções importantes.
- **Webservice**
    - Tipo de API que opera exclusivamente pela web e segue protocolos como SOAP ou REST.
    - Tipo específico de API que opera via web.
    - Baseado em protocolos como SOAP ou REST, geralmente via HTTP.
    - Geralmente usa XML (SOAP) ou JSON (REST).
    - Depende de chamada de rede.
    - Requer uma conexão de rede (geralmente web).
    - Um webservice é um tipo específico de API que permite a comunicação entre sistemas através de uma rede, geralmente usando protocolos como HTTP, SOAP, ou REST.
    - Ele requer que a comunicação ocorra pela web e segue padrões definidos para troca de dados, como XML ou JSON.
- **API** (Application Programming Interface)
    - Conceito mais amplo que inclui webservices, mas também abrange integrações locais ou offline.
    - Interface para integração de software, não limitada à web.
    - Pode usar HTTP/HTTPS, mas também outros, como IPC, TCP, etc.
    - Pode usar JSON, XML, texto simples, binário, entre outros.
    - Pode ser local ou via rede.
    - Pode funcionar localmente ou remotamente.
    - SDKs de bibliotecas (ex.: API gráfica, API de sistema operacional).
    - Uma API é um conjunto de regras e ferramentas que define como sistemas ou componentes de software podem se comunicar.
    - APIs não precisam operar exclusivamente pela web. Elas podem ser locais (no mesmo sistema) ou baseadas em redes internas, além de suportar diversas tecnologias.
    - Exemplos
        - A API de um sistema operacional, como a API do Windows, que permite acessar funcionalidades nativas (ex.: abrir arquivos).
            - Uma API de sistema operacional não é um webservice porque não usa a web para comunicação.
        - Uma API local de uma biblioteca gráfica, usada por um programa para renderizar imagens na tela.
- Atualmente, APIs RESTful são frequentemente chamadas de webservices devido à sua popularidade na web, mas nem toda API é um webservice.
- Webservices tradicionais (SOAP) têm aplicações específicas em sistemas legados e grandes corporações.
- APIs RESTful são webservices.
    - Um webservice é uma forma de comunicação entre sistemas pela web
    - Uma API RESTful é um tipo de webservice que segue os princípios REST (Representational State Transfer), utilizando protocolos da web, como HTTP, para realizar essa comunicação.
- Por que nem toda API é um Webservice?
    - Nem todas as APIs operam na web.
    - APIs podem ser locais (ex.: bibliotecas ou APIs do sistema operacional) e não dependem de protocolos de rede.
    - Já webservices, por definição, dependem de uma rede (geralmente a web) para funcionar.

## Webservices SOAP vs. APIs RESTful

- Webservices tradicionais, como os baseados em SOAP (Simple Object Access Protocol), eram os mais usados no passado.
- REST surgiu como uma alternativa mais leve, flexível e escalável.
- SOAP (Webservice)
    Formato de Dados: XML 
    Complexidade: Mais verboso 
    Estrutura: Baseado em operações fixas (WSDL) 
- RESTful API (Webservice)
    - Formato de dados: JSON, XML, Texto simples
    - Complexidade: Mais leve e simples
    - Estrutura: Baseado em recursos (URI e HTTP)

## WSDL (Web Services Description Language)

- WSDL é um formato padrão baseado em XML usado para descrever webservices SOAP. 
- Ele define como um serviço pode ser chamado, quais operações ele oferece, e quais dados espera e retorna.
- WSDL é essencial para webservices SOAP, pois descreve como eles funcionam.
- Ele detalha operações, mensagens e o local do serviço, permitindo integração entre sistemas.
- Principais Elementos do WSDL
    - <types>:
        - Define os tipos de dados usados no serviço (usando XML Schema).
    - <message>:
        - Especifica as mensagens de entrada e saída para cada operação.
    - <portType>:
        - Lista as operações disponíveis e suas mensagens associadas.
    - <binding>:
        - Detalha como as operações serão transmitidas (protocolo e formato).
    - <service>:
        - Especifica o endereço (URL) onde o serviço está disponível.
- Uso
    - Permite que sistemas entendam como interagir com um webservice SOAP, independentemente da linguagem de programação ou plataforma.
    - Serve como um "contrato" entre o cliente e o servidor. 
- Exemplo Simplificado
    ~~~xml
    <definitions>
    <types>...</types>
    <message name="GetDataRequest">...</message>
    <message name="GetDataResponse">...</message>
    <portType name="ServicePort">
        <operation name="GetData">
        <input message="GetDataRequest"/>
        <output message="GetDataResponse"/>
        </operation>
    </portType>
    <binding name="ServiceBinding" type="ServicePort">...</binding>
    <service name="MyService">
        <port name="MyPort" binding="ServiceBinding">
        <address location="http://example.com/service"/>
        </port>
    </service>
    </definitions>
    ~~~
