## AI, ML, Deep Learning e GenAI

| Conceito | Descrição |
| :--- | :--- |
| **Artificial Intelligence (AI)** | Campo amplo que cria sistemas capazes de simular inteligência humana |
| **Machine Learning (ML)** | Subárea da AI onde modelos aprendem padrões a partir de dados |
| **Deep Learning (DL)** | Subárea do ML baseada em redes neurais profundas |
| **Generative AI (GenAI)** | Modelos capazes de gerar conteúdo novo (texto, imagem, código) |


## ML Terms You May Encounter

Termos comuns na prova:

| Termo | Definição | Exemplo Prático |
| :--- | :--- | :--- |
| **Dataset** | Conjunto completo de dados usados no projeto de ML | Base com 10.000 registros de clientes |
| **Feature** | Variável de entrada usada para fazer a previsão | Idade, renda, histórico de compras |
| **Label** | Resposta correta que o modelo deve aprender | "Fraude" ou "Não Fraude" |
| **Training** | Fase em que o modelo aprende padrões com os dados | Modelo aprende com 70% dos dados disponíveis |
| **Validation** | Dados usados durante o treino para ajustar o modelo | Ajustar hiperparâmetros com 15% dos dados |
| **Test Set** | Dados usados para avaliar o desempenho final | Avaliar modelo com 15% de dados nunca vistos |
| **Model** | Algoritmo treinado que faz previsões | Modelo que prevê churn de clientes |
| **Inference** | Uso do modelo treinado para prever novos dados | Prever se um novo cliente vai cancelar |
| **Overfitting** | Modelo aprende demais os dados de treino e não generaliza | 99% no treino, 70% no teste |
| **Underfitting** | Modelo simples demais, não aprende bem | Baixa acurácia em treino e teste |




## Métricas de Avaliação de Modelos

### Classificação

| Métrica | Pergunta que ela responde | Quando priorizar |
| :--- | :--- | :--- |
| **Accuracy** | Quantas previsões estão corretas no total? | Classes balanceadas |
| **Precision** | Quando o modelo diz que é positivo, ele acerta? | Falso positivo é grave |
| **Recall** | O modelo conseguiu encontrar todos os positivos reais? | Falso negativo é grave |
| **F1 Score** | Qual o equilíbrio entre Precision e Recall? | Dados desbalanceados |
| **AUC-ROC** | O modelo consegue separar bem as classes? | Comparar modelos |

!!! tip
    **Regra de Ouro para a Prova:**
    - Fraude ou Diagnóstico médico → **Recall** (não pode deixar positivo passar)
    - Bloquear cliente legítimo → **Precision** (não pode ter falso positivo)
    - Dados desbalanceados → **F1 Score**
    - Comparar modelos → **AUC-ROC**

---

### Regressão

| Métrica | O que mede | Quando usar |
| :--- | :--- | :--- |
| **MAE** | Erro médio absoluto | Quando quer erro claro e interpretável |
| **MSE** | Erro médio ao quadrado | Quando erros grandes são muito críticos |

!!! tip
    - Quer **penalizar erro grande**? → **MSE**
    - Quer entender o **erro médio simples**? → **MAE**

---

### Métricas — GenAI / LLM

| Métrica | Para que serve | Quando aparece |
| :--- | :--- | :--- |
| **BLEU** | Avaliar qualidade de tradução | Tradução automática |
| **ROUGE** | Avaliar qualidade de resumo | Sumarização de textos |
| **BERTScore** | Avaliar similaridade semântica | Respostas de chatbot |
| **Perplexidade** | Qualidade de previsão da próxima palavra | Avaliar qualidade de LLM |


### Resumo Estratégico para Prova

| Tipo | Métricas |
| :--- | :--- |
| **Classificação** | Accuracy, Precision, Recall, F1, AUC |
| **Regressão** | MAE, MSE |
| **LLMs** | Perplexidade |
| **GenAI (texto)** | BLEU, ROUGE, BERTScore |

---

## Tipos de Aprendizado em Machine Learning

