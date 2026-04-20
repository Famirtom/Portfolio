# Mental Health Clustering in the Tech Sector

This project applies unsupervised machine learning to OSMI (Open Sourcing Mental Illness) survey data (2017–2022) to identify distinct mental health profiles among tech workers.

## Objective

Identify recurring patterns in how tech workers experience and perceive mental health, using clustering on survey responses — without relying on demographic variables like gender.

## Dataset

- Source: OSMI Mental Health in Tech Survey (2017–2022)
- 2,000 respondents across 6 survey years
- Surveys harmonised to extract 56 common questions across all years

## Method

1. **Data cleaning & harmonisation** — merging 6 yearly surveys into one consistent dataset
2. **Preprocessing** — ordinal encoding, missing value imputation, standardisation
3. **Dimensionality reduction** — PCA + UMAP for visualisation and feature compression
4. **Clustering** — K-Means with silhouette score selection (k=3, gender excluded)
5. **Analysis** — cluster profiling and distribution across COVID periods (Pre / During / Post)

## Results

Three clusters were identified:

- **Cluster 1 — Lower support and openness**: respondents less likely to perceive organisational support and more reluctant to discuss mental health at work
- **Cluster 2 — Higher awareness and engagement**: respondents who report more mental health difficulties but also show higher awareness and openness
- **Cluster 0 — Intermediate profile**: respondents with moderate levels of awareness and support, neither clearly positive nor negative

The cluster distribution shifts across COVID periods, with Cluster 0 (intermediate) growing during and after COVID, suggesting a broader shift in how tech workers relate to mental health in the workplace.

## Tech Stack

- Python, Pandas, NumPy
- Scikit-learn (KMeans, PCA, StandardScaler)
- UMAP
- Matplotlib, Seaborn
