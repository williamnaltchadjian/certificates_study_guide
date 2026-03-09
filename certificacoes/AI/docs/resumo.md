## O que é IA Generativa (GenAI)?

Diferente da IA Preditiva (que classifica ou prevê números), a GenAI cria **novos dados** (texto, imagem, áudio, código) baseando-se em padrões aprendidos.

## Modelos de Base (Foundation Models - FMs)

São modelos treinados em uma escala massiva de dados (terabytes de internet/livros) que podem ser adaptados para várias tarefas sem precisar de treino do zero.

## o que  e overfitting  


Modelo bom em treinamento mais pessimo em dados novos 
Baixo Bias
Alta variancia

                                                        
## o que e underfitting

Modelo pessimo em treinamento mais pessimo em dados novos 
Alto Bias
Baixa variancia


## o que e variancia

mede **o quanto o modelo muda suas previsões quando recebe diferentes dados de treinamento**                              


## bias - viés
                                                                                                     
Mede **o erro causado por suposições simplificadas do modelo ao aprender os dados**                                    |
| **Significado** | Indica **o quanto o modelo está distante do padrão real dos dados**                                                    |



## quais sao os tipos de aprendizado

| Tipo de Aprendizado | Termo em Inglês | Usa Rótulo? | Objetivo Principal | Principais Técnicas / Modelos | Casos de Uso Comuns |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Supervisionado | Supervised Learning | ✅ Sim | Prever resultado conhecido | Regressão Linear, Regressão Logística, Árvore de Decisão, Random Forest, SVM, Redes Neurais | Previsão de churn, detecção de fraude, previsão de preço |
| Não Supervisionado | Unsupervised Learning | ❌ Não | Descobrir padrões ocultos | K-Means, DBSCAN, PCA, Hierarchical Clustering | Segmentação de clientes, análise exploratória |
| Autossupervisionado | Self-Supervised Learning | ⚠️ Rótulo gerado automaticamente | Aprender representações dos dados | Modelos Transformer, LLMs | Previsão da próxima palavra, embeddings |
| Aprendizado por Reforço | Reinforcement Learning (RL) | ❌ Não usa rótulo tradicional | Maximizar recompensa | Q-Learning, Policy Gradient, Deep RL | Jogos, robótica, otimização de decisões |
| RLHF | Reinforcement Learning from Human Feedback | ⚠️ Usa feedback humano como recompensa | Alinhar modelo às preferências humanas | PPO + Modelo de Recompensa | Ajuste fino de LLMs, alinhamento de IA generativa |
| Aprendizado por Transferência | Transfer Learning | ⚠️ Depende da tarefa | Reutilizar conhecimento de um modelo pré-treinado em uma nova tarefa | Fine-Tuning, Feature Extraction | Visão computacional, NLP, adaptação de modelos pré-treinados |



## Quais sao os Principais Algoritmos de Machine Learning

| Algoritmo | Termo em Inglês | Tipo de Aprendizado | Quando Usar |
|---|---|---|---|
| Regressão Linear | Linear Regression | Supervisionado | Quando o objetivo é **prever um valor numérico contínuo** (ex: preço de casas, vendas futuras). |
| Regressão Logística | Logistic Regression | Supervisionado | Quando o objetivo é **classificação**, geralmente **binária** (ex: spam vs não spam). |
| Árvore de Decisão | Decision Tree | Supervisionado | Quando se deseja um **modelo interpretável** para classificação ou regressão baseado em regras. |
| Random Forest | Random Forest | Supervisionado | Quando se deseja **maior precisão e menor overfitting**, combinando várias árvores de decisão. |
| SVM | Support Vector Machine | Supervisionado | Quando os dados possuem **fronteiras complexas entre classes** ou dimensões altas. |
| Redes Neurais | Neural Networks / Artificial Neural Networks (ANN) | Supervisionado (mais comum) | Quando o problema é **complexo ou envolve grandes volumes de dados**, como imagem, texto ou voz. |
| K-Means | K-Means Clustering | Não Supervisionado | Quando se deseja **segmentar dados em grupos semelhantes** e já se tem uma estimativa do número de clusters. |
| DBSCAN | Density-Based Spatial Clustering of Applications with Noise | Não Supervisionado | Quando os dados possuem **clusters irregulares** e é necessário **detectar ruídos/outliers**. |
| PCA | Principal Component Analysis | Não Supervisionado | Quando é necessário **reduzir dimensionalidade** mantendo a maior parte da informação. |
| Clusterização Hierárquica | Hierarchical Clustering | Não Supervisionado | Quando se deseja **entender a hierarquia entre grupos de dados** ou visualizar relações entre clusters. |