| Tipo de Aprendizado | Usa Rótulo? | Objetivo Principal | Principais Técnicas / Modelos | Casos de Uso Comuns |
| :--- | :--- | :--- | :--- | :--- |
| Supervisionado | ✅ Sim | Prever resultado conhecido | Regressão Linear, Regressão Logística, Árvore de Decisão, Random Forest, SVM, Redes Neurais | Previsão de churn, detecção de fraude, previsão de preço |
| Não Supervisionado | ❌ Não | Descobrir padrões ocultos | K-Means, DBSCAN, PCA, Hierarchical Clustering | Segmentação de clientes, análise exploratória |
| Autossupervisionado | ⚠️ Rótulo gerado automaticamente | Aprender representações dos dados | Modelos Transformer, LLMs | Previsão da próxima palavra, embeddings |
| Aprendizado por Reforço (RL) | ❌ Não usa rótulo tradicional | Maximizar recompensa | Q-Learning, Policy Gradient, Deep RL | Jogos, robótica, otimização de decisões |
| RLHF (Reinforcement Learning from Human Feedback) | ⚠️ Usa feedback humano como recompensa | Alinhar modelo às preferências humanas | PPO + Modelo de Recompensa | Ajuste fino de LLMs, alinhamento de IA generativa |

### 🎯 Lembra Rápido para Prova (com Modelos)

| Se a questão falar sobre… | Tipo de Aprendizado | Principais Técnicas / Modelos |
| :--- | :--- | :--- |
| 🔮 Prever algo (valor ou categoria) | Supervisionado | Regressão Linear, Regressão Logística, Árvore de Decisão, Random Forest, SVM, Redes Neurais |
| 🔍 Agrupar ou descobrir padrões | Não Supervisionado | K-Means, DBSCAN, Clustering Hierárquico |
| 📉 Reduzir número de variáveis | Não Supervisionado | PCA |
| 📚 Prever próxima palavra / criar embeddings | Autossupervisionado | Transformers, LLMs |
| 🎮 Agente + ambiente + recompensa | Reforço (RL) | Q-Learning, Policy Gradient, Deep RL |
| 👨‍🏫 Modelo ajustado com feedback humano | RLHF | PPO + Modelo de Recompensa |

### 🧠 Dica Estratégica

Se aparecer na questão:

- "Classificar churn" → Árvore de Decisão / SVM
- "Segmentar clientes" → K-Means
- "Reduzir dimensionalidade" → PCA
- "LLM prevê próxima palavra" → Autossupervisionado
- "Ajuste com preferências humanas" → RLHF

---


## Underfitting, Overfitting, Bias e Variância

| Conceito | Alto Bias? | Alta Variância? | Erro no Treino | Erro no Teste | Descrição | Como Melhorar |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Underfitting** | Sim | Não | Alto | Alto | Modelo simples demais, não aprende os padrões | Aumentar complexidade, adicionar features, treinar mais |
| **Overfitting** | Não | Sim | Baixo | Alto | Modelo complexo demais, aprende até o ruído | Regularização, mais dados, simplificar modelo |
| **Bias** | Sim | Não | Alto | Alto | Erro por simplificação excessiva | Modelo mais complexo |
| **Variância** | Não | Sim | Baixo | Alto | Sensível demais aos dados de treino | Regularização, mais dados |



### Leitura rápida para prova

| Situação | Problema | Solução |
| :--- | :--- | :--- |
| Erro alto em treino e teste | Underfitting (Alto Bias) | Modelo mais complexo |
| Erro baixo no treino e alto no teste | Overfitting (Alta Variância) | Regularização, mais dados |
| Erro equilibrado | Modelo adequado | Manter configuração |

!!! important
    **Objetivo:** Baixo Bias + Baixa Variância = melhor generalização.

### Regra de Ouro da Prova

* Muito Bias → modelo fraco
* Muita Variância → modelo instável
* Equilíbrio → melhor generalização

---

### O que são Hiperparâmetros?

São configurações externas definidas antes do treinamento.

- Não são aprendidos pelo modelo.
- Eles controlam estrutura, velocidade e comportamento do treino.

### Hiperparâmetros vs Parâmetros

| Tipo | Quem define | Quando são definidos | Exemplo |
| :--- | :--- | :--- | :--- |
| Hiperparâmetros | Cientista de dados | Antes do treino | Learning rate, nº de camadas |
| Parâmetros | Modelo | Durante o treino | Pesos da rede neural |

### Por que o ajuste é importante?

| Impacto | Explicação |
| :--- | :--- |
| Performance | Pode melhorar muito a precisão do modelo |
| Convergência | Evita treino muito lento ou instável |
| Generalização | Reduz underfitting e overfitting |

### Exemplo clássico

