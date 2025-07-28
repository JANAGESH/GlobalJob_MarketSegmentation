# Global Job Market Segmentation

This repository contains the code, analysis, and results for the project "Global Job Market Segmentation", which explores and clusters a large, synthetic, international job postings dataset using advanced Natural Language Processing (NLP) and unsupervised machine learning methods.

Overview:
Labor markets are increasingly global, digital, and dynamic. This project applies advanced NLP and clustering methods to segment over 100,000 global job postings by job description, salary, experience, geography, and company size, revealing hidden patterns and actionable workforce insights.

Main Deliverables:

End-to-end code (Google Colab Notebook)
Summary documentation and cluster tables
Exploratory and cluster analysis outputs

Dataset:

Source: https://www.kaggle.com/datasets/ravindrasinghrana/job-description-dataset?resource=download
Size: 100,000 stratified-sampled records (from 1.5M+ original)
Coverage: 216 countries, 147 unique job titles, 214 cities, wide salary/experience ranges
Fields: Country, City, Job Title, Role, Salary, Experience, Description, Geolocation, Company Size, etc.

Project Structure:

text
├── GlobalJob_MarketSegmentation.docx    # Project report, summary, and tables
├── GlobalJobMarketSegmentation.ipynb    # Complete data science notebook
├── outputs/                             # (See GDrive link for outputs)
├── README.md                            # (this file)

You can find full outputs, plots, and result tables from the above documents

Methodology:

1. Data Preparation
2. Stratified sampling for balance
3. Cleaning and normalization (salary extraction, missing values, etc.)
4. Text Processing
5. TF-IDF vectorization of job descriptions
6. Dimensionality reduction (Truncated SVD)
7. Topic Modeling
8. Latent Dirichlet Allocation (LDA) to extract job function themes/keywords
9. Clustering
10. KMeans (main model), DBSCAN, MiniBatchKMeans for robustness checks
11. Cluster quality measured with silhouette scores
12. Interpretation via centroids, top keywords, representative roles/cities/salaries
13. Analysis
14. Role/country/city ranking by cluster
15. Salary and experience distributions per segment
16. Cluster-specific recommendations

Key Findings:

Dominant Job Segments (Sample)

Cluster 0 (87%): Mid-salary urban tech roles (e.g., Network Admin, UX Designer in Apia, Seoul, Hanoi) — average salary ~$80K, experience 8–12+ years
Cluster 1 (6.8%): Entry-level support/HR for smaller companies (Customer Success, Sales) — lower salary (<$15K)
Cluster 2 (1.3%): Freelance/remote, lower-paid creative/interaction design roles
Cluster 3 (1.8%): Social/field/media management jobs, often highly variable pay
Cluster 4 (3.1%): Senior engineering and QA (Quality Assurance Analyst, Manufacturing Engineer) — average salary ~$90K, 8–12+ yrs experience

Top Cities: Apia, Seoul, Hanoi, Caracas, San Juan, Cockburn Town, Ashgabat
Topic Themes: Varying by cluster; e.g., "user, data, design" for tech, "sales, customer" for support

See the full report (GlobalJob_MarketSegmentation.pdf) or the notebook for detailed tables.

How to Run:

Install dependencies

python
pip install pandas numpy scikit-learn seaborn matplotlib plotly missingno
Open and Run Notebook

Use provided Jupyter notebook: GlobalJobMarketSegmentation.ipynb
Or run interactively on Google Colab
Make sure to download the dataset from Kaggle and update the dataset path.

View Outputs

You can directly explore output plots, tables, and summaries from Google Drive Output Folder.

Output Files:

📂 Output Files, Cluster Tables, Segment Results: https://drive.google.com/drive/folders/1bxfK7Kn4qTMm-uN0TstGDnIUbklJX9vB?usp=sharing

Recommendations & Next Steps:

Utilize advanced text embeddings (e.g., contextual BERT embeddings) for even better description clustering
Normalize salary bands by country/currency for better cross-region analysis
Add time-trend or employer profiling for dynamic, actionable dashboards
Expand real-world generalization by augmenting with more granular data on job level and organization

References:

Kaggle Job Description Dataset

Project outputs: https://drive.google.com/drive/folders/1bxfK7Kn4qTMm-uN0TstGDnIUbklJX9vB?usp=sharing

For full technical walk-through, see GlobalJobMarketSegmentation.ipynb

Note:

This project utilizes a synthetic dataset. While patterns and methodology are valid for experimentation, exercise caution in applying results directly in real-world HR or policy contexts. For production uses, enriching the dataset with more granular features is recommended.

Author: JANAGESH R
