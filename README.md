# AI-Powered Cross-Platform Influencer-Product Suitability Prediction System

An empirical research study exploring how machine learning can support influencer selection and product suitability ranking for digital marketing campaigns.

## 📌 Research Overview

Selecting suitable influencers for marketing campaigns often relies on follower counts, popularity, or subjective judgments.

This research presents an analytical framework that combines influencer characteristics, product attributes, campaign information, platform context, and historical campaign outcomes to evaluate influencer–product suitability.

The study emphasizes using only information available before a campaign begins when building predictive models, helping prevent data leakage and improve the reliability of evaluation.

## 🎯 Research Objectives

- Develop a reproducible influencer–product suitability framework.
- Integrate influencer, product, and campaign information.
- Identify and prevent feature leakage in predictive modelling.
- Compare machine learning models with transparent suitability scores.
- Evaluate influencer rankings using statistical and revenue-based metrics.
- Examine ranking performance across different temporal cutoffs.
- Support interpretable and data-driven influencer selection.

## 🧠 Machine Learning Techniques

The study evaluates machine learning and ranking approaches, including:

- Random Forest regression
- Mean prediction baseline
- Multi-factor suitability scoring
- Popularity-based ranking
- Audience-match-based ranking
- Temporal evaluation and ranking correlation analysis

## ⚙️ Methodology

The research follows these major stages:

1. Data integration from multiple marketing-related tables.
2. Data validation and quality assessment.
3. Feature engineering and preprocessing.
4. Feature availability and data leakage audit.
5. Temporal training and testing.
6. Machine learning model evaluation.
7. Suitability score and ranking comparison.
8. Temporal robustness analysis.
9. Interpretation of findings and limitations.

## 📊 Dataset Overview

The study uses a project-supplied marketing campaign dataset.

The source tables include:

- Orders
- Influencer campaign performance
- Customer demographics
- Products
- Influencers
- Campaigns

The paper reports an analytical dataset containing 312 influencer–campaign–product observations, derived from 100,000 order-level records.

**Data limitation:** The independent provenance and representativeness of the supplied dataset have not been established. The reported results should therefore be interpreted cautiously.

## 📈 Key Results

The paper reports the following results:

| Experiment | Model or Method | Reported Result |
|---|---|---|
| Principal prediction experiment | Random Forest | R² = 0.920 |
| Principal prediction experiment | Mean baseline | R² = -0.075 |
| Pre-campaign prediction experiment | Random Forest | R² = 0.778 |
| Pre-campaign prediction experiment | Suitability Score v1 | R² = -1.282 |
| Revised ranking experiment | Revised Suitability Score | Spearman ρ = 0.858 |
| Revised ranking experiment | Revised Suitability Score | Top-10% revenue lift = 2.634 |

These values are reported in the research paper and relate to different evaluation experiments. They should not be treated as results from a single unified test.

The findings indicate that predictive performance and ranking quality depend on feature availability, model design, and evaluation methodology.

## 🔍 Feature Leakage Prevention

An important contribution of this research is its feature availability audit.

Historical outcomes such as revenue, order counts, conversions, and return on investment are excluded from prospective predictive features because they are not available when selecting an influencer before a campaign begins.

The study also uses temporal evaluation to examine how well the approaches perform on held-out campaign observations.

## 🏗️ Proposed System Architecture

The conceptual architecture includes:

- Data input layer
- Data validation and quality checks
- Feature engineering and leakage filtering
- Predictive modelling and ranking
- Explainability and decision support
- Model evaluation and temporal robustness checks

The architecture provides a foundation for future implementation of an influencer recommendation and decision-support system.

## 🔮 Future Work

Potential future research directions include:

- Validation using larger, independently sourced campaign datasets.
- Incorporation of consistent engagement metrics across platforms.
- Analysis of influencer biographies, captions, hashtags, and product descriptions.
- Evaluation of learning-to-rank algorithms.
- Fairness and subgroup performance assessment.
- Explainable AI integration.
- Human-expert evaluation of influencer rankings.
- Prospective campaign studies to investigate causal effects.

## 🔐 Ethical Considerations

Influencer recommendation systems should handle personal and audience-related information responsibly.

Future implementations should consider data minimization, access controls, privacy protection, fairness evaluation, and the potential for discriminatory targeting.

## 👤 Authors

- Om Sonawane
- Vishakha Tharkudde
- Prof. Vidya Ugare
- Dr. Prashant Wadkar

**Affiliation:**  
Yashaswi Education Society's International Institute of Management Science, Chinchwad, Pune, India.

## 📄 Research Paper

The complete research paper is available in the `paper/` directory.

**Title:**  
AI-Powered Cross-Platform Influencer-Product Suitability Prediction System

## ⚠️ Limitations

The study uses a relatively small analytical dataset of 312 observations derived from a project-supplied dataset.

The reported results do not establish that influencer selection causes increased sales or return on investment. Model performance and ranking quality require further validation on larger, independently sourced datasets.

The paper also notes that the original modelling source code is unavailable and that no deployed implementation is reported.

## 📜 Disclaimer

This repository documents the research paper and its reported findings. The reported metrics are reproduced from the paper and are not independently verified here.

The repository does not claim that the complete system has been deployed or that the reported findings generalize to all influencers, products, or marketing platforms.
