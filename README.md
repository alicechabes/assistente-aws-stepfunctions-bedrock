# 🤖 Assistente Virtual com AWS Step Functions e Amazon Bedrock

Projeto desenvolvido para o bootcamp da **DIO (Digital Innovation One)** com foco em orquestração de serviços serverless e integração com Inteligência Artificial Generativa na **AWS**.

---

## 📌 Visão Geral do Projeto

Este projeto demonstra como criar um fluxo de trabalho orquestrado (workflow) para um **assistente virtual inteligente** capaz de processar requisições, interagir com múltiplos modelos de linguagem (LLMs) via **Amazon Bedrock** e responder com baixa latência utilizando arquitetura **Serverless**.

---

## 🛠️ Tecnologias Utilizadas

- **AWS Step Functions:** Orquestração de tarefas e controle de estados do fluxo da aplicação.
- **Amazon Bedrock:** Acesso a modelos de IA generativa de ponta (como Claude, Titan, Llama).
- **AWS Lambda:** Execução de código serverless para pré e pós-processamento de dados.
- **Amazon S3 / DynamoDB:** Armazenamento de logs, histórico de conversas ou arquivos temporários.

---

## 🚀 Arquitetura e Fluxo de Funcionamento

```text
[ Entrada do Usuário ] 
          │
          ▼
┌──────────────────┐
│ AWS Step Function│ ◄─── (Orquestra os estados da execução)
└─────────┬────────┘
          │
          ├───► [ Validação da Entrada / Pre-processing ]
          │
          ├───► [ Chamada ao Amazon Bedrock (LLM) ]
          │
          └───► [ Tratamento da Resposta / Output ]
