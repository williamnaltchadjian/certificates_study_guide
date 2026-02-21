# ☁️ AWS Documentation: Amazon Bedrock

Este repositório centraliza o conhecimento técnico sobre o Amazon Bedrock e conceitos de IA Generativa na AWS.

---

## 🧠 O que é IA Generativa (GenAI)?

**Generative AI (IA Generativa)** é um tipo de Inteligência Artificial capaz de criar conteúdo novo (texto, imagens, código, áudio, vídeo) a partir de padrões aprendidos em grandes volumes de dados.

Ela utiliza principalmente **Large Language Models (LLMs)** e modelos baseados em redes neurais profundas.

### Exemplos de uso:
* Chatbots inteligentes
* Geração de código
* Resumo automático de documentos
* Criação de imagens
* Assistentes virtuais corporativos

---

## ☁️ Amazon Bedrock – Overview

O Amazon Bedrock é um serviço gerenciado da AWS que permite construir e escalar aplicações de IA Generativa usando **Foundation Models (FMs)** de diversos provedores, sem precisar gerenciar infraestrutura.

### Principais benefícios:
* **Serverless** – Sem gerenciamento de infraestrutura
* **Integração com serviços AWS** – Conexão nativa com outros serviços AWS
* **Segurança corporativa** – Proteção e governança de dados
* **Suporte a múltiplos modelos** – Diversos provedores em um único serviço
* **Customização** – Fine-tuning e RAG

---

## 🤖 Amazon Bedrock – Foundation Model (FM)

**Foundation Models (FMs)** são modelos de IA pré-treinados em larga escala que podem ser adaptados para diferentes tarefas.

### Provedores disponíveis no Bedrock:
| Provedor | Especialidade |
| :--- | :--- |
| **Anthropic** | LLMs de alta performance (Claude) |
| **AI21** | Modelos de linguagem avançados |
| **Stability AI** | Geração de imagens |
| **Amazon (Titan)** | Modelos proprietários AWS |
| **Cohere** | LLMs empresariais |

### Tipos de geração:
* Texto
* Código
* Imagens
* Embeddings

---

## ⚙️ Amazon Bedrock – Fine-Tuning

**Fine-tuning** é o processo de ajustar um modelo base usando dados específicos da empresa para melhorar sua performance em um domínio particular.

### Benefícios:
* Respostas mais especializadas
* Melhor aderência ao contexto de negócio
* Redução de erros genéricos

> [!NOTE]
> No Bedrock, o fine-tuning é gerenciado e simplificado, reduzindo a complexidade operacional.

---

## 📊 Amazon Bedrock – FM Evaluation

O Amazon Bedrock – FM Evaluation (Foundation Model Evaluation) é uma funcionalidade do Amazon Bedrock projetada para ajudar empresas a avaliar, comparar e selecionar os melhores modelos de base (FMs) para suas aplicações de IA generativa



| Métrica | Descrição |
| :--- | :--- |
| **Precisão** | Qualidade das respostas |
| **Relevância** | Adequação ao contexto |
| **Toxicidade** | Segurança do conteúdo |
| **Custo** | Investimento por requisição |
| **Latência** | Tempo de resposta |

O Bedrock oferece ferramentas para testes comparativos antes de colocar em produção.

---

## 📚 Amazon Bedrock – RAG & Knowledge Base

**RAG (Retrieval-Augmented Generation)** combina:
1. Busca em base de dados privada
2. Geração de resposta pelo modelo

### Fluxo:
```
Usuário faz pergunta → Sistema busca documentos relevantes → Modelo gera resposta com base nesses documentos
```

### Knowledge Bases do Bedrock:
* Conectam dados corporativos (S3, bancos, etc.)
* Criam embeddings automaticamente
* Permitem consultas contextualizadas

> [!IMPORTANT]
> **Benefício:** Reduz alucinação e aumenta precisão das respostas.

---

## 🔑 Mais Conceitos de GenAI

| Conceito | Descrição |
| :--- | :--- |
| **Prompt Engineering** | Técnica de estruturar perguntas para melhorar respostas |
| **Embeddings** | Representação vetorial de texto para busca semântica |
| **Temperature** | Controla criatividade do modelo |
| **Token** | Unidade de texto processada pelo modelo |
| **Hallucination** | Quando o modelo inventa informações |

---

## 🛡️ Amazon Bedrock – Guardrails

**Guardrails** são mecanismos de controle para:
* Bloquear conteúdo impróprio
* Filtrar informações sensíveis
* Aplicar políticas de compliance
* Controlar formato de resposta

> [!IMPORTANT]
> São essenciais para uso corporativo e conformidade regulatória.

---

## 🤖 Amazon Bedrock – Agents

**Agents for Bedrock** permitem criar agentes inteligentes que:
* Entendem intenção do usuário
* Quebram tarefas complexas em etapas
* Chamam APIs automaticamente
* Executam workflows

### Exemplo:
> Usuário: *"Verifique meu saldo e transfira R$ 5.000"*  
> O agente:
> 1. Consulta saldo
> 2. Valida regras de negócio
> 3. Executa transação

> [!TIP]
> Ideal para automação corporativa.

---

## 📈 Amazon Bedrock – CloudWatch Integration

O Bedrock integra com o **Amazon CloudWatch** para:
* Monitorar uso
* Analisar latência
* Acompanhar erros
* Medir consumo de tokens
* Criar alarmes

> [!NOTE]
> Permite governança e observabilidade em produção.

---

## 💰 Amazon Bedrock – Pricing

Modelo de cobrança baseado em:

| Fator | Descrição |
| :--- | :--- |
| **Tokens de input** | Cobrado por requisição enviada |
| **Tokens de output** | Cobrado por resposta gerada |
| **Tipo de modelo** | Preços variam por provedor |
| **Fine-tuning** | Custo adicional quando aplicável |
| **Embeddings** | Cobrado por vetor gerado |
| **Knowledge Base** | Custos de armazenamento |

> [!NOTE]
> Não há custo de infraestrutura, pois é serverless.

---

## 🐾 Amazon Nova

**Amazon Nova** é a família de modelos proprietários da AWS para IA Generativa.

### Inclui modelos otimizados para:
* Texto
* Multimodal (texto + imagem)
* Alto desempenho com menor custo

### Foco:
* Performance empresarial
* Integração nativa com AWS
* Segurança e escalabilidade
