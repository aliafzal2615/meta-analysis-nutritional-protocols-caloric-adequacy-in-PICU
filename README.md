## Meta-Analysis of Structured Nutritional Protocols in the PICU

### Overview
This repository contains the complete analytical pipeline for a systematic review and meta-analysis investigating the impact of **structured nutritional protocols** on **caloric adequacy** in Pediatric Intensive Care Units (PICU). 

The project spans the entire evidence synthesis lifecycle—from machine-learning-assisted screening of thousands of citations to advanced meta-regression and sensitivity modeling. By evaluating nine studies across six countries, this analysis provides a high-resolution look at how standardized feeding algorithms influence the delivery of prescribed energy to critically ill children.

---

### Why This Research Matters
Achieving caloric adequacy in the PICU is a persistent clinical challenge linked to patient outcomes, yet practices vary significantly between institutions. This repository is designed for:
* **Clinical Researchers:** To understand the specific study-level characteristics (e.g., nurse-led vs. dietitian-led) that drive protocol success.
* **PICU Practitioners & Policy Makers:** To access robust evidence supporting the implementation of standardized feeding protocols.
* **Data Scientists/Methodologists:** To see a transparent, "gold-standard" implementation of meta-analytical techniques using Python and active learning.

---

### Repository Contents
The documentation and code are organized into six logical stages, reflecting the rigorous methodology employed:

1.  **Literature Screening (ASReview):** Integration of AI-driven active learning to prioritize relevant citations, utilizing "prior knowledge seeds" to accelerate the screening process while maintaining PRISMA transparency.
2.  **Pooled Meta-Analysis:** Quantitative synthesis using **Restricted Maximum Likelihood (REML)** and **Random-Effects modeling** to account for clinical heterogeneity across global settings.
3.  **Publication Bias Assessment:** Evaluation of small-study effects through Funnel plots, Egger’s test, and the **Trim-and-Fill** method to ensure results are not inflated by non-published null findings.
4.  **Subgroup Analysis:** Comparative evaluation of categorical moderators, such as protocol type (nurse-led vs. non-nurse-led) and study design.
5.  **Meta-Regression:** Advanced modeling using the **Knapp-Hartung (KH) adjustment** to identify which continuous variables (e.g., patient age, study duration) explain variance in treatment effects.
6.  **Sensitivity Analysis:** Seven distinct stress tests—including "leave-one-out" and estimator comparisons—to verify the stability and robustness of the primary findings.

---

### Methodological Strengths & Feasibility
This meta-analysis stands out by addressing common pitfalls in clinical evidence synthesis through several advanced technical choices:

* **Handling Skewed Data:** We utilize the **Wan et al. (2014) method** to accurately convert median/IQR values (common in critical care) into mean/SD, allowing for the inclusion of studies that would otherwise be excluded from traditional meta-analysis.
* **Rigorous Variance Estimation:** By employing the **Knapp-Hartung correction**, this pipeline provides more conservative and reliable inference for small-sample meta-analyses (k < 10), reducing the risk of false positives.
* **Transparency & Reproducibility:** Every analytical step—from the removal of outlier studies to the choice of heterogeneity estimators (REML vs. Paule-Mandel)—is documented with clear rationale and visual diagnostics.
* **Addressing Bias:** Specific sensitivity analyses (SA7) filter for "secular trend bias" by comparing concurrent controls against historical ones, ensuring the measured benefits are truly attributable to the nutritional protocols.

---

[![DOI](https://zenodo.org/badge/1206067592.svg)](https://doi.org/10.5281/zenodo.19486060) "https://doi.org/10.5281/zenodo.19486060"

---
