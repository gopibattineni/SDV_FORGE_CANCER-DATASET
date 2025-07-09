# SDV_FORGE_CANCER-DATASET
This code explains how to create synthetic data using SDV library and tested it cancer dataset 

Key Actions/Steps Taken:

Removed empty column: This indicates a data cleaning step where a column entirely devoid of values (or containing only nulls) was identified and eliminated. This is a standard practice to reduce dimensionality and improve data integrity.

Addressed outlier issues using IQR method: Outliers, which are data points significantly different from others, were handled. The Interquartile Range (IQR) method was employed, suggesting that values falling outside of 1.5 * IQR below Q1 or above Q3 were identified and likely either removed, capped (winsorized), or transformed. This step aims to improve the robustness of subsequent analyses by mitigating the influence of extreme values.

Outcome/Impact:

Quality improved 75% to 79%: This is a crucial metric indicating the success of the preprocessing steps. The "Quality" metric itself isn't defined here, but in the context of synthetic data, it often refers to how well the synthetic data preserves the statistical properties of the real data (e.g., a composite score from SDMetrics, or a specific utility metric). An improvement from 75% to 79% signifies a positive impact from the applied cleaning and outlier handling.

Metrics Used for Evaluation (or related concepts):

Total Variation: This metric (specifically, its complement, TVComplement) is used to assess the similarity of marginal distributions for discrete or categorical columns between two datasets (e.g., real vs. synthetic data). A higher value indicates better similarity.

Kolmogorov-Smirnov Complement: This metric (KSComplement) is used to assess the similarity of marginal distributions for continuous or numerical columns between two datasets. A higher value also indicates better similarity.
