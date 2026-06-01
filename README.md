# Lab 1: Data Exploration, Preprocessing, and Statistical Analysis

**Student:** Arif Ansari  
**Course:** MSCS 634 - Advanced Data Science  

## Purpose of Lab Work
The purpose of this lab is to establish a robust end-to-end data pipeline within Jupyter Notebook. It focuses on taking raw data, inspecting it for discrepancies, running structural statistical diagnostic filters, clean handling anomalies, and formatting inputs to make them ready for downstream machine learning workloads.

## Key Insights
* **Visualizations:** The initial distribution profiles clearly highlighted scale divergence. Our pricing metrics contained long-tail components skewing statistical frameworks, while individual checkout counts (`Units_Sold`) showed uniform tracking profiles across distinct product fields.
* **Pre-processing Adjustments:** * Missing elements inside the `Store_Rating` field were filled using the feature's historical median.
  * Extraneous records where prices exceeded the standard IQR thresholds (\$15.54 to \$494.39) were isolated and removed to prevent modeling skew.
  * Feature variables were mapped smoothly between a 0 to 1 domain via Min-Max scalar techniques.
* **Statistical Inferences:** Correlation matrix analysis revealed negligible linear cross-relationships between item cost profiles and organic store evaluation ratings, reinforcing that satisfaction markers track independently of price parameters.

## Challenges & Strategic Decisions
* **Challenge:** High baseline variance caused by artificially injected extreme outliers skewing parameter calculations.
* **Resolution Decision:** Using mean value computations for substitution would pull baseline distributions out of alignment. Therefore, a clean slice operation using historical IQR bounds was implemented to isolate standard market trends without losing bulk behavioral features.
