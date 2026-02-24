# 📋 Referência Rápida — Serviços AWS

Listagem de todos os serviços AWS mencionados neste guia de estudos, organizados por categoria.

> [!NOTE]
> Este arquivo é gerado a partir da leitura consolidada de todos os domínios do guia de estudos (Domínio 1 ao 5) e dos arquivos de serviços.

---

## 🧠 Amazon Bedrock

| Serviço / Recurso | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon Bedrock** | Serviço gerenciado e serverless para construir aplicações de IA Generativa com Foundation Models | D2, D3 |
| **Amazon Bedrock — Fine-Tuning** | Ajuste de modelos base com dados específicos da empresa | D3 |
| **Amazon Bedrock — FM Evaluation** | Avaliação e comparação de Foundation Models antes da produção | D3 |
| **Amazon Bedrock — Knowledge Bases** | Base de dados corporativa integrada ao Bedrock para RAG | D3 |
| **Amazon Bedrock — Guardrails** | Controles de segurança e compliance para respostas do modelo | D3, D4 |
| **Amazon Bedrock — Agents** | Agentes inteligentes para automação de tarefas multi-etapas | D3 |
| **Amazon Nova** | Família de modelos proprietários da AWS (texto e multimodal) | D3 |

---

## 🔬 Amazon SageMaker

### Desenvolvimento

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon SageMaker Studio** | IDE completa para Machine Learning (notebooks, treino, deploy, debug) | D1 |
| **Amazon SageMaker Canvas** | Plataforma no-code para criação de modelos ML | D1 |
| **Amazon SageMaker JumpStart** | Modelos pré-treinados e Foundation Models prontos para uso | D1 |
| **Amazon SageMaker Playgrounds** | Ambiente para testar prompts e inferência | D1 |

### Preparação de Dados

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon SageMaker Ground Truth** | Rotulagem (labeling) de dados para treinamento | D1 |
| **Amazon SageMaker Data Wrangler** | Exploração, limpeza e transformação de dados | D1 |
| **Amazon SageMaker Feature Store** | Repositório centralizado para armazenar e reutilizar features | D1 |

### Treinamento & Otimização

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon SageMaker Autopilot** | AutoML — automatiza criação e otimização de modelos | D1 |
| **Amazon SageMaker Automatic Model Tuning** | Busca automática dos melhores hiperparâmetros | D1 |
| **Amazon SageMaker Experiments** | Versionamento de treinos e rastreamento de métricas | D1 |

### Deploy & MLOps

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon SageMaker Pipelines** | CI/CD para Machine Learning (automação do fluxo de ML) | D1, D4 |
| **Amazon SageMaker Endpoints** | Inferência em produção (Real-Time, Serverless, Async, Batch) | D1 |
| **Amazon SageMaker Edge Manager** | Gerenciamento de modelos em dispositivos edge (câmeras, robôs) | D1 |
| **Amazon SageMaker Neo** | Otimização de modelos para diferentes hardwares | D1 |

### Governança & Responsible AI

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon SageMaker Model Monitor** | Detecção de data drift e model drift em produção | D1, D4 |
| **Amazon SageMaker Clarify** | Detecção de viés e explicabilidade das previsões | D1, D4, D5 |
| **Amazon SageMaker Model Cards** | Documentação estruturada de modelo (métricas, riscos, uso) | D1, D4 |
| **Amazon SageMaker Model Dashboard** | Painel centralizado para visualizar e monitorar vários modelos | D1 |
| **Amazon SageMaker Role Manager** | Gerenciamento de permissões IAM simplificado | D1 |

---

## 🟣 Amazon Q

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon Q Business** | Assistente de IA corporativa com dados internos via RAG | Serviços |
| **Amazon Q Apps** | Criação de aplicações GenAI sem código (no-code) | Serviços |
| **Amazon Q Developer** | Assistente de IA para desenvolvedores integrado à IDE | Serviços |
| **Amazon Q for AWS Services** | Assistente inteligente dentro do Console AWS | Serviços |
| **PartyRock** | Plataforma experimental para criar e testar apps GenAI | Serviços |

