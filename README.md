# Explainable Techniques: PDP, ICE, and ALE Plots

## Project Overview
This project explores model interpretability using **Partial Dependence Plots (PDP)**, **Individual Conditional Expectation (ICE)** plots, and **Accumulated Local Effects (ALE)** plots.  
The goal is to analyze how selected features of a dataset influence model predictions and to compare the strengths and limitations of each visualization method.  

## Dataset and Model
- **Dataset**: Online Shoppers Purchasing Intention Dataset (UCI)  
- **Model**: XGBoost 

The dataset contains various behavioral and informational features about online shoppers (e.g., Administrative, Informational, Product Related, Bounce Rate, Exit Rate, Page Value, Special Day).  
These features were analyzed to understand their relationship with the probability of purchase.  

## Methods
1. **Exploratory Data Analysis (EDA)**  
   - Checked feature distributions and correlations.  
   - Examined potential multicollinearity between features.  

2. **PDP (Partial Dependence Plots)**  
   - Visualized the average marginal effect of features on purchase probability.  

3. **ICE (Individual Conditional Expectation)**  
   - Displayed feature effects at the individual level to reveal heterogeneity among visitors.  

4. **ALE (Accumulated Local Effects)**  
   - Addressed issues with correlated features by providing unbiased, localized explanations of feature impact.  

## Results & Interpretation
- **PDP vs ICE**  
  - PDP plots showed general trends, while ICE plots revealed variation across individual visitors.  
- **PDP vs ALE**  
  - ALE plots offered more reliable interpretations when features were correlated, avoiding misleading conclusions seen in PDP.  
- **Interesting Findings**  
  - Certain features such as *Page Value* and *Special Day* had clear non-linear effects.  
  - Features like *Administrative* and *Product Related* showed decreasing probabilities beyond certain thresholds, suggesting patterns of "window shopping."  
- **Correlation Impact**  
  - Strong correlations between features (e.g., time spent and number of pages visited) influenced PDP results. ALE plots provided more accurate insights in these cases.  

*The above Readme was edited with ChatGPT 5 at September 29 1:26 AM. It was used to structure, edit and organize text/content* 

 Resources: 
 - https://github.com/AIPI-590-XAI/Duke-AI-XAI/blob/main/explainable-ml-example-notebooks/global_explanations.ipynb
 - https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset
 - https://christophm.github.io/interpretable-ml-book/pdp.html
 - https://slds-lmu.github.io/iml_methods_limitations/pdp-causal.html
 - ChatGPT 5 for editing texts 
 