## 🎯 Lembra Rápido para Prova (com Modelos)

| Se a questão falar sobre… | Tipo de Aprendizado | Principais Técnicas / Modelos |
| :--- | :--- | :--- |
| 🔮 Prever algo (valor ou categoria) | Supervisionado | Regressão Linear, Regressão Logística, Árvore de Decisão, Random Forest, SVM, Redes Neurais |
| 🔍 Agrupar ou descobrir padrões | Não Supervisionado | K-Means, DBSCAN, Clustering Hierárquico |
| 📉 Reduzir número de variáveis | Não Supervisionado | PCA |
| 📚 Prever próxima palavra / criar embeddings | Autossupervisionado | Transformers, LLMs |
| 🎮 Agente + ambiente + recompensa | Reforço (RL) | Q-Learning, Policy Gradient, Deep RL |
| 👨‍🏫 Modelo ajustado com feedback humano | RLHF | PPO + Modelo de Recompensa |



## o que é tecnica PEFT(Parameter-Efficient Fine-Tuning)

- Método de ajuste fino que modifica apenas uma pequena parte dos parâmetros do modelo em vez de todos
- Reduz drasticamente custo computacional e tempo de treinamento
- Muito usado para adaptar grandes modelos sem precisar retreiná-los completamente


## O que e fine tuning ?

é o processo de pegar um modelo de inteligência artificial que já foi pré-treinado com uma vasta quantidade de dados genéricos e realizar um treinamento adicional em um conjunto de dados menor e mais específico


## Principais Ameaças em Aplicações com LLMs

| Ameaça | Descrição | Objetivo do Ataque | Como Prevenir |
|---|---|---|---|
| Sequestro de Prompt (Prompt Hijacking) | O usuário insere comandos que **substituem ou alteram as instruções originais do sistema**. | Desviar a IA de sua função original para executar **tarefas arbitrárias**. | Usar **delimitadores claros** (ex: `###`) e instruir o modelo a **ignorar comandos presentes no input do usuário**. |
| Fuga de Segurança (Jailbreaking) | Uso de **técnicas criativas**, como encenação ou modos fictícios (ex: *DAN*), para burlar filtros éticos. | Forçar o modelo a gerar **conteúdo restrito, perigoso ou ilegal**. | Implementar **filtros de moderação externos** e realizar **Red Teaming** (testes de ataques simulados). |
| Envenenamento (Data Poisoning) | Inserção de **dados corrompidos ou enviesados** na base de treino ou em sistemas **RAG**. | Manipular o comportamento futuro do modelo ou criar **respostas maliciosas pré-definidas**. | Fazer **curadoria rigorosa dos dados**, validar **fontes externas** antes da indexação. |
| Vazamento de Dados (Data Leakage) | Exposição acidental de **informações confidenciais ou dados privados** nas respostas do modelo. | Obter **segredos comerciais, senhas ou dados pessoais** (ex: LGPD/GDPR). | Aplicar **anonimização de dados (PII stripping)** e restringir o acesso do modelo a **bases de dados sensíveis**. |


## Quais sao tipos  de Avaliação de Modelos 

| Técnica | Termo em Inglês | Descrição |
|---|---|---|
| Classificação | Classification | Usada quando o objetivo é **atribuir um dado a uma categoria ou classe específica**. |
| Regressão | Regression | Utilizada quando o objetivo é **prever um valor numérico contínuo**. |
| Clusterização | Clustering | Usada para **encontrar padrões ocultos e organizar dados em grupos baseados em similaridade**, sem saber previamente quais são esses grupos. |


## Quais sao as tecnicas de customizacao de um modelo

| Técnica | Termo em Inglês | Descrição |
|---|---|---|
| Aprendizado em Contexto | In-Context Learning | O modelo utiliza **exemplos fornecidos no próprio prompt** para aprender como responder, sem necessidade de novo treinamento. |
| Geração Aumentada por Recuperação | Retrieval-Augmented Generation (RAG) | Combina **recuperação de informações em bases externas** com geração de texto pelo modelo para produzir respostas mais precisas e atualizadas. |
| Ajuste Fino | Fine-Tuning | Processo de **treinar novamente um modelo pré-treinado com dados específicos** para melhorar seu desempenho em uma tarefa ou domínio específico. |
| Pré-treinamento | Pre-training | Fase inicial em que o modelo é **treinado com grandes volumes de dados gerais** para aprender padrões da linguagem antes de ser adaptado para tarefas específicas. |


## Quais sao as etapas do RAG

