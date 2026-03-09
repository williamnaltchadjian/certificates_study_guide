# FM - Foundation Models

---

## Overfitting

| Aspecto                  | Resumo                                                                                                                                   |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Conceito**             | **Overfitting**                                                                                                                          |
| **O que é**              | Quando o modelo **aprende demais os dados de treinamento**, incluindo **ruídos**, e perde capacidade de **generalizar para novos dados** |
| **Tipo de aprendizado**  | Ocorre principalmente em **Supervised Learning (Aprendizado Supervisionado)**                                                            |
| **Bias (Viés)**          | **Baixo Bias**                                                                                                                           |
| **Variância (Variance)** | **Alta Variância**                                                                                                                       |
| **Quando acontece**      | Modelo **muito complexo**, **poucos dados** ou **treinamento excessivo**                                                                 |
| **Consequência**         | **Alta performance no treino**, mas **baixa performance em dados novos (teste)**                                                         |
| **Exemplo**              | Modelo com **~100% de acerto no treino**, mas **erra muito em dados novos**                                                              |

---

## Underfitting

| Aspecto                  | Resumo                                                                                                |
| ------------------------ | ----------------------------------------------------------------------------------------------------- |
| **Conceito**             | **Underfitting**                                                                                      |
| **O que é**              | Quando o modelo **não consegue aprender os padrões dos dados**, sendo **simples demais**              |
| **Tipo de aprendizado**  | Ocorre principalmente em **Supervised Learning (Aprendizado Supervisionado)**                         |
| **Bias (Viés)**          | **Alto Bias**                                                                                         |
| **Variância (Variance)** | **Baixa Variância**                                                                                   |
| **Quando acontece**      | Modelo **muito simples**, **pouco treinamento** ou **features insuficientes**                         |
| **Consequência**         | **Baixa performance tanto no treino quanto em novos dados**                                           |
| **Exemplo**              | Modelo que **erra muito no treinamento e também no teste** porque **não aprendeu o padrão dos dados** |

---

## Variance (Variância)

| Aspecto             | Resumo                                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Conceito**        | **Variance (Variância)**                                                                                                  |
| **O que é**         | Mede **o quanto o modelo muda suas previsões quando recebe diferentes dados de treinamento**                              |
| **Significado**     | Indica **sensibilidade do modelo aos dados**                                                                              |
| **Alta Variância**  | Modelo **muito sensível aos dados de treino**, podendo causar **Overfitting**                                             |
| **Baixa Variância** | Modelo **mais estável**, com previsões semelhantes em diferentes conjuntos de dados                                       |
| **Exemplo**         | Se o modelo muda muito suas previsões quando treinado com **pequenas mudanças no dataset**, ele possui **alta variância** |

---

## Bias (Viés)

| Aspecto         | Resumo                                                                                                                 |
| --------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Conceito**    | **Bias (Viés)**                                                                                                        |
| **O que é**     | Mede **o erro causado por suposições simplificadas do modelo ao aprender os dados**                                    |
| **Significado** | Indica **o quanto o modelo está distante do padrão real dos dados**                                                    |
| **Alto Bias**   | Modelo **simples demais**, não aprende bem os padrões → pode causar **Underfitting**                                   |
| **Baixo Bias**  | Modelo **mais flexível**, consegue se ajustar melhor aos dados                                                         |
| **Exemplo**     | Usar **regressão linear** para um problema com relação **não linear complexa**, fazendo o modelo errar mesmo no treino |

---

## Tipos de Aprendizado

- Aprendizado supervisionado
- Aprendizado não supervisionado
- Aprendizado por reforço
- Aprendizado por transferência

---

## Amazon Bedrock

- Bedrock RAG
- Bedrock Guardrails
- Bedrock

---

## 1 - Quais são as técnicas de customização de um modelo

- Aprendizado em Contexto
- Geração Aumentada por Recuperação
- Ajuste fino - Fine Tuning
- Pré-treinamento

---

## 2 - Riscos de segurança em LLM

- Sequestro de Prompt - Prompt Hijacking
- Fuga de Segurança - Jailbreaking
- Envenenamento de Prompt - Prompt Poisoning
- Vazamento de Dados - Data Leakage

---

## 3 - Quais são as etapas do RAG

- Ingestão
- Fragmentação
- Vetorização
- Armazenamento Vetorial

---

## 4 - O que é a técnica PEFT (Parameter-Efficient Fine-Tuning)

- Método de ajuste fino que modifica apenas uma pequena parte dos parâmetros do modelo em vez de todos
- Reduz drasticamente custo computacional e tempo de treinamento
- Muito usado para adaptar grandes modelos sem precisar retreiná-los completamente

