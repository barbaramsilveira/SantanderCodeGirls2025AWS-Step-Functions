# AWS Step Functions

O <strong>AWS Step Functions</strong> é um serviço da AWS que permite criar fluxos de trabalho, automatizar processos, orquestrar microsserviços e construir pipelines de dados e de aprendizado de máquina.
Ele é baseado em máquinas de estado e tarefas, permitindo coordenar diferentes componentes de forma visual, confiável e escalável.

A ferramenta oferece dois tipos de fluxos de trabalho:

## 1. Padrão (Standard):

- Permite execuções de longa duração — até 1 ano.

- Cada execução de fluxo é única e cada etapa é executada exatamente uma vez.

- Ideal para processos críticos e de longa duração, como integrações entre sistemas, orquestração de microsserviços e pipelines complexos.

## 2. Expresso (Express):

- Voltado para altas taxas de eventos e execuções de curta duração — até 5 minutos.

- Segue o modelo de execução at least once (pelo menos uma vez).

- As etapas podem ser reexecutadas automaticamente em caso de falhas.

- Ideal para eventos de streaming, processamento em tempo real e ingestão de dados de IoT.

 ****

| Característica                    | Fluxos de trabalho **Padrão (Standard)**                               | Fluxos de trabalho **Expressos (Express)**                                               |
|------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| **Taxa de execução**              | 2 mil por segundo                                                      | 100 mil por segundo                                                                       |
| **Taxa de transição de estado**   | 4 mil por segundo                                                      | Quase ilimitada                                                                          |
| **Cobrança**                      | Por transição de estado                                               | Conforme o número e a duração das execuções                                              |
| **Histórico de execução**        | Exibição do histórico de execução e depuração visual                   | Exibição do histórico de execução e depuração visual com base no nível de log             |
| **Armazenamento de histórico**   | Histórico disponível no Step Functions                                | Histórico enviado para Amazon CloudWatch                                                |
| **Integrações**                  | Suporte a integrações com todos os serviços                           | Suporte a integrações otimizadas com alguns serviços                                    |
| **Padrão de resposta**           | Suporte ao padrão de resposta à solicitação para todos os serviços    | Suporte ao padrão de resposta à solicitação para todos os serviços                      |
| **Run a Job / Wait for Callback**| Suporte em serviços específicos                                       | Suporte em serviços específicos                                                          |


[Documentação Oficial da AWS Step Functions](https://docs.aws.amazon.com/pt_br/step-functions/latest/dg/welcome.html)
