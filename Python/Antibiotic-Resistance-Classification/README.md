# Antibiotic Resistance in *E. coli* – Part I: Exploratory Analysis

This project explores gene expression patterns in *E. coli* strains evolved under antibiotic pressure (GSE59408).  
The goal is to see whether expression profiles naturally separate by **antibiotic type** or by **mechanism of action (MOA)**, and to prepare the data for supervised machine learning in Part II.

---

## 📊 Dataset
- **Accession:** [GSE59408](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE59408) (microarray expression data)  
- **Samples:** 40 resistant strains (4 replicates × 10 antibiotics) + 2 parent controls  
- **Design:** Parallel laboratory evolution under single-drug selection, transcriptomes profiled post-evolution  

---

## 🧪 Methods (Part I – EDA)
- Variance-based filtering to keep top 2000 most variable genes  
- Standardization with `StandardScaler`  
- Dimensionality reduction:
  - PCA with scree plots, PC1–PC3 scatterplots  
  - UMAP (various parameters) for nonlinear visualization  
- Cluster evaluation with **silhouette scores**  
- Heatmaps of top-variance genes (averaged by drug and by MOA)

---

## 🔎 Results (Part I)
- **PCA & UMAP:**  
  - Antibiotic-level clustering was weak with major overlap  
  - MOA-level grouping showed clearer structure, especially for cephalosporins and fluoroquinolones  
- **Silhouette scores:**  
  - Drug-level ≈ –0.12 → poor separation  
  - MOA-level ≈ –0.00 → weak but improved  
- **Heatmaps:**  
  - By drug → noisy and overlapping  
  - By MOA → cleaner signatures, cephalosporins & fluoroquinolones clustered tightly  

---

## 🚀 Next Steps (Part II – Machine Learning)
- Use PCA-reduced features to train supervised classifiers  
- Compare performance on **drug-level** vs **MOA-level** prediction  
- Evaluate models with cross-validation  

---

## 📚 References
- GEO Accession: [GSE59408](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE59408)  
- McInnes, L., Healy, J., & Melville, J. (2018). UMAP: Uniform Manifold Approximation and Projection for Dimension Reduction. *arXiv:1802.03426*  
- Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python. *JMLR, 12*, 2825–2830  

---
