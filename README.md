# 📊 Análise de Vendas e Desempenho das Lojas – AluraStore Brasil

Projeto de **Análise de Dados** desenvolvido para gerar **insights acionáveis** sobre o desempenho comercial da rede **AluraStore Brasil**. A análise investiga padrões de vendas, popularidade de categorias, custos logísticos e performance financeira de cada loja, com o objetivo de **subsidiar uma decisão estratégica de venda de uma unidade**.

---

## 🎯 Objetivo do Projeto

Apoiar o **Sr. João**, proprietário da rede, na decisão de **qual loja vender** para reinvestir o capital em um novo negócio, utilizando dados como base para uma decisão racional, segura e estratégica.

---

## 📂 Fonte dos Dados

* Arquivos **CSV locais**
* Total de **9.435 vendas**, consolidadas a partir das quatro lojas da rede

---

## 🧹 Processamento e Transformação dos Dados

Os dados estavam bem estruturados, sem valores nulos ou duplicados relevantes. Ainda assim, foram aplicadas boas práticas para padronização, organização e ganho de eficiência analítica.

### 🔹 União de DataFrames

* Utilização do método `concat` para unir os DataFrames das quatro lojas
* Criação de uma coluna **ID da Loja** para identificar a origem dos dados

Essa abordagem facilita análises comparativas e escalabilidade do projeto.

### 🔹 Arredondamento de Valores

* Aplicação de `round(2)` em colunas financeiras (Preço e Frete)
* Padronização monetária e melhora da legibilidade de relatórios e gráficos

### 🔹 Conversão de Datas

* Conversão de colunas de data com `pd.to_datetime`
* Possibilitou análises temporais, agrupamentos mensais e identificação de sazonalidade

---

## 📊 Etapas da Análise

### 1️⃣ Faturamento Total por Loja

O faturamento é a principal métrica de desempenho financeiro.

| Loja   | Faturamento Total (R$) | Posição |
| ------ | ---------------------- | ------- |
| Loja 1 | 1.534.509,12           | 1º      |
| Loja 2 | 1.488.459,06           | 2º      |
| Loja 3 | 1.464.025,03           | 3º      |
| Loja 4 | 1.384.497,58           | 4º      |

**Conclusão:** A **Loja 4** apresenta o menor faturamento, com cerca de **R$ 150 mil a menos** que a Loja 1.

---

### 2️⃣ Faturamento por Categoria

A receita da rede é fortemente concentrada em categorias de maior valor agregado:

* **Eletrônicos:** 37,7%
* **Eletrodomésticos:** 30,1%
* **Móveis:** 17,2%

➡️ Essas três categorias representam **85% do faturamento total** da AluraStore.

**Observação:** Categorias como *Instrumentos Musicais* e *Esporte e Lazer* possuem participação marginal.

---

### 3️⃣ Sazonalidade de Vendas

A análise temporal revelou comportamento **cíclico do faturamento mensal**, com picos em períodos específicos, indicando sazonalidade possivelmente relacionada a datas promocionais e épocas festivas.

➡️ Essa informação é estratégica para decisões de **estoque, marketing e logística**.

---

### 4️⃣ Média de Avaliação dos Clientes

| Loja   | Média de Avaliação |
| ------ | ------------------ |
| Loja 3 | 4,05               |
| Loja 4 | 4,00               |
| Loja 2 | 4,01               |
| Loja 1 | 3,98               |

**Análise:**

* A Loja 1, apesar do maior faturamento, possui a **pior avaliação**.
* A Loja 4 mantém uma **boa percepção dos clientes**.

---

### 5️⃣ Custo Médio do Frete por Loja

| Loja   | Custo Médio do Frete (R$) |
| ------ | ------------------------- |
| Loja 1 | 34,69                     |
| Loja 2 | 33,17                     |
| Loja 3 | 32,58                     |
| Loja 4 | 31,28                     |

**Análise:** A Loja 4 apresenta o **frete mais barato**, enquanto a Loja 1 possui o maior custo logístico, impactando sua margem.

---

## 🧠 Cenários Estratégicos Avaliados

### ✅ Cenário 1 – Vender a Loja de Pior Desempenho (Recomendado)

**Recomendação:** Vender a **Loja 4**

**Justificativa:**

* Menor faturamento da rede
* Menor impacto na receita global
* Liberação de capital para novos investimentos

**Ponto de Atenção:** Boa avaliação e menor custo de frete

---

### ⚠️ Cenário 2 – Vender a Loja de Maior Dificuldade Operacional (Alternativa)

**Alternativa:** Vender a **Loja 1**

**Justificativa:**

* Maior faturamento (R$ 1,53M)
* Maior valor potencial de venda

**Ponto de Atenção:**

* Maior custo de frete
* Pior avaliação dos clientes

---

## 📌 Recomendação Final

A decisão **mais segura e racional** é **vender a Loja 4**.

### Motivos principais:

* Menor faturamento (R$ 1,38M)
* Menor impacto negativo na receita global
* Preservação das lojas mais rentáveis
* Otimização do portfólio
* Liberação de capital para expansão ou melhoria operacional

---

## 📑 Resumo Executivo

| Indicador             | Melhor Loja       | Pior Loja         |
| --------------------- | ----------------- | ----------------- |
| Faturamento Total     | Loja 1 (R$ 1,53M) | Loja 4 (R$ 1,38M) |
| Avaliação de Clientes | Loja 3 (4,05)     | Loja 1 (3,98)     |
| Custo Médio do Frete  | Loja 4 (R$ 31,28) | Loja 1 (R$ 34,69) |

---

## 🛠️ Tecnologias Utilizadas

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

---
