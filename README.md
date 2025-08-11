# Projeto 3: Sistema de Recomendação de Produtos

## 📝 Introdução

Este projeto tem como objetivo desenvolver um **sistema de recomendação baseado em regras de associação**, utilizando transações de compra de clientes em um supermercado. A proposta é identificar padrões de consumo que permitam recomendar produtos frequentemente comprados juntos.

Utilizamos os algoritmos **Apriori** e **FP-Growth** para encontrar **conjuntos frequentes de itens** e **gerar regras de associação**, filtradas com base em métricas como **suporte**, **confiança** e **lift**.

---

## 📊 Dados

Os dados estão contidos no arquivo `transacoes.csv`, composto por **listas de produtos comprados por clientes em uma única transação**. Cada linha representa uma transação individual.

### Etapas realizadas:
- Leitura e limpeza das transações (remoção de espaços e aspas)  
- Transformação para o formato transacional (one-hot encoding com `TransactionEncoder`)  
- Geração de conjuntos frequentes com `Apriori` e `FP-Growth`  
- Extração de regras com `association_rules()`  
- Aplicação de filtros com base em suporte, confiança e lift

---

## 🤖 Modelagem com Apriori e FP-Growth

A modelagem foi feita utilizando dois algoritmos populares para análise de padrões de associação:

- **Apriori**  
- **FP-Growth**

Os parâmetros principais utilizados foram:

- Suporte mínimo: **1%**  
- Confiança mínima: **20%**  
- Lift mínimo: **1.5**  
- Tamanho mínimo do antecedente (LHS): **1**

As regras geradas foram ordenadas por **lift** para destacar as mais relevantes.

---

## 🔍 Exemplos de Regras Geradas

| Antecedente         | Consequente       | Confiança | Lift |
|---------------------|-------------------|-----------|------|
| [leite]             | [café]            | 0.45      | 1.8  |
| [pão, manteiga]     | [leite]           | 0.37      | 1.7  |
| [refrigerante]      | [salgadinho]      | 0.29      | 1.6  |

Essas regras indicam produtos que frequentemente aparecem juntos nas transações e podem ser utilizados para recomendações direcionadas.

## 💼 Impacto Financeiro Estimado

Este script estima o impacto financeiro potencial de um sistema de recomendação, considerando parâmetros definidos pelo negócio.

**Parâmetros**
- Lucro médio por transação: R$ 5,00  
- Aumento estimado na taxa de conversão: 10%  
- Total de transações: 500

**Cálculos**
- Transações adicionais = 500 × 0,10 = 50  
- Impacto financeiro = 50 × R$ 5,00 = R$ 250,00

**Resultados**
- Transações adicionais estimadas: 50  
- Impacto financeiro estimado: R$ 250,00

Este ganho pode ser ainda maior com a personalização contínua e integração em tempo real das recomendações.

---

## 📈 Visualizações

- Tabela com os **conjuntos frequentes** encontrados  
- Tabela ordenada com as **regras de associação filtradas** por lift  
- (Opcional) Gráficos de barras com os itens mais frequentes ou pares mais comuns

---

## 🛠️ Ferramentas Utilizadas

- **Python** – Linguagem principal  
- **Pandas** – Manipulação de dados  
- **MLxtend** – Algoritmos Apriori, FP-Growth e geração de regras  
- **Google Colab** – Ambiente de desenvolvimento  

---

## ✅ Resultados

- Foram geradas diversas **regras de associação entre produtos**.  
- O sistema é capaz de indicar **recomendações automáticas** com base no histórico de compras.  
- As regras mais fortes têm **alto lift** e podem servir como base para ações promocionais ou sugestões no e-commerce.

---

## 🧠 Conclusões

O projeto demonstra como técnicas de **mineração de padrões frequentes** podem:

- Identificar produtos com forte correlação de compra  
- **Apoiar estratégias de venda cruzada (cross-selling)**  
- Melhorar a personalização em plataformas de recomendação  

---

## 🔄 Próximos Passos

- Implementar recomendações em tempo real com base no carrinho do usuário.
- Integrar com dados de perfil do cliente para recomendações personalizadas.
- Testar regras em um sistema de A/B Testing para medir impacto em vendas.



---

🧑‍💻 **Autor e Contato**

Higor Roberto Coutinho Caetano  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com
