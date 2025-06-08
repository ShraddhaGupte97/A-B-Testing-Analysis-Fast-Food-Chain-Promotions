# 🧪 A/B Testing Analysis: Fast-Food Chain Promotions

📂 Dataset Source: This dataset is publicly available on [Kaggle](https://www.kaggle.com/datasets/chebotinaa/fast-food-marketing-campaign-ab-test/data), and has been used here for educational and portfolio purposes.

A fast-food chain introduced a new menu item and tested three different promotional strategies (Promotion 1, 2, and 3) across different store locations. Each store ran one of these promotions for four weeks, and weekly sales data was collected.

The goal is to determine which promotion led to the highest sales, so the company can deploy it chain-wide.

---

## 📊 Analysis Summary

- **Statistical Method**: One-way ANOVA (with assumptions tested)
- **Post-hoc Testing**: Tukey's HSD to identify specific group differences
- **Robustness Check**: Kruskal-Wallis test (non-parametric)

---

## ✅ Key Findings

- ANOVA p-value: **0.0037** → at least one promotion performs differently
- **Tukey HSD**:
  - Promotion 1 vs 2 → significant (p = 0.004)
  - Promotion 2 vs 3 → significant (p = 0.037)
  - Promotion 1 vs 3 → not significant
- **Kruskal-Wallis p-value**: 0.00017 → supports ANOVA conclusion despite non-normal data

---

## 🎯 Business Recommendation

- **Promotion 1** performs significantly better than **Promotion 3**
- Promotion 1 is **recommended** for rollout across stores as it outperforms both Promotion 2 and Promotion 3 and has highest weekly sales
- Optionally, test further between Promotion 1 and Promotion 2 to explore edge cases like specific store types, regions, or longer-term effects using a **separate dataset or experimental setup** to ensure no prior exposure bias. This would ideally involve rerunning the test by randomly assigning Promotions 1 and 2 across a new set of stores and tracking performance independently of the current campaign.

---

## 📂 Repository Structure

```
fastfood-promotion-abtest/
├── data/
│ └── WA_Marketing-Campaign.csv
├── notebooks/
│ └── ab_test_analysis.ipynb
├── visuals/
│ └── [saved plots].png
├── requirements.txt
└── README.md
```

## 📦 How to Run

1. Clone the repository
2. Install dependencies using: 

```python
pip install -r requirements.txt
```

3. Open and run `notebooks/ab_test_analysis.ipynb`

---

## 📈 Dependencies

See `requirements.txt` for the complete list.

## 👩‍💻 Author

**Shraddha Gupte**
*Data Scientist | Machine Learning | NLP | LLM | Product Strategy*
🔗 [LinkedIn](https://www.linkedin.com/in/shraddha-gupte/) | 🌐 [GitHub](https://github.com/ShraddhaGupte97)