---

## 5 - Quais são os tipos de Avaliação de Modelos

- **Classificação** - A classificação é usada quando o objetivo é atribuir um dado a uma categoria ou classe específica.
- **Regressão** - A técnica de regressão é usada quando o objetivo é prever um valor numérico contínuo.
- **Clusterização** - O agrupamento é usado para encontrar padrões ocultos e organizar os dados em grupos baseados em similaridades, sem que você saiba previamente quais são esses grupos.

---

## 6 - Métricas de Avaliação de Modelos - Classificação

### Accuracy (Acurácia)

| Aspecto                 | Resumo                                                                           |
| ----------------------- | -------------------------------------------------------------------------------- |
| **Métrica**             | **Accuracy (Acurácia)**                                                          |
| **O que é**             | Proporção de **previsões corretas** do modelo                                    |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                             |
| **Tipo de problema**    | **Classification (Classificação)**                                               |
| **Quando usar**         | **Dataset balanceado** e quando quer medir o **desempenho geral**                |
| **Quando não usar**     | **Dataset desbalanceado** ou quando **erros têm impactos diferentes**            |
| **Exemplo**             | Modelo de fraude com **99% de Accuracy**, mas que **não detecta nenhuma fraude** |

---

### Precision (Precisão)

| Aspecto                 | Resumo                                                                                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **Precision (Precisão)**                                                                                      |
| **O que é**             | Proporção de **previsões positivas corretas** entre todas as previsões positivas feitas pelo modelo           |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                          |
| **Tipo de problema**    | **Classification (Classificação)**                                                                            |
| **Quando usar**         | Quando **False Positives são críticos**                                                                       |
| **Quando não usar**     | Quando é mais importante **não perder casos positivos (False Negatives)**                                     |
| **Exemplo**             | Detecção de **spam**: se o modelo marcar um e-mail como spam, a **Precision mede quantos realmente são spam** |

---

### Recall (Sensibilidade / True Positive Rate)

| Aspecto                 | Resumo                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| **Métrica**             | **Recall (Sensibilidade / True Positive Rate)**                                                       |
| **O que é**             | Proporção de **positivos reais que o modelo conseguiu identificar corretamente**                      |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                  |
| **Tipo de problema**    | **Classification (Classificação)**                                                                    |
| **Quando usar**         | Quando **não detectar um caso positivo é crítico**                                                    |
| **Quando não usar**     | Quando **falsos positivos são mais problemáticos**                                                    |
| **Exemplo**             | Diagnóstico médico: o **Recall mede quantos pacientes realmente doentes o modelo conseguiu detectar** |

---

### F1 Score

| Aspecto                 | Resumo                                                                                                                                 |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **F1 Score**                                                                                                                           |
| **O que é**             | Média harmônica entre **Precision** e **Recall**, equilibrando as duas métricas                                                        |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                                   |
| **Tipo de problema**    | **Classification (Classificação)**                                                                                                     |
| **Quando usar**         | **Dataset desbalanceado** ou quando **Precision e Recall são igualmente importantes**                                                  |
| **Quando não usar**     | Quando apenas **uma das métricas (Precision ou Recall) é mais importante**                                                             |
| **Exemplo**             | Detecção de **fraude**: o **F1 Score** avalia o equilíbrio entre **detectar fraudes (Recall)** e **evitar falsos alarmes (Precision)** |

---

### AUC-ROC (Receiver Operating Characteristic / Area Under the Curve)

| Aspecto                 | Resumo                                                                                                                                                                                         |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **ROC Curve (Receiver Operating Characteristic) / AUC (Area Under the Curve)**                                                                                                                 |
| **O que é**             | **ROC Curve** mostra a relação entre **True Positive Rate (Recall)** e **False Positive Rate**. **AUC** mede a **área sob essa curva**, indicando a capacidade do modelo de distinguir classes |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                                                                                           |
| **Tipo de problema**    | **Classification (Classificação)**                                                                                                                                                             |
| **Quando usar**         | Para avaliar **modelos de classificação probabilísticos** e comparar diferentes modelos                                                                                                        |
| **Quando não usar**     | Quando o problema exige foco específico em **Precision ou Recall**                                                                                                                             |
| **Exemplo**             | Em **detecção de fraude**, um modelo com **AUC próxima de 1** consegue **distinguir bem entre transações fraudulentas e normais**                                                              |

---

## Métricas de Avaliação de Modelos - Regressão

### MSE (Mean Squared Error)