| Etapa | Termo em Inglês | Descrição |
|---|---|---|
| Ingestão | Ingestion | Processo de **coletar e importar dados** (documentos, PDFs, páginas web, bancos de dados) para serem utilizados pelo sistema. |
| Fragmentação | Chunking | Divisão dos documentos em **pequenos trechos (chunks)** para facilitar o processamento e recuperação de informações. |
| Vetorização | Embedding / Vectorization | Conversão do texto em **vetores numéricos (embeddings)** que representam o significado semântico do conteúdo. |
| Armazenamento Vetorial | Vector Storage / Vector Database | Armazenamento dos **vetores gerados em um banco vetorial** para permitir buscas por similaridade semântica. |


## - Quais sao as Métricas de Avaliação de Modelos 


| Métrica | Termo em Inglês | Categoria / Tipo de Problema | Quando Usar |
|---|---|---|---|
| Acurácia | Accuracy | Classificação | Quando o **dataset é balanceado** e se deseja medir a proporção total de previsões corretas. |
| Precisão | Precision | Classificação | Quando **falsos positivos são críticos**, como em **detecção de spam ou fraude**. |
| Revocação | Recall | Classificação | Quando **falsos negativos são mais graves**, como em **diagnóstico médico**. |
| F1-Score | F1 Score | Classificação | Quando é necessário **equilibrar Precision e Recall**, especialmente com **classes desbalanceadas**. |
| AUC-ROC | Area Under the Curve – ROC | Classificação | Avaliar a **capacidade do modelo de distinguir entre classes**. |
| MAE | Mean Absolute Error | Regressão | Medir o **erro médio absoluto** entre valores previstos e reais. |
| MSE | Mean Squared Error | Regressão | Penalizar **erros maiores**, pois os erros são elevados ao quadrado. |
| RMSE | Root Mean Squared Error | Regressão | Avaliar erro médio com **mesma unidade do valor previsto**. |
| BLEU | Bilingual Evaluation Understudy | Geração de Texto / Tradução | Avaliar **tradução automática**, comparando a saída com traduções de referência. |
| ROUGE | Recall-Oriented Understudy for Gisting Evaluation | Geração de Texto / Sumarização | Avaliar **resumos automáticos**, verificando sobreposição com o texto de referência. |
| METEOR | Metric for Evaluation of Translation with Explicit ORdering | Geração de Texto / Tradução | Avaliação de tradução considerando **sinônimos e variações linguísticas**. |
| Perplexidade | Perplexity (PPL) | Modelos de Linguagem | Medir **quão bem um modelo prevê o próximo token**. |
| BERTScore | BERTScore | NLP / Similaridade Semântica | Comparar **similaridade semântica entre textos** usando embeddings. |
| Avaliação Humana | Human Evaluation | Avaliação Qualitativa | Avaliar **criatividade, utilidade, segurança e tom de voz** das respostas de IA. |


## Avaliação de Modelos (Model Evaluation)

| Categoria de Avaliação | Termo em Inglês | Métricas / Métodos | Quando Usar |
|---|---|---|---|
| Classificação | Classification Evaluation | Accuracy, Precision, Recall, F1-Score, AUC-ROC | Quando o modelo **classifica dados em categorias** (ex: spam vs não spam). |
| Regressão | Regression Evaluation | MAE (Mean Absolute Error), MSE (Mean Squared Error), RMSE (Root Mean Squared Error), R² (R-Squared) | Quando o modelo **prevê valores numéricos contínuos** (ex: preço de casas). |
| Geração de Texto | Text Generation Evaluation | BLEU, ROUGE, METEOR | Quando o modelo gera **traduções, resumos ou textos**. |
| Modelos de Linguagem | Language Model Evaluation | Perplexity (PPL), BERTScore | Quando se avalia **qualidade semântica e capacidade de previsão de tokens**. |
| Avaliação Humana | Human Evaluation | A/B Testing, Likert Scale | Quando é necessário avaliar **qualidade subjetiva**, como utilidade, fluidez e segurança. |
| Benchmarks | Benchmark Evaluation | MMLU, GSM8K, HELM | Quando se deseja **comparar desempenho entre modelos** em tarefas padronizadas. |

## O que é Ajuste de Hiperparâmetros?

É o processo de testar diferentes combinações de hiperparâmetros para encontrar a configuração que gera o melhor desempenho do modelo.


## Quais sao os Tipos de Inferência (Inference Types)

