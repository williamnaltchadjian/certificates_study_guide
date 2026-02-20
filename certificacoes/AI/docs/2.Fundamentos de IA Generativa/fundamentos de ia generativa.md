# 🚀 Fundamentos de IA Generativa

*Domínio 2 - Representa 24% da nota*

Para o Domínio 2 (Fundamentos de IA Generativa), a AWS quer testar se você entende a "ciência" por trás da criação de conteúdo e como os modelos de base funcionam antes de serem aplicados.

---

## 🤖 O que é IA Generativa (GenAI)?

Diferente da IA Preditiva (que classifica ou prevê números), a GenAI cria **novos dados** (texto, imagem, áudio, código) baseando-se em padrões aprendidos.

### Modelos de Base (Foundation Models - FMs)

São modelos treinados em uma escala massiva de dados (terabytes de internet/livros) que podem ser adaptados para várias tarefas sem precisar de treino do zero.

### Capacidades Principais

| Tipo | Função | Exemplos |
| :--- | :--- | :--- |
| **Text-to-Text** | Resumos, tradução, chat | Claude, Llama |
| **Text-to-Image** | Criação de artes/diagramas | Stable Diffusion, Titan Image Generator |
| **Text-to-Code** | Gerar scripts SQL, Python, etc. | Codex, CodeLlama |

---

## 🧠 A Arquitetura Transformer (O Motor da GenAI)

> [!NOTE]
> Você não precisa saber a matemática, mas precisa entender os conceitos.

| Conceito | Definição |
| :--- | :--- |
| **Self-Attention** | Permite que o modelo entenda a relação entre palavras distantes em uma frase. Ex: Em "O animal não atravessou a rua porque ele estava cansado", a atenção liga "ele" a "animal" |
| **Tokens** | A "moeda" da GenAI. Palavras são quebradas em pedaços |
| **Janela de Contexto** | O limite de "memória" de curto prazo do modelo em uma conversa |

> [!TIP]
> **Regra de bolso:** 1.000 tokens ≈ 750 palavras.

---

## ⚙️ Parâmetros de Inferência (Ajustando a Resposta)

> [!IMPORTANT]
> No console do Amazon Bedrock, você verá esses controles. Eles caem direto na prova:

| Parâmetro | O que faz? | Quando usar? |
| :--- | :--- | :--- |
| **Temperature** | Controla a aleatoriedade/criatividade | 0.0: Respostas exatas (TI/Código). 1.0: Criatividade total |
| **Top-P / Top-K** | Filtra as palavras mais prováveis | Usado para evitar que o modelo escolha palavras sem sentido |
| **Stop Sequences** | Diz ao modelo onde parar de escrever | Ex: Parar de gerar texto quando encontrar um "###" |

---

## 🔄 O Ciclo de Vida do Modelo de Base

| Fase | Descrição |
| :--- | :--- |
| **Pre-training** | O modelo aprende gramática e fatos do mundo (Custo altíssimo) |
| **Instruction Fine-Tuning** | O modelo aprende a seguir comandos (ex: "Traduza este texto") |
| **RLHF** | Humanos dão notas às respostas. Isso alinha o modelo com valores humanos e segurança |

---

## 📊 Avaliação de Modelos (Model Evaluation)

Como saber qual modelo usar? A AWS cobra as métricas e o processo:

| Tipo | Métrica | Descrição |
| :--- | :--- | :--- |
| **Automática** | ROUGE / BLEU | Usadas para tradução e resumos (comparam a resposta da IA com um texto de referência) |
| **Humana** | Revisão manual | No Amazon Bedrock, você pode configurar um fluxo onde pessoas revisam as respostas para critérios de toxicidade, precisão e estilo |

---

## ⚠️ Desafios e Riscos (Fundamentais para IA Responsável)

| Risco | Descrição |
| :--- | :--- |
| **Alucinações** | O modelo gera informações falsas com confiança |
| **Vazamento de Dados** | Risco de dados sensíveis do treino aparecerem nas respostas |
| **Custo** | GenAI é computacionalmente cara; entender o custo por token é vital |

---

## 📝 Check-list de Termos para Decorar

- [ ] **Zero-shot Prompting:** Pedir algo sem dar exemplos
- [ ] **Few-shot Prompting:** Dar 2 ou 3 exemplos no prompt antes da pergunta
- [ ] **Chain-of-Thought:** Pedir para o modelo "pensar passo a passo"
- [ ] **Negative Prompt:** (Em imagens) Dizer o que você não quer que apareça

---

*Documentação atualizada em: 2026*