| Aspecto                 | Resumo                                                                                                     |
| ----------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **MSE (Mean Squared Error)**                                                                               |
| **O que é**             | Média dos **quadrados dos erros** entre o valor real e o valor previsto pelo modelo                        |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                       |
| **Tipo de problema**    | **Regression (Regressão)**                                                                                 |
| **Quando usar**         | Quando se quer **penalizar erros grandes**, pois o erro é elevado ao quadrado                              |
| **Quando não usar**     | Quando há **outliers fortes**, pois eles podem distorcer muito o resultado                                 |
| **Exemplo**             | Previsão de **preço de casas**: o MSE mede o quanto as previsões do modelo **se afastam dos preços reais** |

---

### MAE (Mean Absolute Error)

| Aspecto                 | Resumo                                                                                                      |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **MAE (Mean Absolute Error)**                                                                               |
| **O que é**             | Média dos **erros absolutos** entre o valor real e o valor previsto pelo modelo                             |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                        |
| **Tipo de problema**    | **Regression (Regressão)**                                                                                  |
| **Quando usar**         | Quando se quer **interpretar facilmente o erro médio** e reduzir impacto de **outliers**                    |
| **Quando não usar**     | Quando se deseja **penalizar erros grandes mais fortemente**                                                |
| **Exemplo**             | Previsão de **vendas**: se o MAE for 10, significa que o modelo erra em média **10 unidades nas previsões** |

---

### RMSE (Root Mean Squared Error)

| Aspecto                 | Resumo                                                                                                                           |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **RMSE (Root Mean Squared Error)**                                                                                               |
| **O que é**             | **Raiz quadrada do MSE**, mede o tamanho médio do erro entre valores reais e previstos                                           |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                             |
| **Tipo de problema**    | **Regression (Regressão)**                                                                                                       |
| **Quando usar**         | Quando se quer medir o erro **na mesma unidade da variável prevista** e **penalizar erros grandes**                              |
| **Quando não usar**     | Quando existem **outliers muito extremos**, pois eles podem aumentar muito o erro                                                |
| **Exemplo**             | Previsão de **preço de casas**: se o RMSE for 20.000, significa que o modelo erra em média **cerca de 20 mil no preço previsto** |

---

### R² (R-Squared / Coefficient of Determination)

| Aspecto                 | Resumo                                                                                                         |
| ----------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **R² (R-Squared / Coefficient of Determination)**                                                              |
| **O que é**             | Mede **quanto da variabilidade dos dados é explicada pelo modelo**                                             |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                           |
| **Tipo de problema**    | **Regression (Regressão)**                                                                                     |
| **Quando usar**         | Para avaliar **o quanto o modelo explica os dados** em problemas de regressão                                  |
| **Quando não usar**     | Quando o objetivo é **medir erro absoluto do modelo** ou comparar modelos com **datasets diferentes**          |
| **Exemplo**             | Previsão de **preço de casas**: um **R² = 0.80** significa que o modelo explica **80% da variação dos preços** |

---

## NLP Metrics (Métricas de Processamento de Linguagem Natural)

### ROUGE (Recall-Oriented Understudy for Gisting Evaluation)

| Aspecto                 | Resumo                                                                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **ROUGE (Recall-Oriented Understudy for Gisting Evaluation)**                                                                   |
| **O que é**             | Métrica que mede **similaridade entre textos**, comparando o texto gerado pelo modelo com um **texto de referência**            |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                            |
| **Tipo de problema**    | **Natural Language Processing (NLP)** – principalmente **Text Summarization**                                                   |
| **Quando usar**         | Para avaliar **qualidade de resumos automáticos ou textos gerados por IA**                                                      |
| **Quando não usar**     | Quando a tarefa não envolve **comparação entre textos**                                                                         |
| **Exemplo**             | Em **geração automática de resumos**, o **ROUGE** mede o quanto o resumo gerado é **semelhante ao resumo humano de referência** |

---

### BLEU (Bilingual Evaluation Understudy)

| Aspecto                 | Resumo                                                                                                                                 |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **BLEU (Bilingual Evaluation Understudy)**                                                                                             |
| **O que é**             | Métrica que mede **similaridade entre um texto gerado e um texto de referência**, baseada na **sobreposição de palavras ou n-grams**   |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                                   |
| **Tipo de problema**    | **Natural Language Processing (NLP)** – principalmente **Machine Translation**                                                         |
| **Quando usar**         | Para avaliar **traduções automáticas ou textos gerados por modelos de linguagem**                                                      |
| **Quando não usar**     | Quando a tarefa não envolve **comparação direta entre textos**                                                                         |
| **Exemplo**             | Em **tradução automática**, o **BLEU Score** mede o quanto a tradução gerada pelo modelo é **semelhante à tradução feita por humanos** |