- Learning rate muito alto → converge rápido, mas mal
- Learning rate muito baixo → demora demais

### Como Funciona o Ajuste?

1. Definir métrica alvo (ex: accuracy)
2. Testar combinações de hiperparâmetros
3. Avaliar com validação cruzada
4. Escolher melhor resultado



## Técnicas de Ajuste de Hiperparâmetros

| Técnica | Como funciona | Vantagem | Desvantagem |
| :--- | :--- | :--- | :--- |
| Grid Search | Testa todas as combinações possíveis | Simples e completo | Muito custoso |
| Random Search | Testa combinações aleatórias | Mais eficiente que Grid | Pode perder melhor combinação |
| Otimização Bayesiana | Usa probabilidade para escolher próximas combinações | Mais inteligente e eficiente | Mais complexa |
| Hyperband | Elimina modelos ruins cedo | Muito rápido para deep learning | Foco em grandes modelos |

---

## Exemplos de Hiperparâmetros Comuns

| Hiperparâmetro | O que controla |
| :--- | :--- |
| Learning Rate | Velocidade de aprendizado |
| Learning Rate Decay | Redução gradual da taxa |
| Momentum | Direção do próximo passo |
| Nº de Camadas | Profundidade da rede |
| Nº de Nós | Complexidade da rede |
| Batch Size | Tamanho do lote de treino |
| Epochs | Quantas vezes o dataset é usado |
| Eta | Controle para evitar overfitting |


## Fases de um Projeto de ML

A AWS segue este fluxo lógico:

| Fase | Descrição |
| :--- | :--- |
| **1. Definição do Problema** | É viável? Temos dados? |
| **2. Preparação de Dados** | Limpeza e transformação |
| **3. Treinamento** | Onde o algoritmo "estuda" |
| **4. Avaliação** | Teste de estresse do modelo |
| **5. Deployment** | Disponibilizar para o usuário |


## When is ML Not Appropriate?

ML não é ideal quando:

* Regras são simples e determinísticas
* Poucos dados disponíveis
* Custo maior que benefício
* Explicabilidade total é exigida
* Problema pode ser resolvido com lógica simples

!!! tip
    Nem todo problema precisa de ML.



## Resumo Estratégico para Prova

Você precisa dominar:

* Diferença AI vs ML vs DL vs GenAI
* Supervised vs Unsupervised
* Overfitting vs Underfitting
* Bias vs Variance
* Precision vs Recall
* Treinamento vs Inferência
* O que são hiperparâmetros
* Fases do ciclo de ML
* Quando NÃO usar ML
---

## Ciclo de Vida do Modelo de Base (Foundation Model)

| Fase | Descrição | Objetivo |
| :--- | :--- | :--- |
| **1️⃣ Coleta de Dados** | Reunião de grandes volumes de dados (texto, imagem, código, etc.) | Criar base ampla de conhecimento |
| **2️⃣ Pré-treinamento** | Treinamento em larga escala usando aprendizado auto-supervisionado | Aprender padrões gerais da linguagem ou dados |
| **3️⃣ Ajuste Fino (Fine-Tuning)** | Especialização do modelo para tarefas específicas | Melhorar desempenho em casos de uso específicos |
| **4️⃣ Avaliação** | Testes com métricas (loss, accuracy, avaliações humanas) | Garantir qualidade, segurança e desempenho |
| **5️⃣ Implantação (Deployment)** | Disponibilização via API ou serviço (ex: nuvem) | Permitir uso em aplicações reais |
| **6️⃣ Monitoramento** | Acompanhamento de desempenho, viés e segurança | Detectar drift, erros ou uso inadequado |
| **7️⃣ Atualização / Re-treinamento** | Ajustes contínuos com novos dados | Manter modelo atualizado e relevante |

### 🎯 Resumo Estratégico para Prova

- 📚 Pré-treinamento → aprendizado geral
- 🎯 Fine-tuning → especialização
- 🚀 Deploy → disponibilização
- 📊 Monitoramento → governança e melhoria contínua

---

## Avaliação de Modelos (Model Evaluation)