| Tipo | Como Funciona | Casos de Uso | Vantagem | Desvantagem |
| :--- | :--- | :--- | :--- | :--- |
| Inferência em Tempo Real (Real-time Inference) | Modelo hospedado em endpoint sempre ativo, resposta imediata | Chatbots, detecção de fraude, recomendações em e-commerce | Baixa latência, feedback instantâneo | Mais caro (recursos ativos continuamente) |
| Inferência em Lote (Batch Inference / Batch Transform) | Processa grandes volumes de dados de uma vez em horários programados | Relatórios de vendas, análise de sentimento, pontuação de crédito | Mais barato, custo sob demanda | Alta latência (não é imediato) |
| Inferência Assíncrona (Asynchronous Inference) | Envia requisição, recebe recibo e resultado posterior | Geração de imagens, processamento de vídeos | Ideal para tarefas longas | Não é resposta imediata |
| Inferência na Borda (Inference at the Edge) | Processamento direto no dispositivo, sem nuvem | Celular, câmera, sensor industrial | Funciona offline, maior privacidade | Limitado por hardware do dispositivo |


### Quais sao as Fases de um Projeto de ML

A AWS segue este fluxo lógico:

| Fase | Descrição |
| :--- | :--- |
| **1. Definição do Problema** | É viável? Temos dados? |
| **2. Preparação de Dados** | Limpeza e transformação |
| **3. Treinamento** | Onde o algoritmo "estuda" |
| **4. Avaliação** | Teste de estresse do modelo |
| **5. Deployment** | Disponibilizar para o usuário |



## Pipeline de Machine Learning — Resumo Estratégico

| Etapa | O que é | Objetivo Principal | Pontos Importantes |
| :--- | :--- | :--- | :--- |
| Coleta de Dados | Reunião de dados de múltiplas fontes | Garantir volume e qualidade | SQL, logs, S3, APIs |
| AED / EDA | Análise inicial dos dados | Entender padrões e problemas | Missing values, distribuições, padrões |
| Pré-processamento | Limpeza e transformação | Tornar dados utilizáveis | Remover duplicatas, tratar faltantes, converter formatos |
| Engenharia de Atributos | Criação de novas features | Melhorar capacidade do modelo | Ex: Data de Nascimento → Idade |
| Treinamento | Modelo aprende padrões | Gerar conhecimento | Uso de dados históricos |
| Ajuste de Hiperparâmetros | Teste de configurações | Encontrar melhor performance | Profundidade de árvore, combinações de parâmetros |
| Avaliação | Teste com dados não vistos | Validar qualidade | Acurácia, Precisão, Recall |
| Implantação | Colocar em produção | Permitir inferência | Ex: SageMaker Endpoints |
| Monitoramento | Acompanhamento contínuo | Detectar perda de performance | Model Drift |



## Quando o Uso de Machine Learning nao e apropriado ?

ML não é ideal quando:

* Regras são simples e determinísticas
* Poucos dados disponíveis
* Custo maior que benefício
* Explicabilidade total é exigida
* Problema pode ser resolvido com lógica simples



## O que e k-NN no Amazon OpenSearch Service

| Aspecto | Descrição |
| :--- | :--- |
| **O que é** | Plugin para pesquisas de similaridade vetorial |
| **Uso** | Encontrar "vizinhos mais próximos" em espaço vetorial |
| **Algoritmos** | Distância euclidiana, similaridade de cosseno |



### 🔎 O que o chunking faz?

| Função | Benefício |
| :--- | :--- |
| **Divide textos longos** | Facilita processamento |
| **Mantém coerência semântica** | Melhora relevância na busca |
| **Permite indexação vetorial eficiente** | Melhora RAG |
| **Reduz ruído na recuperação** | Respostas mais precisas |


## O que e Embeddings

| Conceito | Explicação |
| :--- | :--- |
| **Embeddings** | Representações numéricas de texto/imagem em vetores |
| **Uso** | Busca semântica, RAG, clustering |
| **Similaridade** | Cosine similarity mede proximidade entre vetores |



### Quais sao os Riscos e Limitações da IA Generativa (Generative AI) – Resumo em Tabela

| Desvantagem | O que é | Causa | Mitigação |
|-------------|--------|-------|------------|
| **Alucinações (Hallucinations)** | Geração de informações falsas, porém convincentes | Modelo é um preditor estatístico de palavras, não um banco de fatos | RAG (Retrieval-Augmented Generation) / Knowledge Bases |
| **Não Determinismo (Non-determinism)** | Respostas diferentes para o mesmo prompt | Natureza probabilística do modelo | Reduzir Temperatura (Temperature = 0) |
| **Falta de Interpretabilidade (Lack of Interpretability / Black Box)** | Difícil explicar por que o modelo tomou uma decisão | Bilhões de parâmetros (model parameters) sem regra explícita | Ferramentas como SageMaker Clarify |
| **Imprecisão e Falta de Raciocínio Lógico (Imprecision / Lack of True Reasoning)** | Erros matemáticos ou falhas em cadeias lógicas longas | Modelo trabalha por associação de padrões (pattern recognition) | Chain-of-Thought (CoT) prompting |
| **Viés e Toxicidade (Bias & Toxicity)** | Respostas ofensivas, estereotipadas ou discriminatórias | Dados de treinamento herdados da internet | Guardrails (ex: Amazon Bedrock Guardrails) |