---

### BERTScore

| Aspecto                 | Resumo                                                                                                                             |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **BERTScore**                                                                                                                      |
| **O que é**             | Métrica que avalia **similaridade semântica entre textos** usando embeddings de modelos baseados em **BERT**                       |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                               |
| **Tipo de problema**    | **Natural Language Processing (NLP)** – geração de texto, tradução e sumarização                                                   |
| **Quando usar**         | Quando se quer avaliar **similaridade de significado (semântica)** entre textos, não apenas palavras iguais                        |
| **Quando não usar**     | Quando basta medir **sobreposição literal de palavras** (como em métricas mais simples)                                            |
| **Exemplo**             | Avaliar se uma **resposta gerada por IA** tem **mesmo significado que a resposta de referência**, mesmo usando palavras diferentes |

---

### Perplexity

| Aspecto                 | Resumo                                                                                                                            |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Métrica**             | **Perplexity**                                                                                                                    |
| **O que é**             | Mede **o quão bem um modelo de linguagem prevê a próxima palavra em uma sequência de texto**                                      |
| **Tipo de aprendizado** | **Supervised Learning (Aprendizado Supervisionado)**                                                                              |
| **Tipo de problema**    | **Natural Language Processing (NLP)** – **Language Modeling**                                                                     |
| **Quando usar**         | Para avaliar **modelos de linguagem** e a **qualidade das previsões de palavras**                                                 |
| **Quando não usar**     | Quando a tarefa não envolve **previsão de sequência de texto**                                                                    |
| **Exemplo**             | Em um **modelo de geração de texto**, uma **Perplexity menor** indica que o modelo **prevê melhor as próximas palavras** na frase |

---

## Tópicos de Estudo

- O que são FM (Foundation Models)
- Diferença entre Fine-Tuning (Instruction Based & Domain Adaptation), Engenharia de Prompt, Retrieval-Augmented Generation (RAG)
- Diferença entre os tipos de aprendizado: supervisionado, não-supervisionado, por reforço, por transferência

### Amazon SageMaker

- SageMaker Canvas
- SageMaker Autopilot
- SageMaker Jumpstart
- SageMaker Ground Truth
- SageMaker Data Wrangler
- SageMaker Feature Store
- SageMaker Studio
- SageMaker Clarify
- SageMaker Model Monitor
- SageMaker Pipelines
- SageMaker Model Cards
- SageMaker Agents
- SageMaker Experiments
- SageMaker Playgrounds
- SageMaker Model Dashboard
- Amazon SageMaker Role Manager

### Conceitos Fundamentais

- Explicabilidade
- Bias (Viés)
- Variância
- Overfitting (Sobreajuste)
- Underfitting (Subajuste)
- Top P
- Top K
- K-Means
- Acurácia
- Temperatura
- Épocas
- Precisão
- Recall

### Tipos de Inferência

- Diferença entre Inferência em lote x Inferência assíncrona
- Diferença entre Throughput provisionado x Throughput sob-demanda

### Conceitos de IA Generativa

- Diferença entre Alucinações x Imprecisão Inerente x Não Determinismo x Interpretabilidade Limitada
- Diferença entre Token, Vetor e Embedding

### Fundamentos de IA

- O que é um LLM
- O que é NLP
- Conceitos de IA, Machine Learning, LLM, Deep Learning, Rede Neural

### Métricas de Avaliação de Modelos

- Acurácia
- Precisão
- Recall
- Desvio Absoluto Médio
- Erro Quadrático Médio
- AUC-ROC
- Perplexidade
- BERTScore
- BLEU
- ROUGE
- F1 Score

### Tipos de Aprendizado

- Zero-Shot Learning
- One-Shot / Single-Shot Learning
- Few-Shot Learning
- Chain-of-Thought
- In-Context Learning
- Negative Learning
- Continue Pré-Training

### Serviços AWS de IA

Diferença entre os serviços:

- AWS Translate
- AWS Comprehend
- AWS Rekognition
- AWS Kendra
- AWS Polly
- AWS Lex
- AWS Transcribe
- AWS Personalize
- AWS Textract

### Serviços AWS de Governança e Compliance

Diferença entre:

- AWS Config
- AWS CloudTrail
- AWS Trusted Advisor
- AWS Audit Manager
- AWS Artifact

### Regulamentações

- O que são GDPR, HIPAA

### Conceitos Avançados

- Qual a diferença entre RLHF e A2I
- Para que serve o AWS Kendra
- O que é a classificação multi-classe
- O que é o Amazon Bedrock?
- Para que servem os Guardrails for Bedrock
- Diferença entre Underfitting x Overfitting