| Categoria | Métrica / Método | O que Avalia | Quando Usar |
| :--- | :--- | :--- | :--- |
| **Métricas Quantitativas (Treinamento)** | Training Loss | Erro no conjunto de treino | Monitorar aprendizado |
| | Validation Loss | Erro em dados não vistos | Detectar overfitting |
| | Perplexidade (PPL) | Capacidade de prever próxima palavra | Modelos de linguagem |
| **Geração de Texto (LLMs)** | ROUGE | Sobreposição com texto de referência | Sumarização |
| | BLEU | Similaridade com tradução de referência | Tradução automática |
| | BERTScore | Similaridade semântica por embeddings | Avaliar significado |
| **Classificação** | Acurácia | % de previsões corretas | Dados balanceados |
| | Precisão | % de positivos corretos | Reduzir falso positivo |
| | Recall | % de positivos recuperados | Reduzir falso negativo |
| | F1-Score | Equilíbrio entre precisão e recall | Classes desbalanceadas |
| **QA (Perguntas e Respostas)** | Exact Match (EM) | Correspondência exata com resposta correta | Avaliação objetiva |
| **Avaliação Qualitativa** | Avaliação Humana | Coerência, fluidez, factualidade, segurança | Avaliação profunda |
| | LLM-as-a-Judge | Julgamento automatizado por outro LLM | Escalabilidade |

### 🎯 Conceitos-Chave para Prova

- 📉 Validation loss → principal para evitar overfitting
- 🧠 BERTScore > BLEU/ROUGE para capturar significado
- ⚖ F1-score → essencial em datasets desbalanceados
- 👩‍⚖️ Avaliação humana → qualidade subjetiva

---

## Desafios e Riscos em IA (IA Responsável)

| Desafio / Risco | O que é | Impacto | Como Mitigar |
| :--- | :--- | :--- | :--- |
| **Viés (Bias)** | Modelo reproduz preconceitos presentes nos dados | Decisões injustas ou discriminatórias | Curadoria de dados, avaliação contínua, testes de fairness |
| **Alucinação** | Modelo gera informação incorreta com alta confiança | Desinformação | RAG, validação factual, filtros |
| **Falta de Transparência (Explainability)** | Dificuldade de explicar decisões do modelo | Baixa confiança e risco regulatório | Modelos interpretáveis, documentação |
| **Privacidade de Dados** | Uso indevido ou vazamento de dados sensíveis | Risco legal e reputacional | Anonimização, criptografia, governança |
| **Segurança (Security)** | Ataques como prompt injection ou data poisoning | Manipulação do sistema | Validação de entrada, monitoramento |
| **Overfitting** | Modelo memoriza dados de treino | Baixa generalização | Validação adequada, regularização |
| **Drift de Dados** | Mudança nos dados ao longo do tempo | Perda de desempenho | Monitoramento contínuo |
| **Uso Indevido (Misuse)** | Aplicação maliciosa da IA | Danos sociais | Políticas de uso responsável |
| **Toxicidade** | Geração de conteúdo ofensivo ou perigoso | Risco legal e ético | Filtros de conteúdo |

### 🎯 Conceitos que mais caem em prova

- ⚖ Bias → justiça e fairness
- 🧠 Alucinação → risco comum em LLMs
- 🔒 Privacidade → proteção de dados
- 🛡 Segurança → ataques como prompt injection
- 📉 Drift → necessidade de monitoramento contínuo

---

## Embeddings – Resumo

| Aspecto | Descrição |
| :--- | :--- |
| **O que são** | Representações numéricas (vetores) que capturam o significado semântico de dados |
| **Entrada** | Texto, imagem, áudio ou outros dados |
| **Saída** | Vetor em espaço multidimensional |
| **Objetivo** | Medir similaridade semântica |
| **Como funciona** | Dados são convertidos em números onde proximidade = similaridade |
| **Base técnica** | Espaço vetorial + cálculo de distância (ex: similaridade de cosseno) |
| **Principais usos** | Busca semântica, RAG, recomendação, clustering |
| **Benefício principal** | Permite entender significado, não apenas palavras-chave |

### 🎯 Frase-chave para prova

Embeddings transformam dados em vetores numéricos que preservam significado semântico, permitindo comparar similaridade.



## Prompt Performance Optimization

É o processo de melhorar a eficiência e qualidade dos prompts.

### Foca em:
* Reduzir número de tokens (menor custo)
* Ajustar temperature (controla criatividade)
* Melhorar clareza da instrução
* Fornecer contexto relevante
* Definir formato estruturado (ex: JSON)

> **Objetivo:** melhor resposta com menor custo e maior previsibilidade.

---

## Tabela de Parâmetros (LLMs)

