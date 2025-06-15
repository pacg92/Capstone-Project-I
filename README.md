### SaaS Product Recommendation for Targeted Marketing  
 

**Pablo Cisternas G. **  

[Click here to go to the notebook](https://github.com/pacg92/Capstone-Project-I/blob/master/SaaS%20Product%20Recommendation%20for%20Targeted%20Marketing%20%20-%20number%20crunching.ipynb)

#### Executive summary  
This project aims to support a SaaS sales department in optimizing its marketing campaigns by recommending the most likely product a B2B customer will purchase. Using a dataset of ~10,000 historical transactions, we built predictive models based on client segment, industry, seasonality, and transaction value. Our best-performing model, a Decision Tree, achieved approximately 48–51% accuracy and provides interpretable decision rules. These insights can be embedded in the marketing workflow to boost conversion rates, currently around ~10%, by enabling more targeted and timely outreach.

---

#### Rationale  
- Marketing teams currently rely on manual heuristics and broad segmentation, which results in inefficient targeting and low campaign conversion (~10%). 
- A data-driven product recommender can help personalize outreach, reduce wasted efforts, and improve revenue per campaign.
- This approach supports more efficient allocation of marketing resources while enhancing the client experience.

---

#### Research Question   
 
Which SaaS product category is a given customer most likely to purchase next, considering their segment, industry, and seasonal purchasing behavior?

---

#### Data Sources  
Due to data protection laws and company security policies, access to real transactional data was restricted. Instead, the [Amazon AWS SaaS Sales Dataset](https://www.kaggle.com/datasets/nnthanh101/aws-saas-sales/data) was selected as a suitable alternative due to its strong similarity to the originally intended data and its relevance for modeling purposes.

Historical Amazon AWS SaaS Sales Dataset (~10,000 transactions), containing fields such as:  
  - `Order Date` (YYYY-MM-DD)  
  - `Industry`, `Segment`  
  - `Product Purchased`  
  - `Sales`, `Discount`, `Profit`  

---

#### Methodology    
1. **Data Understanding & Preparation**: cleaning, outlier removal, feature engineering.  
2. **Exploratory Analysis**: distribution plots, seasonality decomposition, segment-industry heatmaps.  
3. **Modeling**: train/test split (80/20), label encoding, pipelines with StandardScaler and classifiers.  
4. **Model Selection & Tuning**: Decision Tree, Random Forest, XGBoost, KNN; grid search with 5-fold CV.  
5. **Model Improvement**: robust CV, learning curves, hyperparameter tuning, class-weighted adjustments.  
6. **Evaluation**: hold-out test metrics (accuracy, F1, recall by class), confusion matrices, rule extraction.

---

#### Results    
- The **Decision Tree** model achieved ~51% accuracy and balanced recall across four product categories.  
- Top predictors: **Regular Sale amount**, **Industry Category**, **Segment**, **Quarter**.  
- Extracted decision rules (e.g., low sale amounts in Q2 for Core Economic → Product A) provide clear marketing triggers.

---



##### Contact and Further Information  
For questions or collaboration, please contact **pcisternas@fen.uchile.cl** or visit the project repository on GitHub.  