## Vantagens dos Modelos de IA Generativa / LLMs

| Vantagem | Descrição Curta |
|-----------|----------------|
| Adaptabilidade (Adaptability) | "Um modelo, mil utilidades" |
| Capacidade de Resposta (Responsiveness) | Velocidade extrema via Prompt Engineering |
| Simplicidade (Simplicity) | Linguagem natural em vez de código |
| Eficiência (Efficiency) | Menos dados rotulados manualmente |



## O que e a Arquitetura Transformer — Resumo para Prova

| Conceito | Descrição |
|---|---|
| Arquitetura Transformer | Modelo de Deep Learning usado em NLP que utiliza **mecanismo de atenção (Self-Attention)** para entender o contexto entre palavras. |
| Ideia Principal | Permite que o modelo **analise todas as palavras da frase ao mesmo tempo**, capturando relações entre elas. |
| Componentes Principais | **Self-Attention, Multi-Head Attention, Positional Encoding e Feedforward Neural Network**. |
| Estrutura | Possui **Encoder (entende o texto)** e **Decoder (gera a resposta)**. |
| Vantagem | Melhor **captura de contexto e processamento paralelo**, sendo mais eficiente que RNNs e LSTMs. |
| Usado em | Base dos **LLMs modernos** como GPT, BERT e T5. |


## O que é Prompt Engineering?

**Prompt Engineering** é a prática de escrever instruções claras e estruturadas para obter respostas melhores de modelos de IA generativa.


## Quais sao Parâmetros de Geração

### Tabela de Parâmetros
| Parâmetro | O que controla | Valores baixos | Valores altos | Faixa comum |
| :--- | :--- | :--- | :--- | :--- |
| **Temperature** | Criatividade / aleatoriedade | 0 – 0.3 → determinístico | 0.7 – 1.0+ → criativo | 0 a 1 |
| **Top-p** | Probabilidade acumulada | 0.1 – 0.5 → conservador | 0.9 – 1.0 → diverso | 0 a 1 |
| **Top-k** | Nº de palavras candidatas | 1 – 20 → previsível | 50 – 100+ → variado | Inteiro ≥ 1 |
| **Max Length** | Tamanho máximo da resposta | 50–100 tokens → curto | 500–2000+ → longo | Depende do modelo |
| **Stop Sequences** | Onde o modelo deve parar | "###", "Fim", "\nUsuário:" | — | Texto definido pelo usuário |

### Dicas para a prova:
* **Temperature** = criatividade
* **Top-p** = probabilidade acumulada
* **Top-k** = quantidade fixa de opções
* Temperature alta + Top-p alto = mais variabilidade
* Max tokens controla custo
* Stop sequences evitam texto indesejado



## Quais sao as Técnicas de Prompt Engineering

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




## Quais sao os Princípios de IA Responsável

| Princípio | Foco Principal |
| :--- | :--- |
| **Bias (Viés)** | Dados enviesados |
| **Fairness (Imparcialidade)** | Justiça nas decisões |
| **Inclusion (Inclusão)** | Diversidade e representatividade |
| **Robustness (Robustez)** | Resistência a falhas |
| **Security (Segurança)** | Proteção contra ataques |
| **Truthfulness / Accuracy (Veracidade / Precisão)** | Precisão e confiabilidade |



## Quais sao as Práticas Responsáveis ao Escolher um Modelo (Responsible AI Practices)

| Prática | Termo em Inglês | Descrição |
|---|---|---|
| Justiça | Fairness | Garantir que o modelo **não produza resultados enviesados ou discriminatórios**. |
| Transparência | Transparency | Ser claro sobre **como o modelo funciona e como os dados são utilizados**. |
| Explicabilidade | Explainability / Interpretability | Permitir entender **como o modelo chegou a uma decisão**. |
| Privacidade | Privacy | Proteger **dados sensíveis e informações pessoais (PII)** durante treino e uso do modelo. |
| Segurança | Security | Evitar **ataques, vazamento de dados e uso malicioso da IA**. |
| Responsabilidade | Accountability | Definir **quem é responsável pelas decisões e resultados gerados pelo modelo**. |
| Conformidade | Compliance | Garantir que o modelo esteja **alinhado com leis e regulações** (ex: LGPD, GDPR). |



