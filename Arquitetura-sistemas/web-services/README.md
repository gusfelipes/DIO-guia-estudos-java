# Serviços Web
- Serviços web ou web services são soluções para aplicações se comuniquem independentes de linguagem, softwares e hardwares diferentes
- Inicialmente foram criados para troca de mensagem em XML (Extensible Markup Language) rodando em protocolo HTTP sendo identificado por URI (Uniform Resource Identifier)
- Sendo assim, pode-se dizer que web services são API's que se comunicam por meio de redes sobre o protocolo HTTP

![web service]()

### XML x JSON
```xml 
<endereco>
    <cep>999999</cep>
    <bairro>centro</bairro>
    <cidade>Florianópolis</cidade>
</endereco>
``` 

```json
"endereco":{
    "cep": "999999",
    "bairro": "centro",
    "cidade": "Florianópolis"
}
```
### Vantagens
- linguagem comum
- Integração
- Reutilização de implementação
- Segurança
- Custos

## SOAP
- Simple Object Access Protocol
- protocolo baseado em XML para acessar web services principalmente por HTTP
- é uma definição de como serviços web se comunicam
- desenvolvido para facilitar integrações
- vantagens iguais ao web services
- independentes da plataforma e software
- Pode rodar através de outros protocolos além do HTTP


### Estrutura SOAP
![estrutura soap message]()
- SOAP Envelope: primeiro elemento do documento e é usado para encapsular toda a mensagem
- SOAP Header: possui as informações de atributos e metadados da requisição
- SOAP Body: contém os detalhes da mensagem

![soap message]()


## WSDL e XSD
- Web Service Description Language (WSDL)
  - Usado para descrever Web Services, funciona como um contrato do serviço
  - Um documento XML, com a descrição do serviço, espeficicações de acesso, operações e métodos.
- XML Schema Definition (XSD)
  - Um esquema no formato XML usado para definir a estrutura de dados que será validada no XML
  - Funciona como uma documentação de como de ser montado o SOAP Message enviado pelo Web Service
  
  [SoapClient](http://www.soapclient.com)

  [Exemplo](http://www.soapclient.com/xml/soapresponder.wsdl)

Para testar SOAP
  [SOAPui](https://www.soapui.org/)

## REST, API e JSON
- Representational State Transfer (REST)
  - Estilo de arquitetura de software define a implementação de um serviço web
  - Trabalha com formato XML, JSON e outros
- Vantagens:
  - Permite integrações entre aplicações e também entre cliente e servidor em páginas web e aplicações
  - Utiliza dos métodos HTTP para definir a operação que está sendo efetuada
  - Arquitetura de fácil compreensão

Quando uma aplicação web disponibiliza um conjunto de rotimas e padrões através de serviços web pode-se chamar esse conjunto de API

- Application Programming Interface (API)
- Conjuntos de rotinas documentados e disponibilizados por uma aplicação para que outras aplicações possam consumir suas funcionalidades
- Ex: Facebook, twitter, telegram, github

Principais métodos HTTP
- GET: Solicita a representação de um recurso
- POST: Solicita a criação de um recurso
- DELETE: Solicita a exclusão de um recurso
- PUT: Solicita a atualização de um recurso

- Jascript Object Notation (JSON)
  - Formatação Leve
  - Estrutura de chave-valor e de lista ordenadas
  - Formato muito popular

### Codigo de Estado
- Status Code
- Usado pelo servidor para avisar o cliente sobre o estado da operação solicitada
- https://httpstatuses.com/
- Programas para usar API
  - [Postman](https://www.postman.com/)
  - [Imsonia](https://insomnia.rest/)