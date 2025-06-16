# 🏀 ACB Basketball Player Performance Analysis

Multivariate analysis of ACB (Spanish Basketball League) player statistics to identify key performance indicators using PCA, MDS, MCA, and discriminant analysis techniques.

## 📌 Project Context

Developed for the *Data Analysis* course in the **Bachelor's Degree in Data Science and Engineering** at **Universitat Politècnica de Catalunya (UPC)**, this project investigates which statistics most impact player performance in Spain's top basketball league.

## 📊 Dataset

- **Source:** [Zenodo - Estadísticas de jugadores ACB](https://zenodo.org/record/4243039)
- **Scope:** 2020-2021 season (first 9 games)
- **Players:** 262 (after preprocessing)
- **Key Metric:** Performance Index Rating (PIR)
- **Classes:** 
  - *Poor* (PIR ≤ 5)
  - *Good* (5 < PIR ≤ 15)  
  - *Outstanding* (PIR > 15)

## 🔍 Methodology

### 1. Dimensionality Reduction
- **PCA:** Identified 3 principal components explaining 62.6% variance
  - PC1: Scoring metrics (*PPG, FGM, FGA*)
  - PC2: Defense/playmaking (*height, BLKF, TR, AST*)
- **MDS:** Compared Euclidean vs. Gower distances for performance separation

### 2. Categorical Analysis
- **MCA:** Revealed strong association between:
  - Player *license type* (EXT/JFL) and *performance*
  - *Position* and defensive contributions

### 3. Classification
- **LDA/QDA:** Achieved 96.5% CCR in performance prediction
- **Cluster Analysis:** Grouped teams by player performance profiles (k=3 optimal)

## 📈 Key Insights
1. Foreign players (*EXT license*) disproportionately dominate *Outstanding* class
2. Scoring metrics (*PPG, FGM*) explain most performance variance (PC1)
3. Defensive stats (*blocks, rebounds*) separate centers/power forwards (PC2)
4. Team affiliation (*club*) showed minimal performance correlation

## 🛠️ Tools & Libraries
- R 
- `FactoMineR` (PCA/MCA)
- `cluster` 
- `MASS` (LDA/QDA)
- `ggplot2` for visualization

## 👥 Authors
- Adrián Cerezuela Hernández
- Ramon Ventura Navarro

## 📚 Course  
**Data Analysis** (*Análisis de Datos*)  
Universitat Politècnica de Catalunya (UPC)  
