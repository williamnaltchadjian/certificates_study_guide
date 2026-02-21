# ☁️ AWS Documentation: Amazon SageMaker

Este documento apresenta um resumo organizado por categoria do Amazon SageMaker, a plataforma ML da AWS.

---

## 📊 Visão Geral por Fase do Ciclo de ML   


| Fase                            | Serviço                                 | Para que serve                                          | Perfil Ideal             |
| ------------------------------- | --------------------------------------- | ------------------------------------------------------- | ------------------------ |
| **No-Code**                     | Amazon SageMaker Canvas                 | Criar modelos sem programar                             | Analistas de negócio     |
| **Ambiente de Desenvolvimento** | Amazon SageMaker Studio                 | IDE completa para ML (notebooks, treino, deploy, debug) | Cientistas de dados      |
| **Modelos Prontos**             | Amazon SageMaker JumpStart              | Modelos pré-treinados e foundation models               | Projetos rápidos / GenAI |
| **Exploração GenAI**            | Amazon SageMaker Playgrounds            | Testar prompts e inferência                             | Experimentação           |
| **Rotulagem de Dados**          | Amazon SageMaker Ground Truth           | Criar labels para treino                                | Times de dados           |
| **Preparação de Dados**         | Amazon SageMaker Data Wrangler          | Explorar, limpar e transformar dados                    | Engenharia de dados      |
| **Gerenciamento de Features**   | Amazon SageMaker Feature Store          | Armazenar e reutilizar features                         | ML em produção           |
| **AutoML**                      | Amazon SageMaker Autopilot              | Automatiza criação e otimização de modelos              | Desenvolvimento rápido   |
| **Otimização**                  | Amazon SageMaker Automatic Model Tuning | Busca melhores hiperparâmetros                          | Melhorar performance     |
| **Rastreamento**                | Amazon SageMaker Experiments            | Versionar treinos e métricas                            | Comparação de modelos    |
| **Pipelines (MLOps)**           | Amazon SageMaker Pipelines              | Automatizar fluxo de ML (CI/CD)                         | Produção corporativa     |
| **Automação de Deploy**         | Amazon SageMaker Agents                 | Gerenciar endpoints e infraestrutura                    | Operações                |
| **Monitoramento**               | Amazon SageMaker Model Monitor          | Detectar drift e queda de performance                   | Produção                 |
| **Explicabilidade & Bias**      | Amazon SageMaker Clarify                | Detectar viés e explicar previsões                      | Governança               |
| **Documentação do Modelo**      | Amazon SageMaker Model Cards            | Registrar métricas, riscos e uso                        | Compliance               |
| **Painel de Governança**        | Amazon SageMaker Model Dashboard        | Visualizar e monitorar múltiplos modelos                | Gestão                   |
| **Permissões**                  | Amazon SageMaker Role Manager           | Gerenciar acessos (IAM simplificado)                    | Segurança                |



---

## 🎯 Visão Estratégica para Prova

| Se a pergunta falar sobre… | Resposta provável |
| :--- | :--- |
| Usuário sem código | Canvas |
| IDE completa | Studio |
| Modelos prontos / GenAI | JumpStart |
| Rotulagem | Ground Truth |
| Limpeza de dados | Data Wrangler |
| Reuso de variáveis | Feature Store |
| AutoML | Autopilot |
| Melhorar hiperparâmetros | Automatic Model Tuning |
| Versionamento de treino | Experiments |
| CI/CD de ML | Pipelines |
| Detectar viés | Clarify |
| Detectar drift | Model Monitor |
| Documentação de risco | Model Cards |

---

## 🏗️ Arquitetura do Amazon SageMaker

## 🧑‍💻 Desenvolvimento

- **Studio** – IDE completa de Machine Learning  
- **Canvas** – Plataforma No-Code para criação de modelos  
- **JumpStart** – Modelos prontos e Foundation Models  
- **Playgrounds** – Testes de prompts e inferência  

---

## 📊 Preparação de Dados

- **Data Wrangler** – Limpeza e transformação de dados  
- **Ground Truth** – Rotulagem (labeling) de dados  
- **Feature Store** – Repositório central de features  

---

## ⚙️ Treinamento & Otimização

- **Autopilot** – AutoML (treinamento automatizado)  
- **Automatic Model Tuning** – Otimização de hiperparâmetros  
- **Experiments** – Rastreamento de versões e métricas  

---

## 🚀 Deploy & MLOps

- **Pipelines** – CI/CD para Machine Learning  
- **Agents** – Automação de endpoints  
- **Endpoints** – Inferência em produção  

---

## 📈 Monitoramento

- **Model Monitor** – Detecta data drift e model drift  

---

## ⚖️ Governança & Responsible AI

- **Clarify** – Detecção de viés e explicabilidade  
- **Model Cards** – Documentação estruturada do modelo  
- **Model Dashboard** – Visão centralizada de modelos  
- **Role Manager** – Gerenciamento de permissões (IAM)  