## Quais sao Principais Riscos Legais da IA Generativa

| Risco | O que significa na prática |
| :--- | :--- |
| **Intellectual Property Infringement (Violação de Propriedade Intelectual)** | O modelo pode gerar conteúdo semelhante a material protegido por direitos autorais |
| **Bias and Discrimination (Viés e Discriminação)** | Resultados injustos podem gerar ações legais ou violar leis antidiscriminação |
| **Loss of Customer Trust (Perda de Confiança do Cliente)** | Respostas incorretas ou inadequadas afetam reputação da empresa |
| **End-User Risk (Risco ao Usuário Final)** | O usuário pode tomar decisões prejudiciais baseadas em respostas erradas |
| **Hallucinations (Alucinações)** | Geração de informações falsas apresentadas como verdadeiras |


## Diferença entre Modelos Transparentes e Não-Transparentes

| Tipo de Modelo | Termo em Inglês | Característica Principal | Exemplos | Quando Usar |
|---|---|---|---|---|
| Modelos Transparentes | Interpretable / Transparent Models | É possível **entender claramente como o modelo tomou a decisão**. | Regressão Linear, Regressão Logística, Árvore de Decisão | Quando **explicabilidade é importante**, como em finanças, saúde ou auditoria. |
| Modelos Não-Transparentes | Black Box Models | O processo interno é **difícil ou impossível de interpretar diretamente**. | Redes Neurais Profundas, Random Forest, SVM, LLMs | Quando se busca **maior precisão em problemas complexos**, como visão computacional ou NLP. |



## O que é Human-Centered Design (HCD)?

**Human-Centered Design** (Design Centrado no Ser Humano) é uma abordagem que:

* Coloca o usuário no centro do desenvolvimento
* Considera contexto social, cultural e ético
* Prioriza clareza, transparência e confiança



## Desafios específicos da IA Generativa:

| Desafio | Descrição |
| :--- | :--- |
| **Hallucinations** | Modelo inventa informações |
| **Toxicidade** | Geração de conteúdo ofensivo |
| **Prompt Injection** | Usuário tenta manipular o modelo para burlar regras |
| **Data Leakage** | Exposição de dados sensíveis |
| **Deepfakes** | Conteúdo sintético enganoso |


## Mitigação:
* RAG
* Guardrails
* Monitoramento
* Controle de acesso



## Bancos de Dados com Busca Vetorial na AWS


| Serviço AWS | Tipo de Banco | Termo em Inglês | Quando Usar | Observação para Prova |
|---|---|---|---|---|
| Amazon OpenSearch Service / OpenSearch Serverless | Motor de busca e analytics | Vector Search with k-Nearest Neighbors (k-NN) | Quando precisa de **busca vetorial em grande escala** para aplicações de IA e RAG | Usa motores como **FAISS, NMSLIB e Lucene** e pode armazenar **bilhões de vetores** |
| Amazon RDS for PostgreSQL / Amazon Aurora | Banco relacional SQL | pgvector extension | Empresas que já usam **PostgreSQL** e querem adicionar **busca por embeddings** sem mudar de banco | Permite **dados relacionais + vetores no mesmo banco** |
| Amazon MemoryDB for Redis | Banco em memória | In-memory Vector Search (Redis-based) | Sistemas que exigem **latência muito baixa** e alta taxa de atualização | Ideal para aplicações **tempo real com milissegundos de resposta** |
| Amazon DocumentDB (compatível com MongoDB) | Banco de documentos | Vector Search for Document Databases | Aplicações baseadas em **JSON / MongoDB** que precisam armazenar e buscar embeddings | Suporte nativo para **armazenar, indexar e consultar vetores** |
| Amazon S3 Vectors | Armazenamento de objetos | Vector Storage for Object Data | Armazenamento **massivo de vetores em larga escala** com busca rápida | Serviço **novo da AWS** para vetores em grande escala com **consultas em subsegundos** |



### Critérios de Seleção de Modelos Pré-Treinados

Quando escolher um modelo no Amazon Bedrock, considere:

| Critério | O que avaliar |
| :--- | :--- |
| **Custo** | Preço por token (input + output) |
| **Latência** | Tempo de resposta |
| **Modalidade** | Texto? Imagem? Multimodal? |
| **Multilíngue** | Suporte a vários idiomas |
| **Tamanho do modelo** | Maior = mais capacidade, mais caro |
| **Janela de contexto** | Quantidade máxima de tokens |
| **Customização** | Permite fine-tuning? |
| **Complexidade** | Modelo grande pode não ser necessário |

