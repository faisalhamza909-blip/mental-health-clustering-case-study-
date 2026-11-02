# Mental Health in Tech: Clustering Employees for an HR Prevention Programme

Case study for the IU course **DLBDSMLUSL01 – Machine Learning: Unsupervised Learning and Feature Engineering**.

## Goal
Group employees from a mental health survey into interpretable clusters, to help an HR department target a preventive mental health programme.

## Data
OSMI Mental Health in Tech Survey 2016 (1,433 respondents, 63 questions).
Source: https://www.kaggle.com/osmi/mental-health-in-tech-2016

## Approach
1. **Data exploration:** missing values, messy free-text answers, unrealistic ages
2. **Data cleaning:** employees only, dropped unusable columns, grouped gender answers, filled missing values with meaningful categories
3. **Encoding and scaling:** ordinal and one-hot encoding, country grouping, role columns, standardisation
4. **Feature selection:** removed low-variance and highly correlated columns (168 → 151)
5. **Dimensionality reduction:** PCA (65 components, 80% of variance), compared with MDS
6. **Clustering:** k-Means (k = 3, chosen with elbow method and silhouette score), checked with Gaussian Mixture Models
7. **Cluster profiles:** description of each employee group

## Main result
Three overlapping employee profiles were found:
- **Fearful & unsupported** (331): often affected, but fear stigma and do not trust supervisors
- **Affected but supported** (380): similarly affected, but have benefits and trust supervisors
- **Not personally affected** (432): little personal experience with mental health conditions

## How to run
1. Open `mental_health_case_study.ipynb` in Google Colab.
2. Download the CSV from Kaggle and upload it to your Google Drive.
3. In the setup cell, change `path` to the location of the CSV in your Drive.
4. Run all cells (Runtime → Run all). Charts are saved to the `figures` folder set in the setup cell.

All charts are also included in the `figures` folder of this repository and are shown directly in the notebook outputs.

## Libraries
Python 3, pandas, NumPy, scikit-learn, matplotlib
