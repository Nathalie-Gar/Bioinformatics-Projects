# Antibiotic Resistance in *E. coli* – Gene Expression Classification

This project uses microarray data (GSE59408) from *E. coli* strains evolved under 10 antibiotics to explore whether gene expression patterns can be used to classify antibiotic resistance. The project is split into **two parts**:

---

## 🔹 Part I – Exploratory Data Analysis (EDA)
The first part focuses on **unsupervised analysis** to see whether resistant strains cluster naturally by antibiotic type or by mechanism of action (MOA).  
Methods used:
- Variance-based gene filtering (top 2000 most variable genes)  
- PCA with scree plots and scatterplots  
- UMAP for nonlinear visualization  
- Silhouette scores to measure cluster separability  
- Heatmaps comparing average expression profiles by **drug** vs. **MOA**  

**Key findings (Part I):**
- At the **drug level**, clustering was weak with heavy overlap (silhouette ≈ –0.12).  
- At the **MOA level**, structure was slightly clearer (silhouette ≈ 0), especially for cephalosporins and fluoroquinolones.  
- Heatmaps supported this: drug-level averages were noisy, while MOA-level averages produced coherent transcriptional signatures.  
- Overall: **mechanism of action explains more variance than drug identity, but unsupervised methods alone cannot classify the groups well.**

---

## 🔹 Part II – Machine Learning (in progress)
The second part will focus on **supervised classification models** using PCA-reduced features:
- Train baseline models (e.g., logistic regression) at both the drug and MOA level  
- Use cross-validation to assess predictive power  
- Compare whether ML can separate antibiotics more effectively than unsupervised methods  

---

## 📊 Dataset
- **Accession:** [GSE59408](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE59408)  
- **Samples:** 40 resistant strains (4 per drug × 10 drugs) + 2 parent controls  
- **Design:** Parallel laboratory evolution under single-drug selection, followed by transcriptome profiling  

---

## 📚 References
- GEO Accession: [GSE59408](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE59408)  
- McInnes, L., Healy, J., & Melville, J. (2018). UMAP: Uniform Manifold Approximation and Projection for Dimension Reduction. *arXiv:1802.03426*  
- Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python. *JMLR, 12*, 2825–2830  

---
