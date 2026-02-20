# ☁️ AWS Documentation: SageMaker & Security

Este repositório centraliza o conhecimento técnico sobre os serviços de Machine Learning e as camadas de segurança da AWS.

---

## 🧠 Amazon SageMaker
*Plataforma completa para o ciclo de vida de Machine Learning.*

### 🛠️ Desenvolvimento e Preparação
| Serviço | Função | Descrição |
| :--- | :--- | :--- |
| **SageMaker Studio** | IDE Unificada | Interface visual única para escrever código, treinar e monitorar modelos. |
| **SageMaker Canvas** | No-Code ML | Interface "point-and-click" para criar previsões sem escrever código. |
| **Data Wrangler** | Prep de Dados | Agiliza a limpeza e normalização com centenas de conversões prontas. |
| **Feature Store** | Repositório | Armazena e compartilha variáveis (features) para treino e inferência. |
| **Ground Truth** | Rotulagem | Gerencia a rotulagem de dados brutos via força humana ou assistência por IA. |

### 📈 Treinamento e Otimização
* **SageMaker Automatic Model Tuning:** O motor de **AutoML** que testa combinações de hiperparâmetros para máxima precisão.
* **SageMaker JumpStart:** Hub de modelos pré-treinados, incluindo algoritmos prontos e **LLMs** de código aberto.
* **MLflow on SageMaker:** Gerenciamento do ciclo de vida e rastreamento de experimentos usando o framework open-source MLflow.

### 🚢 Implantação e Governança
* **Deployment & Inference:** Entrega de modelos via endpoints em tempo real, processamento em lote (batch) ou inferência assíncrona.
* **SageMaker Pipelines:** O motor de **CI/CD** específico para fluxos de trabalho de Machine Learning.
* **Model Registry:** Catálogo para gerenciar e aprovar versões de modelos para produção.
* **Role Manager:** Simplifica a gestão de permissões (IAM) focada em funções de ML.

### 🔍 Monitoramento e Ética
> [!IMPORTANT]
> A transparência e o monitoramento contínuo garantem que o modelo permaneça confiável após o deploy.

* **SageMaker Clarify:** Detecta vieses e fornece explicabilidade (quais variáveis influenciam o resultado).
* **SageMaker Model Monitor:** Alerta sobre a queda de qualidade ou desvio (*drift*) dos dados em produção.
* **SageMaker Model Cards:** Documentação automática para fins de auditoria e registro de métricas.
* **SageMaker Model Dashboard:** Painel central para monitorar a saúde de todos os modelos implantados.

---
