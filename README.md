# **Multivariate-Customer-Segmentation-for-E-Commerce**

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

This repository contains an end-to-end data science project focused on creating statistically rigorous and interpretable customer segments for an e-commerce business. The analysis moves beyond traditional RFM modeling by applying a suite of multivariate statistical techniques—including PCA, Factor Analysis, and Clustering—to a dataset of brand-level purchase histories.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **📋 Problem Statement**
E-commerce businesses need accurate, explainable customer segmentation to improve marketing targeting, personalize offers, and allocate budgets efficiently. This project addresses the challenge of identifying distinct customer groups based on their purchasing patterns when traditional recency and monetary data are unavailable. The goal is to uncover latent behavioral drivers and create business-actionable segments that tie directly to marketing levers like retention, cross-selling, and customer lifetime value (LTV).

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **📊 Data Summary**
The analysis is based on a customer-level e-commerce dataset containing purchase counts for approximately 35 different brands.

Schema: The data includes Cust_ID, Gender, Orders, and a series of columns representing the quantity purchased for each brand.

Nature of Data: The dataset is rich in behavioral signals but lacks explicit Recency and Monetary values. To overcome this, the analysis uses purchase frequency (brand_sum) and purchase diversity (the number of unique brands purchased) as key proxies for customer value and engagement.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **🛠️ Methodology & Techniques**
To ensure the segments are both statistically valid and business-relevant, a sophisticated multivariate analysis workflow was employed.

Feature Engineering: New features were derived to capture key behavioral traits, including brand_sum (total items purchased) and purchase_diversity. Brands were also grouped into higher-level categories like Electronics, Apparel, and Food.

Dimensionality Reduction (PCA): Principal Component Analysis was used to reduce the high-dimensional brand data and identify the primary axes of variance in customer purchasing behavior.

Exploratory Factor Analysis (EFA): EFA was used to extract latent, unobservable behavioral factors (e.g., "affinity for electronics," "preference for apparel"). The suitability of the data was confirmed with KMO and Bartlett's tests, and a Varimax rotation was applied to ensure the resulting factors were interpretable.

Clustering (K-Means): K-Means clustering was performed on the customer factor scores derived from EFA. The optimal number of clusters was determined using the Elbow Method and Silhouette Score.

Segment Validation & Exploration:

Linear Discriminant Analysis (LDA): Used to confirm the linear separability of the resulting clusters.

Canonical Correlation Analysis (CCA): Employed to explore the relationships between purchasing in different product categories (e.g., Electronics vs. Apparel).

Hypothesis Testing: A suite of statistical tests (including ANOVA/Kruskal-Wallis, MANOVA, and Chi-square) was conducted to formally validate that the identified segments were statistically different from one another in terms of their purchasing behavior.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **🚀 Tools and Libraries**
This project was built using Python and the following core data science libraries:

Pandas & NumPy: For data manipulation and numerical operations.

Scikit-learn: For data preprocessing (scaling), PCA, K-Means Clustering, and LDA.

Statsmodels: For advanced statistical modeling and hypothesis testing.

FactorAnalyzer: For performing Exploratory Factor Analysis, including KMO and Bartlett's tests.

Matplotlib & Seaborn: For data visualization and diagnostic plotting.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **💡 Inference and Conclusion**
The analysis successfully demonstrated that rich, brand-level purchase data is sufficient to produce highly interpretable and statistically significant customer segments, even without traditional RFM data.

The key insight is that Factor Analysis effectively condensed noisy, brand-level preferences into a few core behavioral dimensions. Clustering on these factors yielded distinct personas (e.g., "High-Value Specialists," "Frequent Low-Diversity Buyers," "Occasional CPG Buyers") that showed statistically significant differences in their purchasing habits. These differences directly inform tailored marketing strategies.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# **Final Conclusion:**
This project provides a reproducible and statistically robust framework for customer segmentation. The resulting segments are not just abstract groupings; they are tied to actionable business plans. For example:

High-Value Segments can be targeted with VIP loyalty programs and premium bundles.

High-Frequency / Low-Diversity Segments are prime candidates for discovery campaigns and cross-selling initiatives.

Low-Engagement Segments can be entered into cost-effective win-back campaigns.

This framework is ready for A/B testing of these targeted campaigns and can be easily extended to include CLTV modeling if monetary and recency data become available in the future.
