# Customer Segmentation Using K-Means

A clean, reproducible project that segments customers into meaningful groups using **unsupervised learning**.  
This repository contains a Jupyter notebook that loads the classic **Mall Customers** dataset, engineers features, and applies **K-Means** clustering to discover distinct customer personas.

---

## 🚀 What you get
- End‑to‑end notebook: `/CustomerSegmentation.ipynb`
- Dataset reference: `Mall_Customers.csv` (public toy dataset)
- Features used: `Age, Annual Income (k$), Spending Score (1-100)`
- Algorithm: `K-Means`
- Model selection aid: `Elbow Method`
- Visualizations: cluster scatter plots, elbow curve

> Why this matters: customer segmentation enables **targeted marketing, tailored offers, and better retention** without needing labeled data.

---

## 🧱 Project Structure
```
.
├── CustomerSegmentation.ipynb
├── Mall_Customers.csv                  # expected dataset (put in repo root or update path in notebook)
└── README.md
```

---

## 📊 Dataset
- **Name:** Mall Customers (commonly available on Kaggle/UCI mirrors)  
- **Target:** Unsupervised (no label)  
- **Core features in this project:** Age, Annual Income (k$), Spending Score (1-100)  
- **Rows/Columns:** Depends on the specific CSV you use (typical version has ~200 rows).

> If your CSV is in a different location, update the path in the notebook where `pd.read_csv(...)` is called.

---

## 🧪 Methodology (short)
1. Load and preview data (`pandas`).
2. Basic EDA and sanity checks (missing values, distributions).
3. Optional scaling (not strictly needed for the included features).
4. Determine a good `k` using the **Elbow method**.
5. Fit **K‑Means** with `k = 4`.
6. Visualize clusters and interpret actionable segments.

Typical business‑friendly segment names for this dataset:
- **High-Value Regulars** (high income & spending)
- **Careful Spenders** (high income, moderate/low spending)
- **Budget Shoppers** (lower income, variable spending)
- **Occasional Visitors** (lower engagement patterns)

*(Your exact segments may differ; always validate with domain context.)*

---
**Cloning the Repository**

```bash
git clone https://github.com/Prasad-Arugollu/CustomerSegmentation-ML.git
```

## 🔧 Setup
### 1) Environment
```bash
# Python 3.9+ recommended
pip install -r requirements.txt
```
If you don't use a `requirements.txt`, install the essentials manually:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly
```

### 2) Run the notebook
```bash
jupyter notebook CustomerSegmentation.ipynb
```
Or with JupyterLab:
```bash
jupyter lab CustomerSegmentation.ipynb
```

---

## 📝 Repro tips
- Ensure `Mall_Customers.csv` is present at the path used in the notebook.
- Random seeds (`random_state`) may be set for repeatability.
- K‑Means assumes roughly spherical clusters; try **GMM/DBSCAN** if shapes look non‑convex.

---

## 📈 Evaluation & sanity checks
Because this is unsupervised, use **internal** validation:
- **Elbow method** for inertia drop‑off.
- (**Optional**) **Silhouette score** if you add it.
- Always validate clusters against **business KPIs** (e.g., conversion, AOV, churn proxy).

---

## 🧩 Extending the project
- Add **RFM features** (Recency, Frequency, Monetary).
- Try **feature scaling** (StandardScaler/MinMaxScaler) and compare results.
- Compare with **Hierarchical**, **DBSCAN**, or **GMM**.
- Add **interactive Plotly** visualizations and segment profiling dashboards.
- Productionize: persist clusters with joblib and score new customers.

---


---

## 🙋 FAQ
**Q: My elbow plot is ambiguous—how do I choose k?**  
A: Try 3–8 clusters, inspect **silhouette scores**, and prefer the smallest `k` that yields **clear business separation**.

**Q: Do I need scaling?**  
A: If features are on very different ranges, yes. For `Age`, `Annual Income (k$)`, and `Spending Score (1–100)`, scaling is optional but worth trying.

---

