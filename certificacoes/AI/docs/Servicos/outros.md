
## 🛡️ AWS Security Services and More
*Identidade, Conformidade e Governança.*



### 🔑 Identidade e Acesso (IAM)
* **IAM (Identity and Access Management):** O coração da segurança AWS; controla quem acessa o quê.
* **IAM Groups:** Coleção de usuários para aplicação de permissões em massa.
* **IAM Policies:** Documentos **JSON** que definem explicitamente permissões de acesso.
* **IAM Roles:** Identidades para serviços (EC2, Lambda) assumirem permissões temporárias.




### 📋 Segurança, Auditoria e Conformidade
| Serviço | Propósito |
| :--- | :--- |
| **Amazon Macie** | Usa ML para descobrir dados sensíveis (CPF, cartões) no S3. |
| **AWS Config** | Monitora configurações e avalia a conformidade dos recursos. |
| **Amazon Inspector** | Scanner automático de vulnerabilidades em instâncias e containers. |
| **AWS CloudTrail** | Log de auditoria: registra todas as chamadas de API (quem, quando, onde). |
| **AWS Artifact** | Portal para relatórios de conformidade (ISO, PCI) e contratos. |
| **Audit Manager** | Simplifica a gestão de riscos e auditoria contínua. |
| **Trusted Advisor** | Consultor para reduzir custos e aumentar a performance/segurança. |

---

## 💻 Computação e Armazenamento Core

### 🗄️ Amazon S3 (Simple Storage Service)
Armazenamento de objetos altamente escalável, seguro e durável.

#### **S3 Storage Classes**
| Storage Class | Uso Ideal | Tempo de Recuperação |
| :--- | :--- | :--- |
| **S3 Standard** | Acesso frequente e dados ativos. | Milissegundos |
| **S3 Intelligent-Tiering** | Dados com padrões de acesso desconhecidos/variáveis. | Milissegundos |
| **S3 Standard-IA** | Acesso infrequente, mas precisa de acesso rápido. | Milissegundos |
| **S3 One Zone-IA** | Dados não críticos em apenas uma zona (mais barato). | Milissegundos |
| **S3 Glacier Instant** | Arquivos raramente acessados com recuperação imediata. | Milissegundos |
| **S3 Glacier Flexible** | Backups tradicionais com custo baixo. | Minutos a Horas |
| **S3 Glacier Deep Archive** | Retenção de longo prazo (anos) - Classe mais barata. | Até 12 Horas |

### ⚡ Computação
* **Amazon EC2:** Servidores virtuais na nuvem com controle total do Sistema Operacional.
* **Amazon Lambda:** Serviço **Serverless** que executa código em resposta a eventos (pague pelo uso).

---

## 🌐 Networking e Conectividade Privada
*Mantendo o tráfego fora da internet pública.*

* **VPC Endpoint:** Conecta sua rede privada aos serviços AWS de forma isolada.
* **AWS PrivateLink:** Tecnologia de conectividade privada entre VPCs e redes on-premises.
* **S3 Gateway Endpoint:** Permite acesso gratuito ao S3 para instâncias em redes privadas sem NAT Gateway.

---
*Documentação atualizada em: 2026*