| Parâmetro | O que controla | Valores baixos | Valores altos | Faixa comum | Caso de uso |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Temperature** | Criatividade / aleatoriedade | 0 – 0.3 → determinístico | 0.7 – 1.0+ → criativo | 0 a 1 | Baixa: respostas técnicas, jurídicas, financeiras. Alta: geração criativa, storytelling |
| **Top-p** | Probabilidade acumulada (nucleus sampling) | 0.1 – 0.5 → conservador | 0.9 – 1.0 → diverso | 0 a 1 | Controlar diversidade mantendo coerência |
| **Top-k** | Nº de palavras candidatas | 1 – 20 → previsível | 50 – 100+ → varied | Inteiro ≥ 1 | Ajustar variedade sem perder controle |
| **Max Length** | Tamanho máximo da resposta | 50–100 tokens → curto | 500–2000+ → longo | Depende do modelo | Respostas objetivas vs relatórios longos |
| **Stop Sequences** | Onde o modelo deve parar | "###", "Fim", "\nUsuário:" | — | Texto definido pelo usuário | Chatbots estruturados, evitar extrapolação |

### 🎯 Dica de Prova

- Temperature baixa → precisão
- Temperature alta → criatividade
- Top-p / Top-k → controlam diversidade
- Max length → controla custo + tamanho
- Stop sequence → controle de formato

---

## Técnicas de Prompt Engineering

| Tipo                       | O que é                                 | Como funciona                              | Quando usar                                   | Exemplo                                            |
| -------------------------- | --------------------------------------- | ------------------------------------------ | --------------------------------------------- | -------------------------------------------------- |
| **Zero-Shot Learning**     | Executa tarefa sem exemplos             | Apenas instrução no prompt                 | Modelo já pré-treinado amplamente             | “Classifique esse texto como positivo ou negativo” |
| **One-Shot Learning**      | Recebe 1 exemplo                        | Um exemplo guia o padrão                   | Tarefa nova ou específica                     | “Exemplo: X → Positivo. Agora classifique Y”       |
| **Few-Shot Learning**      | Recebe poucos exemplos                  | Aprende padrão pelo contexto               | Melhorar consistência                         | Fornecer 3 exemplos antes da tarefa                |
| **Chain-of-Thought (CoT)** | Raciocínio passo a passo                | Decompõe problema em etapas                | Problemas lógicos/matemáticos                 | “Explique passo a passo”                           |
| **In-Context Learning**    | Aprende temporariamente pelo contexto   | Ajusta comportamento sem retreinar         | Customização rápida                           | Definir formato antes da resposta                  |
| **Role Prompting**         | Define um “papel” para o modelo assumir | Modelo responde sob perspectiva específica | Controlar tom, especialização ou profundidade | “Você é um especialista em segurança AWS…”         |
| **Negative Learning**      | Ensinar o que NÃO fazer                 | Instruções explícitas de restrição         | Reduzir erros/comportamentos indesejados      | “Não inclua opinião pessoal”                       |
| **Continue Pre-Training**  | Continuação do pré-treinamento          | Atualiza pesos do modelo                   | Adaptar a domínio específico                  | Treinar modelo geral com dados médicos             |


### RAG (Retrieval-Augmented Generation)

**Definição:** Combina busca em base de conhecimento com geração por modelo de linguagem.

**Fluxo:**

1. Usuário faz uma pergunta
2. Sistema busca documentos relevantes na base de conhecimento
3. Modelo gera a resposta com base nesses documentos

**Benefícios:**

| Benefício | Descrição |
| :--- | :--- |
| Reduz alucinações | Ancora resposta em dados reais |
| Atualiza o conhecimento | Sem necessidade de re-treinamento |
| Protege dados privados | Dados ficam fora do modelo |


### Armazenamento de Embeddings (Vector Databases)

Serviços AWS que suportam vetores:

| Serviço | Uso |
| :--- | :--- |
| **Amazon OpenSearch Service** | Busca vetorial e semântica |
| **Amazon Aurora** | Banco relacional com suporte a vetores |
| **Amazon Neptune** | Banco de grafos |
| **Amazon DocumentDB** | Banco de documentos |
| **Amazon RDS for PostgreSQL** | PostgreSQL com extensão pgvector |

**Usado para:** Busca semântica, similaridade vetorial e RAG.





### Personalização do modelo — Comparação de Custos

