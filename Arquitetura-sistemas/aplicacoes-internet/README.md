# Tipos de Arquiteturas

## Monolito
![monolito]()
| Pros                       | Contras                      |
| -------------------------- | ---------------------------- |
| Baixa Complexidade         | Stack única                  |
| Monitoramento Simplificado | Compartilhamento de recursos |
|                            | Acoplamento                  |
|                            | Mais complexo a escabilidade |

## Microsserviços

![microsserviço1]()

Serviços diretamente ligados uns aos outros

| Pros                   | Contras                       |
| ---------------------- | ----------------------------- |
| Stack dinâmica         | Acoplamento                   |
| Simples escalabilidade | Monitoramento mais complexo   |
|                        | Provisionamento mais complexo |

![microsserviço2]()

Serviços com um único ponto de comunicação (Message Broker)

| Pros                   | Contras                       |
| ---------------------- | ----------------------------- |
| Stack dinâmica         | Monitoramento mais complexo   |
| Simples escalabilidade | Provisionamento mais complexo |
| Desacoplamento         |                               |


![microsserviço3]()

Serviços ligado ao um pipeline

| Pros                   | Contras                                               |
| ---------------------- | ----------------------------------------------------- |
| Stack dinâmica         | Provisionamento mais complexo                         |
| Simples escalabilidade | Plataforma inteira depende do gerenciador de pipeline |
| Desacoplamento         |                                                       |
| Menor complexidade     |                                                       |


## Gerenciamento de erros e volume de acesso

Onde é mais complexo:
- Processos assíncronos (microsserviço 2)
- Pipeline

Solução:
- Dead letter queue
- filas de re-tentativas