!!! tip
    **Regra AWS:** Use o modelo **menor e mais barato** que resolva o problema.



## Etapas de Treinamento de Modelos de IA (AI Model Training Stages)

| Etapa | Termo em Inglês | Descrição | Objetivo | Custo / Complexidade |
|---|---|---|---|---|
| Pré-treinamento | Pre-training | Treinamento do modelo do zero usando enormes volumes de dados não estruturados (internet, livros, códigos, artigos) com aprendizado não supervisionado | Criar um **Modelo de Base (Foundation Model)** com conhecimento geral | **Altíssimo** – milhares de GPUs e meses de processamento |
| Pré-treinamento Contínuo | Continued Pre-training / Domain Adaptation | Continuação do treinamento de um modelo já existente usando dados específicos de um domínio (ex: jurídico ou médico) | Ensinar **vocabulário técnico e conhecimento especializado** | **Alto**, mas menor que o pré-treinamento original |
| Ajuste Fino | Fine-tuning | Treinamento com um dataset menor e **rotulado** (ex: pares de pergunta e resposta) | Ajustar **comportamento, formato de resposta ou estilo** do modelo | **Moderado**, pode ser feito no Amazon Bedrock usando dados no S3 |
| Ajuste Fino por Instrução | Instruction Fine-tuning | Variante do fine-tuning que ensina o modelo a seguir melhor comandos e instruções | Transformar o modelo em **chatbot ou assistente conversacional** | Moderado |



## Técnicas de Ajuste e Aprendizado em Modelos de IA

| Técnica | Termo em Inglês | Descrição | Objetivo | Observação |
|---|---|---|---|---|
| Ajuste por Instrução | Instruction Fine-tuning | Treinamento com pares **{Instrução, Resposta}** para ensinar o modelo a executar tarefas específicas | Fazer o modelo **seguir comandos, resumir, extrair dados ou formatar respostas** | Método mais comum para transformar LLMs em **assistentes ou chatbots** |
| Adaptação de Domínio | Domain Adaptation | Ajuste usando dados de um setor específico (ex: jurídico, petróleo, genômica) | Ensinar **terminologia técnica e jargões especializados** | Meio-termo entre **Fine-tuning** e **Continued Pre-training** |
| Aprendizado por Transferência | Transfer Learning | Reutilização do conhecimento aprendido em uma tarefa para resolver outra | Permitir aprendizado rápido com **menos dados** | Base conceitual por trás do **Fine-tuning moderno** |
| Pré-treinamento Contínuo | Continued Pre-training | Continuação do treinamento original usando **dados brutos privados** | Especializar profundamente o modelo em **um domínio específico** | Diferente do **Fine-tuning**, pois não exige dados rotulados |


## Personalização — Comparação de Custos

| Método | Custo | Complexidade | Quando usar |
| :--- | :--- | :--- | :--- |
| **Prompt Engineering** | Muito baixo | Baixa | Sempre primeiro |
| **Few-shot** | Baixo | Baixa | Pequenas melhorias |
| **RAG** | Médio | Média | Dados atualizados |
| **Fine-tuning** | Alto | Alta | Domínio específico |
| **Pré-treinamento do zero** | Altíssimo | Extremamente alta | Raramente usado |



## Fases do Desenvolvimento

| Fase | O que é |
| :--- | :--- |
| **Pré-treinamento** | Treino massivo inicial com dados da internet |
| **Fine-tuning** | Ajuste para tarefa ou domínio específico |
| **Continuous Pretraining** | Continuação do pré-treino com novo corpus |

---

## Métodos de Fine-tuning

| Método | Descrição |
| :--- | :--- |
| **Instruction Tuning** | Ensina o modelo a seguir instruções |
| **Domain Adaptation** | Adapta para vocabulário e domínio específico |
| **Transfer Learning** | Reutiliza pesos pré-treinados |
| **RLHF** | Humanos avaliam respostas e ajudam no alinhamento |


## Quais sao as tecnicas de otimizacao de um modelo ?


| Técnica | O que faz | Resultado | Trade-off |
|---|---|---|---|
| Pruning | Remove **pesos menos importantes** do modelo | Modelo **menor e mais rápido** | Pode ocorrer **pequena perda de precisão** |
| Quantization | Reduz a **precisão numérica dos pesos** (ex: 32 bits → 8 bits) | **Menor uso de memória** e **inferência mais rápida** | Pode causar **leve perda de qualidade** |
| Distillation | Treina um **modelo pequeno (student)** para imitar um **modelo grande (teacher)** | Modelo **menor, mais rápido e com menor custo** | Requer **processo adicional de treinamento** |


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