| Método | Custo | Complexidade | Quando usar |
| :--- | :--- | :--- | :--- |
| **Prompt Engineering** | Muito baixo | Baixa | Sempre primeiro |
| **Few-shot** | Baixo | Baixa | Pequenas melhorias |
| **RAG** | Médio | Média | Dados atualizados |
| **Fine-tuning** | Alto | Alta | Domínio específico |
| **Pré-treinamento do zero** | Altíssimo | Extremamente alta | Raramente usado |

!!! tip
    **Ordem de prioridade AWS:** Prompt → RAG → Fine-tuning → Pré-treinar do zero



### Riscos de Segurança em Prompts

| Risco | Definição |
| :--- | :--- |
| **Prompt Injection** | Manipulação maliciosa da instrução |
| **Data Leakage** | Vazamento de dados sensíveis |
| **Jailbreak** | Bypass das restrições do modelo |
| **Prompt Poisoning** | Contaminação de entradas |

!!! important
    **Como mitigar:** Validação de entrada, filtros de conteúdo e uso de **Guardrails** no Amazon Bedrock.


## Treinamento e Ajuste Fino (Fine Tuning)

### Fases do Desenvolvimento

| Fase | O que é |
| :--- | :--- |
| **Pré-treinamento** | Treino massivo inicial com dados da internet |
| **Fine-tuning** | Ajuste para tarefa ou domínio específico |
| **Continuous Pretraining** | Continuação do pré-treino com novo corpus |


### Métodos de Fine-tuning

| Método | Descrição |
| :--- | :--- |
| **Instruction Tuning** | Ensina o modelo a seguir instruções |
| **Domain Adaptation** | Adapta para vocabulário e domínio específico |
| **Transfer Learning** | Reutiliza pesos pré-treinados |
| **RLHF** | Humanos avaliam respostas e ajudam no alinhamento |

!!! note
    **RLHF (Reinforcement Learning from Human Feedback):** Humanos avaliam as respostas do modelo para melhorar alinhamento com valores humanos.




##  Otimização de Modelos

### Objetivo das Técnicas de Otimização

Reduzir custo, latência e uso de memória **mantendo desempenho aceitável**.

---

### Pruning

| Aspecto | Descrição |
| :--- | :--- |
| **O que faz** | Remove pesos menos importantes do modelo |
| **Resultado** | Modelo menor e mais rápido |
| **Trade-off** | Pode perder um pouco de precisão |

---

### Quantization

| Aspecto | Descrição |
| :--- | :--- |
| **O que faz** | Reduz precisão numérica (ex: 32 bits → 8 bits) |
| **Resultado** | Menor uso de memória e inferência mais rápida |
| **Trade-off** | Pequena perda de qualidade |

---

### Distillation

| Aspecto | Descrição |
| :--- | :--- |
| **O que faz** | Treina modelo pequeno (student) para imitar modelo grande (teacher) |
| **Resultado** | Modelo menor com latência e custo menores |
| **Trade-off** | Requer processo adicional de treinamento |

---

### Comparação Rápida das Técnicas

| Técnica | Reduz Tamanho | Reduz Latência | Precisa de Novo Treino? |
| :--- | :--- | :--- | :--- |
| **Pruning** | Sim | Sim | Não necessariamente |
| **Quantization** | Sim | Sim | Não |
| **Distillation** | Sim | Sim | Sim |

!!! tip
    **Para a prova AWS:**
    - "Reduzir custo mantendo desempenho aceitável" → Pruning, Quantization ou Distillation
    - "Executar modelo em ambiente com recurso limitado" → **Quantization** ou **Distillation**
    - "Criar versão mais leve de modelo grande" → **Distillation**


### Qual abordagem escolher?

| Ordem | Abordagem | Quando usar |
| :--- | :--- | :--- |
| **1** | Melhorar o Prompt | Sempre tente primeiro |
| **2** | Usar RAG | Dados precisam ser atualizados ou privados |
| **3** | Fine-tuning | Domínio muito específico |
| **4** | Treinar do zero | Quase nunca — custo altíssimo |


## O que é Stable Diffusion?

Stable Diffusion é um modelo de IA generativa que produz imagens fotorrealistas exclusivas a partir de instruções de texto e imagem.

### Por que o Stable Diffusion é importante?

