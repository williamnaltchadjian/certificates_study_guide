# Projeto: AWS Certification Study Guide (AI/ML)

Este repositório contém um guia de estudos abrangente para as certificações da AWS focadas em IA e Machine Learning. O projeto utiliza **MkDocs** para gerar um site estático de documentação com navegação estruturada por domínios de conhecimento e serviços.

## 🛠️ Tecnologias e Ferramentas
- **MkDocs**: Gerador de sites estáticos para documentação técnica.
- **Material for MkDocs**: Tema visual com suporte a busca, modo escuro e componentes avançados.
- **Python 3.11+**: Ambiente base para execução das ferramentas de build.
- **Plugins MkDocs**: Minificação, suporte a diagramas Mermaid, busca semântica e gestão de tags.

## 📂 Estrutura do Diretório
- `mkdocs.yml`: Arquivo central de configuração (temas, plugins e navegação).
- `requirements.txt`: Lista de dependências Python necessárias.
- `.agents/workflows/aistudy.md`: Instruções específicas para agentes de IA que colaboram neste projeto.
- `docs/`: Contém todo o conteúdo em Markdown.
    - `Dominios/`: Detalhamento dos tópicos por domínios da prova (Fundamentos, GenAI, Prompt Engineering, Responsabilidade, etc.).
    - `Servicos/`: Documentação específica de serviços AWS (ex: Amazon SageMaker).
    - `resumo.md`: Visão geral estratégica e tabelas comparativas de conceitos de ML.

## 🚀 Comandos Principais
Para trabalhar neste projeto, utilize os comandos abaixo no terminal:

- **Instalar dependências**:
  ```bash
  pip install -r requirements.txt
  ```
- **Executar servidor local** (com live-reload):
  ```bash
  mkdocs serve
  ```
- **Gerar build estático**:
  ```bash
  mkdocs build
  ```

## 📝 Convenções de Desenvolvimento
- **Formatação**: Todo o conteúdo deve seguir o padrão de tabelas e blocos de nota (`!!! tip`, `!!! warning`) do MkDocs Material.
- **Linguagem**: O conteúdo principal está em Português (Brasil).
- **Agentes de IA**: Ao editar arquivos, consulte `.agents/workflows/aistudy.md` para garantir que a formatação e os padrões de resumo estratégico sejam mantidos.
- **Imagens e Ativos**: Devem ser referenciados localmente ou via links estáveis, preferencialmente usando a extensão `attr_list` para redimensionamento se necessário.

## 🎯 Foco do Conteúdo
O guia prioriza "Dicas de Prova" e "Resumos Estratégicos", focando em:
1. Diferenças conceituais (AI vs ML vs DL vs GenAI).
2. Métricas de avaliação (Precision, Recall, F1, ROUGE, BLEU).
3. Técnicas de otimização (Pruning, Quantization, Distillation).
4. Prompt Engineering e RAG (Retrieval-Augmented Generation).
5. Governança e IA Responsável na AWS.
