# 🧠 Machine Learning: Fundamentos

*Overfitting e Underfitting são os dois erros principais que um modelo de ML comete durante o aprendizado.*

---

## ⚖️ Balanceamento do Modelo

### 📉 Underfitting (Subajuste)

O Underfitting acontece quando o modelo é simples demais para entender os dados. É como o estudante que "não estudou o suficiente".

| Aspecto | Descrição |
| :--- | :--- |
| **Problema** | Modelo muito simples para capturar padrões nos dados |
| **Sintoma** | Alto erro tanto em treino quanto em dados novos |
| **Solução** | Aumentar complexidade, mais features, mais treino |

**Exemplo:** Tentar prever o preço de uma casa olhando apenas para o tamanho, ignorando bairro, idade e acabamento.

---

### 📈 Overfitting (Sobreajuste)

O Overfitting é o oposto: o modelo é detalhista demais. Ele decora os dados de treino, incluindo o "ruído" (erros aleatórios e detalhes irrelevantes).

| Aspecto | Descrição |
| :--- | :--- |
| **Problema** | Modelo memoriza dados de treino em vez de aprender padrões |
| **Sintoma** | Excelente em treino, falha em dados novos (falta de generalização) |
| **Solução** | Regularização, dropout, mais dados, menos complexidade |

**Exemplo:** Um robô que reconhece maçã só se for vermelha e sob luz específica - não reconhece maçã verde.

---

## 🎯 Resumo

| Problema | Treino | Dados Novos | Solução |
| :--- | :--- | :--- | :--- |
| **Underfitting** | Ruim | Ruim | Mais complexidade |
| **Overfitting** | Ótimo | Ruim | Regularização |

> [!TIP]
> O objetivo é encontrar o **ponto ideal** entre underfitting e overfitting - o modelo que generaliza bem para dados nunca vistos.

---

*Documentação atualizada em: 2026*
