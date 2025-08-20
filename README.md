	<<<<<<< HEAD
# Indian Stocks Clustering Project

This project explores **unsupervised learning techniques** to group Indian companies based on financial and stock market indicators. The goal is to identify natural clusters among companies, which may represent similar business/financial characteristics and provide insights for investors, analysts, or portfolio managers.

---

## 📂 Dataset
- **File:** `StockDataWithoutClusters_v2.csv`
- **Rows:** 1,225 companies
- **Columns (12 features):**
  - Company, Sector
  - Price, Market Cap, Free Float Market Cap %, 6m ADV
  - RoE %, RoCE %, EBIT Margin %, EPS, PAT %, Stock Return %

### Feature Engineering
Additional features were created to enhance clustering:
- **PE_Ratio:** Price / EPS
- **EPS_to_Price:** EPS / Price
- **RoE_minus_RoCE:** RoE - RoCE
- **PAT_to_EBIT:** PAT % / EBIT Margin %

---

## 📓 Notebook Workflow (`indian_stocks_clustering_project_1.ipynb`)

### 1. Preprocessing
- Missing values handling
- Standardization using `StandardScaler`

### 2. Dimensionality Reduction
Three methods applied for better cluster separation & visualization:
- **PCA** (Principal Component Analysis)
- **t-SNE** (t-Distributed Stochastic Neighbor Embedding)
- **UMAP** (Uniform Manifold Approximation & Projection)

### 3. Clustering Algorithms
- **K-Means**
- **Agglomerative Clustering** (Hierarchical)
- **DBSCAN**

### 4. Evaluation Metrics
- **Silhouette Score** → Cluster cohesion vs separation
- **Davies-Bouldin Index** → Lower is better
- **Calinski-Harabasz Score** → Higher is better

### 5. Visualization
- 2D scatter plots using PCA, t-SNE, and UMAP projections
- Color-coded clusters

---

## 🚀 How to Run
1. Clone the repository and navigate to the project folder:
   ```bash
   git clone https://github.com/d-binu163/indian_stocks_clustering_project-1.git
   cd indian_stocks_clustering_project-1
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook:
   ```bash
   jupyter notebook indian_stocks_clustering_project_1.ipynb
   ```

---

## 📊 Results & Insights
- Different dimensionality reduction techniques reveal varying cluster shapes.
- K-Means generally produced stable clusters.
- UMAP + K-Means gave the most interpretable groupings.
- Sectors like **Auto, Banks, and IT** showed distinct separations, while others overlapped.

---

## 📌 Future Work
- Add sector-wise cluster validation.
- Apply **Gaussian Mixture Models (GMM)** for soft clustering.
- Compare clusters with actual stock performance over time.
- Build a dashboard (e.g., in **Power BI** or **Plotly Dash**) for interactive exploration.

---

## 🛠️ Tech Stack
- **Python** (pandas, numpy, matplotlib, seaborn)
- **Scikit-learn** (clustering, scaling, metrics)
- **UMAP-learn**, **t-SNE**
- **Jupyter Notebook**

---

## 📖 License
This project is for educational purposes. Please check dataset source before commercial use.