É acessível e fácil de usar. Pode ser executado em placas gráficas de consumo. Qualquer pessoa pode baixar o modelo e gerar suas imagens. Você tem controle sobre hiperparâmetros como o número de etapas de redução de ruído e o grau de ruído aplicado.

### Como o Stable Diffusion funciona?

Como modelo de difusão, o Stable Diffusion difere de outros modelos de geração de imagens. Modelos de difusão usam ruído gaussiano para codificar uma imagem. Em seguida, usam um preditor de ruído junto com um processo de difusão reversa para recriar a imagem.

---

## Multimodal Search (Busca Multimodal)

| Aspecto | Resumo |
| :--- | :--- |
| **O que é** | Método de busca que utiliza múltiplos tipos de dados (texto, imagem, áudio, vídeo) ao mesmo tempo para encontrar informações |
| **Objetivo** | Entender melhor a intenção do usuário usando diferentes formatos de entrada |
| **Principais Características** | Permite múltiplas entradas (foto + texto, voz, etc.), retorna resultados em diversos formatos e usa compreensão semântica |
| **Diferença da busca tradicional** | Não depende apenas de palavras-chave; entende significado e contexto |
| **Como funciona (técnico)** | Usa IA e embeddings para converter diferentes tipos de dados em um mesmo espaço vetorial compartilhado |
| **Benefício principal** | Resultados mais precisos, contextuais e alinhados à intenção humana |

---

## Busca Tradicional vs Busca Multimodal

| Critério | Busca Tradicional | Busca Multimodal |
| :--- | :--- | :--- |
| **Tipo de entrada** | Texto (palavras-chave) | Texto, imagem, áudio, vídeo ou combinação |
| **Método de busca** | Correspondência exata de palavras | Compreensão semântica com IA |
| **Tecnologia base** | Indexação e matching de texto | Embeddings + espaço vetorial compartilhado |
| **Compreensão de contexto** | Limitada | Alta (entende intenção) |
| **Formato dos resultados** | Principalmente texto | Texto, imagem, vídeo ou áudio |
| **Exemplo prático** | Digitar: "sofá azul" | Enviar foto de sofá + escrever "cor azul" |
| **Precisão semântica** | Baseada em palavra exata | Baseada em significado |

### 🧠 Resumo Estratégico

- 🔎 Busca tradicional → palavra-chave
- 🧠 Busca multimodal → significado + múltiplos formatos
- 📐 Base técnica da multimodal → embeddings + vector search

---

## Tipos de Hiperparâmetros

Os hiperparâmetros são configurações definidas antes do treinamento e que controlam como o modelo aprende.

Podemos dividir em 3 principais categorias:

### 1️⃣ Hiperparâmetros de Otimização

Controlam como o modelo aprende.

| Hiperparâmetro | O que faz |
| :--- | :--- |
| **Learning Rate** | Define o tamanho do passo na atualização dos pesos |
| **Optimizer (Adam, SGD)** | Algoritmo usado para atualizar os pesos |
| **Momentum** | Acelera o aprendizado em direções consistentes |
| **Weight Decay** | Regularização para evitar overfitting |

### 2️⃣ Hiperparâmetros de Treinamento

Controlam como o processo de treino ocorre.

| Hiperparâmetro | O que faz |
| :--- | :--- |
| **Epochs** | Número de vezes que o modelo percorre todo o dataset |
| **Batch Size** | Quantidade de exemplos usados antes de atualizar os pesos |
| **Early Stopping** | Interrompe treino quando validação piora |

### 3️⃣ Hiperparâmetros de Arquitetura

Controlam a estrutura do modelo.

| Hiperparâmetro | O que faz |
| :--- | :--- |
| **Número de camadas (layers)** | Profundidade da rede |
| **Número de neurônios** | Capacidade do modelo |
| **Dimensão de embeddings** | Tamanho da representação vetorial |
| **Número de attention heads (LLMs)** | Complexidade do mecanismo de atenção |

### 🎯 Resumo para prova

- 🔧 Learning rate → controla velocidade
- 🔁 Epochs → controla duração
- 📦 Batch size → controla tamanho do lote
- 🏗 Arquitetura → controla complexidade

---

## Shadow Deployment

O Shadow Deployment (ou "implantação sombra", "modo sombra" / dark launch) em Machine Learning é uma estratégia de MLOps na qual um novo modelo de IA é implantado em produção ao lado do modelo atual (ativo), mas sem interagir com os usuários finais. 

