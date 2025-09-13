#  Product Recommender System

## 📝 Introduction

This project aims to develop an **association rule-based recommender system**, using customer purchase transactions from a supermarket. The goal is to identify consumption patterns that allow us to recommend products frequently bought together.

We use the **Apriori** and **FP-Growth** algorithms to find **frequent itemsets** and **generate association rules**, filtered based on metrics such as **support**, **confidence**, and **lift**.

---

## 📊 Data

The data is contained in the `transacoes.csv` file, which consists of **lists of products purchased by customers in a single transaction**. Each line represents an individual transaction.

### Steps performed:
- Reading and cleaning transactions (removal of spaces and quotes)
- Transformation to transactional format (one-hot encoding with `TransactionEncoder`)
- Generation of frequent itemsets with `Apriori` and `FP-Growth`
- Extraction of rules with `association_rules()`
- Application of filters based on support, confidence, and lift

---

## 🤖 Modeling with Apriori and FP-Growth

Modeling was done using two popular algorithms for association pattern analysis:

- **Apriori**
- **FP-Growth**

The main parameters used were:

- Minimum support: **1%**
- Minimum confidence: **20%**
- Minimum lift: **1.5**
- Minimum size of the antecedent (LHS): **1**

The rules generated were ordered by **lift** to highlight the most relevant ones.

---

## 🔍 Examples of Generated Rules

| Antecedent         | Consequent       | Confidence | Lift |
|--------------------|------------------|------------|------|
| [milk]             | [coffee]         | 0.45       | 1.8  |
| [bread, butter]    | [milk]           | 0.37       | 1.7  |
| [soda]             | [chips]          | 0.29       | 1.6  |

These rules indicate products that frequently appear together in transactions and can be used for targeted recommendations.

## 💼 Estimated Financial Impact

This script estimates the potential financial impact of a recommender system, considering parameters defined by the business.

**Parameters**
- Average profit per transaction: R$ 5.00
- Estimated increase in conversion rate: 10%
- Total transactions: 500

**Calculations**
- Additional transactions = 500 × 0.10 = 50
- Financial impact = 50 × R$ 5.00 = R$ 250.00

**Results**
- Estimated additional transactions: 50
- Estimated financial impact: R$ 250.00

This gain can be even greater with continuous personalization and real-time integration of recommendations.

---

## 📈 Visualizations

- Table with **frequent itemsets** found
- Sorted table with **association rules filtered** by lift
- (Optional) Bar charts of the most frequent items or common pairs

---

## 🛠️ Tools Used

- **Python** – Main programming language
- **Pandas** – Data manipulation
- **MLxtend** – Apriori, FP-Growth algorithms and rule generation
- **Google Colab** – Development environment

---

## ✅ Results

- Various **association rules between products** were generated.
- The system can provide **automatic recommendations** based on purchase history.
- The strongest rules have **high lift** and can serve as a basis for promotional actions or suggestions in e-commerce.

---

## 🧠 Conclusions

The project demonstrates how **frequent pattern mining** techniques can:

- Identify products with strong purchase correlation
- **Support cross-selling strategies**
- Improve personalization in recommendation platforms

---

## 🔄 Next Steps

- Implement real-time recommendations based on the user's cart.
- Integrate with customer profile data for personalized recommendations.
- Test rules in an A/B Testing system to measure impact on sales.

---

🧑‍💻 **Author and Contact**

Higor Roberto Coutinho Caetano  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com