## O que é Stable Diffusion?

Stable Diffusion é um modelo de IA generativa que produz imagens fotorrealistas exclusivas a partir de instruções de texto e imagem.

### Por que o Stable Diffusion é importante?

É acessível e fácil de usar. Pode ser executado em placas gráficas de consumo. Qualquer pessoa pode baixar o modelo e gerar suas imagens. Você tem controle sobre hiperparâmetros como o número de etapas de redução de ruído e o grau de ruído aplicado.

### Como o Stable Diffusion funciona?

Como modelo de difusão, o Stable Diffusion difere de outros modelos de geração de imagens. Modelos de difusão usam ruído gaussiano para codificar uma imagem. Em seguida, usam um preditor de ruído junto com um processo de difusão reversa para recriar a imagem.


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



## Estrategias de deploy modelos 

| Estratégia de Implantação | Termo em Inglês | Descrição | Quando Usar |
|---|---|---|---|
| Implantação Sombra | Shadow Deployment | O novo modelo roda **em paralelo com o modelo atual**, processando dados reais sem impactar o usuário. | Avaliar **desempenho em produção sem risco**. |
| Implantação Canário | Canary Deployment | O modelo é liberado para **uma pequena porcentagem de usuários** e expandido gradualmente se funcionar bem. | Detectar **erros ou problemas cedo** antes de liberar para todos. |
| Implantação Azul-Verde | Blue-Green Deployment | Mantém **dois ambientes idênticos**: um com a versão atual (Blue) e outro com a nova (Green). A troca é imediata. | Permitir **rollback rápido** caso haja problemas. |
| Teste A/B | A/B Testing | Duas versões do modelo recebem **partes do tráfego** para comparar qual gera melhores resultados. | Avaliar **qual modelo tem melhor performance ou impacto de negócio**. |

### Conceitos fundamentais:

| Assunto | O que você precisa saber |
| :--- | :--- |
| **Modelo de Responsabilidade Compartilhada** | AWS protege a infraestrutura; você protege dados, acessos e configurações |
| **IAM (Identity and Access Management)** | Controle de acesso com usuários, roles e políticas |
| **Princípio do menor privilégio** | Conceder apenas o acesso estritamente necessário |
| **Criptografia** | Dados em trânsito (TLS) e em repouso (KMS) |
| **Monitoramento** | Logs e auditoria com CloudTrail |


## Conformidade (Compliance)

Compliance garante que o uso de IA:

* Siga leis e regulações vigentes
* Respeite a LGPD / GDPR
* Proteja dados pessoais e sensíveis
* Mantenha registros auditáveis

| Assunto | O que estudar |
| :--- | :--- |
| **LGPD / GDPR** | Proteção de dados pessoais |
| **PII (Personally Identifiable Information)** | Identificação e proteção de dados sensíveis |
| **Data Residency** | Onde os dados estão armazenados |
| **Certificações AWS** | ISO, SOC, HIPAA, etc. |


!!! note
    O **AWS Artifact** é a ferramenta para acessar relatórios de conformidade e auditorias da AWS.


## O que e Governança de IA

Governança de IA significa definir políticas, processos e responsabilidades claras para uso ético dos modelos.

| Assunto | O que entender |
| :--- | :--- |
| **IA Responsável** | Justiça, transparência, explicabilidade |
| **Bias em modelos** | Modelos podem gerar decisões injustas |
| **Explainability** | Entender por que o modelo tomou uma decisão |
| **Human-in-the-loop** | Revisão humana quando necessário |
| **Model Monitoring** | Detectar drift e problemas em produção |


## Serviços AWS Relacionados

| Serviço | Para que serve | Por que cai na prova |
| :--- | :--- | :--- |
| **AWS IAM** | Controle de acesso | Princípio do menor privilégio |
| **AWS KMS** | Gerenciar chaves de criptografia | Proteção de dados sensíveis |
| **AWS CloudTrail** | Auditoria e logs de ações | Conformidade e rastreabilidade |
| **AWS Config** | Monitorar conformidade de recursos | Governança contínua |
| **Amazon SageMaker Clarify** | Detectar bias e explicar modelo | IA responsável |
| **Amazon Augmented AI (A2I)** | Revisão humana de previsões | Human-in-the-loop |
| **Amazon Macie** | Detectar PII automaticamente | Proteção de dados pessoais |
| **AWS Artifact** | Acessar relatórios de compliance | Auditorias e certificações |
| **Amazon GuardDuty** | Detecção de ameaças | Segurança da infraestrutura |