---

## 🗄️ Bancos de Dados e Armazenamento Vetorial

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon OpenSearch Service** | Busca vetorial e semântica para RAG e embeddings | D3 |
| **Amazon Aurora** | Banco relacional gerenciado com suporte a vetores | D3 |
| **Amazon Neptune** | Banco de dados de grafos | D3 |
| **Amazon DocumentDB** | Banco de dados de documentos compatível com MongoDB | D3 |
| **Amazon RDS for PostgreSQL** | PostgreSQL gerenciado com extensão pgvector para vetores | D3 |

---

## 🔐 Segurança, Identidade e Conformidade

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **AWS IAM** | Controle de identidade e acesso — quem acessa o quê na AWS | D4, D5 |
| **AWS KMS** | Gerenciamento de chaves de criptografia de dados | D5 |
| **Amazon Macie** | Descoberta de dados sensíveis (PII) no S3 usando ML | D5 |
| **AWS Config** | Monitoramento de configurações e conformidade de recursos | D5 |
| **Amazon Inspector** | Scanner automático de vulnerabilidades em instâncias e containers | Serviços |
| **AWS CloudTrail** | Log de auditoria de todas as chamadas de API da conta | D5 |
| **AWS Artifact** | Portal de relatórios de conformidade (ISO, PCI, SOC, HIPAA) | D5 |
| **AWS Audit Manager** | Gestão de riscos e auditoria contínua | Serviços |
| **AWS Trusted Advisor** | Consultor para reduzir custos e aumentar segurança e performance | Serviços |
| **Amazon GuardDuty** | Detecção de ameaças e comportamentos maliciosos | D5 |

---

## 🤝 IA Responsável e Revisão Humana

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon Augmented AI (A2I)** | Revisão humana de previsões de ML (human-in-the-loop) | D5 |

---

## 💾 Armazenamento

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon S3** | Armazenamento de objetos escalável, seguro e durável | D5 |
| **Amazon S3 Glacier** | Arquivo de longo prazo com custo baixo | Serviços |
| **Amazon S3 Intelligent-Tiering** | Movimentação automática entre classes por padrão de acesso | Serviços |

---

## ⚡ Computação

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon EC2** | Servidores virtuais na nuvem com controle total do SO | Serviços |
| **AWS Lambda** | Execução serverless de código em resposta a eventos | Serviços |

---

## 📊 Monitoramento e Observabilidade

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **Amazon CloudWatch** | Monitoramento de uso, latência, erros e criação de alarmes | D5 |

---

## 🌐 Networking e Conectividade

| Serviço | Descrição Resumida | Domínio |
| :--- | :--- | :--- |
| **VPC Endpoint** | Conecta rede privada aos serviços AWS de forma isolada | Serviços |
| **AWS PrivateLink** | Conectividade privada entre VPCs e redes on-premises | Serviços |
| **S3 Gateway Endpoint** | Acesso gratuito ao S3 para redes privadas sem NAT Gateway | Serviços |

---

## 📊 Contagem de Serviços por Categoria

| Categoria | Qtd. de Serviços |
| :--- | :---: |
| Amazon Bedrock | 7 |
| Amazon SageMaker | 17 |
| Amazon Q | 5 |
| Bancos de Dados e Vetorial | 5 |
| Segurança e Conformidade | 10 |
| IA Responsável e Revisão Humana | 1 |
| Armazenamento | 3 |
| Computação | 2 |
| Monitoramento | 1 |
| Networking | 3 |
| **Total** | **54** |

---

> [!TIP]
> **Legenda da coluna Domínio:**
> - **D1** = Domínio 1 — Fundamentos de IA e ML
> - **D2** = Domínio 2 — Fundamentos de IA Generativa
> - **D3** = Domínio 3 — Aplicações de Modelos de Base
> - **D4** = Domínio 4 — Diretrizes de IA Responsável
> - **D5** = Domínio 5 — Segurança, Conformidade e Governança
> - **Serviços** = Encontrado nos arquivos da pasta Serviços
