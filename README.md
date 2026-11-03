

# Financial Inclusion under PMJDY: Clustering Indian States Based on Account Uptake and Usage Indicators

**Author:** Nancy Singh  
**Course:** B.Sc. (Hons.) Computer Science  
**Institution:** Ramanujan College, University of Delhi  
**Roll Number:** 24570042  
**Email:** singhnancy6285@gmail.com  

---

## 1. Project Overview

Financial inclusion is an important part of India's economic development. The Pradhan Mantri Jan-Dhan Yojana (PMJDY) was launched to provide access to financial services, including bank accounts, savings facilities, and RuPay debit cards, to individuals across the country.

This project uses **Machine Learning (K-Means Clustering)** to group Indian States and Union Territories based on selected PMJDY financial inclusion indicators.

The objective is to identify patterns and similarities among states in terms of account uptake, rural participation, average account balance, and RuPay card distribution.

## 2. Research Objectives

- To study the distribution of PMJDY beneficiaries across Indian States and Union Territories.
- To examine rural and urban participation in financial inclusion.
- To analyse average balance per beneficiary.
- To examine RuPay card distribution as an indicator of card coverage.
- To apply K-Means clustering to group states with similar financial inclusion characteristics.
- To interpret the resulting clusters and identify regional patterns.

## 3. Dataset Description

The dataset contains state-wise PMJDY indicators used for the clustering analysis.

The main indicators include:

- State/Union Territory
- Total beneficiaries
- Rural beneficiaries
- Urban beneficiaries
- Amount deposited
- RuPay cards issued

### Derived Features

The following features were calculated for the analysis:

1. **Rural Beneficiary Share (%)**

   Rural beneficiaries as a percentage of total beneficiaries.

2. **Average Balance per Beneficiary (₹)**

   Total amount deposited divided by total beneficiaries.

3. **RuPay Cards per 100 Beneficiaries**

   RuPay cards issued per 100 beneficiaries. This represents card distribution or coverage, not actual card activation or transaction usage.

4. **Log Total Beneficiaries**

   Log-transformed beneficiary count to reduce the effect of differences in scale.

## 4. Methodology

The project follows these steps:

1. Data loading and inspection.
2. Data cleaning and preprocessing.
3. Feature engineering to calculate relevant financial inclusion indicators.
4. Feature scaling using `StandardScaler`.
5. Application of K-Means clustering.
6. Comparison of different cluster values using inertia and silhouette score.
7. Selection of three clusters (`K = 3`) for the final analysis.
8. Visualisation and interpretation of cluster results.

### Model Selection

Different values of K were evaluated using inertia and silhouette score.

| Number of Clusters (K) | Inertia | Silhouette Score |
|---|---:|---:|
| 2 | 103.010 | 0.278 |
| 3 | 79.081 | 0.315 |
| 4 | 57.125 | 0.283 |
| 5 | 46.647 | 0.297 |
| 6 | 39.086 | 0.240 |

K = 3 achieved the highest silhouette score among the tested values and was selected for the final clustering analysis.

## 5. Clustering Results

The K-Means model grouped 36 States and Union Territories into three clusters.

| Cluster | Number of States/UTs | Percentage |
|---|---:|---:|
| Cluster 0 | 14 | 38.89% |
| Cluster 1 | 2 | 5.56% |
| Cluster 2 | 20 | 55.56% |
| **Total** | **36** | **100%** |

### Cluster Profiles

| Indicator | Cluster 0 | Cluster 1 | Cluster 2 |
|---|---:|---:|---:|
| Number of States/UTs | 14 | 2 | 20 |
| Average Beneficiaries | 1,174,169.07 | 3,771,428.50 | 28,616,435.75 |
| Average Rural Share (%) | 80.81 | 11.98 | 75.60 |
| Average Balance (₹) | 8,094.40 | 6,070.42 | 5,242.76 |
| RuPay Indicator | 64.14 | 72.97 | 70.12 |

### Interpretation

- **Cluster 0:** Contains 14 States/UTs and has a high average rural beneficiary share and the highest average balance per beneficiary among the three clusters.
- **Cluster 1:** Contains 2 States/UTs and has a comparatively low rural beneficiary share. It includes Chandigarh and Delhi.
- **Cluster 2:** Contains 20 States/UTs and has the highest average beneficiary count, along with a high rural beneficiary share.

These clusters highlight differences in the scale and characteristics of financial inclusion across Indian States and Union Territories.

## 6. Visual Results

### 6.1 K-Means Clustering of Indian States

![K-Means Clusters](PMJDY_KMeans_Clusters%20%288%29.png)

### 6.2 Average Balance per Beneficiary by Cluster

![Average Balance by Cluster](PMJDY_Balance_by_Cluster%20%288%29.png)

### 6.3 Rural Beneficiary Share by Cluster

![Rural Share by Cluster](PMJDY_Rural_Share_by_Cluster%20%288%29.png)

## 7. Repository Structure

The repository contains the following files:

| File Name | Description |
|---|---|
| `PMJDY_Financial_Inclusion (2).ipynb` | Jupyter Notebook containing the complete analysis |
| `PMJDY_Statewise_Cleaned (9).csv` | Cleaned state-wise dataset |
| `PMJDY_Clustered_States (8).csv` | State-wise cluster assignments |
| `PMJDY_Cluster_Profiles (9).csv` | Summary statistics of the three clusters |
| `PMJDY_KMeans_Clusters (8).png` | K-Means cluster visualisation |
| `PMJDY_Balance_by_Cluster (8).png` | Average balance comparison |
| `PMJDY_Rural_Share_by_Cluster (8).png` | Rural beneficiary share comparison |

## 8. Tools and Technologies

- **Python**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualisation
- **Seaborn** – Statistical visualisation
- **Scikit-learn** – StandardScaler and K-Means clustering
- **Jupyter Notebook** – Development and analysis environment
- **GitHub** – Project version control and documentation

## 9. Limitations

- The analysis is based on the indicators available in the dataset.
- K-Means clustering is sensitive to feature scaling and the selected number of clusters.
- The silhouette score of 0.315 indicates modest separation between clusters; therefore, the results should be interpreted as exploratory patterns.
- RuPay card distribution does not necessarily indicate card activation or actual transaction activity.
- The analysis identifies associations and patterns; it does not establish causal relationships.

## 10. Conclusion

This project applies K-Means clustering to explore differences in financial inclusion across Indian States and Union Territories under PMJDY.

The analysis identifies three groups with different characteristics in terms of beneficiary scale, rural participation, average balance, and RuPay card distribution.

The findings demonstrate how unsupervised machine learning can be used to explore regional patterns in financial inclusion and support further data-driven research.

## 11. Academic Use

This project has been developed as part of academic work for the B.Sc. (Hons.) Computer Science programme at Ramanujan College, University of Delhi.

## 12. Research Paper

"C:\Users\Shivani Singh\Downloads\PMJDY_Research_Paper_Nancy_Singh.docx"

## 13. Author

## Nancy singh
B.Sc(H) Computer Science 
Ramanujan College,University of Delhi

## Project: Machine Learning
## Supervisor: Mr.Nikhil Kumar
## Problem No:- 45




