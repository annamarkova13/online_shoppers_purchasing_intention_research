# Research on Shoppers Purchasing Intention Dataset

## **This project attracted me due to its:**
- **Real-world impact**. The findings have practical implications for optimizing customer behavior, improving user experiences, and driving revenue growth.
- **Broad applicability**. The methodologies and insights can be applied across various customer-focused products and industries, making it universally valuable.
- **Skills development**. The project involved tackling complex data analysis challenges, predictive modeling, and feature engineering, offering opportunities to enhance technical and analytical expertise.
- **Data and modeling challenges**. Addressing issues such as outliers, feature correlations, and model performance provided a stimulating environment to refine problem-solving skills and deliver actionable results. 
By engaging with this project, it was possible to align technical skills with real-world outcomes, contributing to meaningful and measurable improvements in the e-commerce domain.

## **Project Introduction**

### **Product for research**
- **Product**: E-commerce platform, focusing on understanding consumer behavior and enhancing conversion rates.
- **Context**: The dataset includes feature vectors from 12,330 user sessions over a 1-year period, ensuring no bias toward specific campaigns, special days, or user profiles.

### **Research goal**
- To identify key factors influencing purchasing decisions and optimize the platform to enhance revenue generation.

### **Research objectives**
1. Explore user engagement patterns across pages (administrative, informational, and product-related).
2. Investigate the impact of categorical features like Region, TrafficType, Operating System, and Browser on revenue.
3. Detect outliers and analyze their effects on user behavior and model performance.
4. Build a predictive model for identifying sessions likely to generate revenue.

### **Research Tasks**
1. **Data cleaning and validation**: find duplicates and outliers, validate data types
2. **Exploratory data analysis (EDA)**:
   - Univariate analysis of numerical and categorical features.
   - Bivariate analysis by target variable (Revenue).
   - Correlation analysis to identify relationships among features.
3. **Cluster analysis**: Segmented user sessions into behavioral groups.
4. **Predictive modeling**: Compared Random Forest, XGBoost, and Logistic Regression to predict revenue.

### **Data analysis methods used:**
- **Univariate Analysis**: Summary statistics and visualization of feature distributions.
- **Bivariate Analysis**: Feature relationships with Revenue.
- **Correlation Analysis**: Identify strongly correlated features and reduced redundancy.
- **Cluster Analysis**: Behavioral segmentation using k-means clustering.
- **Predictive Modeling**: Machine learning techniques (Random Forest, XGBoost, Logistic Regression) with hyperparameter tuning.

### **Data Source:** 
- Shoppers Purchasing Intention Dataset from the UC Irvine Machine Learning Repository. [Link to dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset)
- This wealth of information allows retailers to understand consumer preferences better, tailor their marketing strategies, and enhance the overall shopping experience, thus further solidifying the role of e-commerce in modern retail.  

### Features
**Class variable:** `Revenue`  
**The description of the dataset features**:

| **Feature**                  | **Description**                                                                                                                                                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administrative               | Number of different types of administrative pages visited by the visitor in a session.                                                                                                                                                               |
| Administrative Duration      | Total time spent on administrative pages in a session.                                                                                                                                                                                               |
| Informational                | Number of different types of informational pages visited by the visitor in a session.                                                                                                                                                               |
| Informational Duration       | Total time spent on informational pages in a session.                                                                                                                                                                                                |
| Product Related              | Number of different types of product-related pages visited by the visitor in a session.                                                                                                                                                             |
| Product Related Duration     | Total time spent on product-related pages in a session.                                                                                                                                                                                              |
| Bounce Rate                  | Percentage of visitors who enter the site from a specific page and leave without<br>triggering any other requests to the analytics server during that session.                                                                                          |
| Exit Rate                    | Percentage of pageviews where a specific page was the last one in the session.                                                                                                                                                                      |
| Page Value                   | Average value for a web page that a user visited before completing an e-commerce transaction.                                                                                                                                                        |
| Special Day                  | Indicates the closeness of the site visiting time to a specific special day (e.g., Mother’s Day, Valentine's Day). Takes values between 0 and 1 based on proximity to the special day,with 1 being the closest.                                        |
| Operating System             | Operating system used by the visitor.                                                                                                                                                                                                                |
| Browser                      | Browser used by the visitor.                                                                                                                                                                                                                        |
| Region                       | Geographic region of the visitor.                                                                                                                                                                                                                   |
| Traffic Type                 | Type of traffic source bringing the visitor to the site (e.g., direct, referral).                                                                                                                                                                   |
| Visitor Type                 | Indicates whether the visitor is a returning or new visitor.                                                                                                                                                                                         |
| Weekend                      | Boolean value indicating whether the visit occurred on a weekend.                                                                                                                                                                                   |
| Month                        | Month of the year when the visit occurred.                                                                                                                                                                                                          |


  
## Research results

### **Impact of Analysis**
The analysis provides actionable insights for optimizing the e-commerce platform, with significant implications for user experience, revenue growth, and operational efficiency:
| **Analysis area**                 | **Impact**                                                                                         |
|-----------------------------------|----------------------------------------------------------------------------------------------------|
| **Improved user targeting**       | Understanding key user behaviors (e.g., product page engagement, bounce rates) allows for better segmentation and targeting of campaigns. |
| **Revenue maximization**          | Focused improvements on high-impact pages (e.g., product-related pages) can directly increase conversions. <br>  Strategies tailored to high-value users and time-intensive explorers enhance revenue opportunities.|
| **Strategic campaign planning**   | Insights on peak activity months and special days enable data-driven marketing campaigns, aligning with user behavior patterns. |
| **Enhanced retention strategies** | Targeted approaches for returning visitors, who form the majority of sessions, can improve loyalty and repeat purchases. |
| **Operational efficiency**        | Cluster-based strategies optimize resources by prioritizing high-value segments and addressing the pain points of low-engagement users. |
| **Data-driven decisions**         | Predictive modeling enables the identification of revenue-generating sessions, guiding business strategies with precision.|

### **Key insights**

1. **User engagement**:
   - Product-related pages dominate user engagement, indicating their critical role in driving purchases.
   - Administrative and informational pages see minimal engagement, suggesting they are less relevant to purchase decisions.
  
  
2. **Behavioral patterns**:
   - Returning visitors have higher session counts but lower conversion rates (14%) compared to new visitors (25%).
   - Peak activity aligns with specific months (March, May, November, December), likely due to seasonality and promotions.
   - Lower bounce and exit rates correlate with higher revenue sessions.
  
  
3. **Cluster analysis**:
   - Identified four clusters:
     - **Low Engagement Users** Cluster 1 (6%): This cluster represents users with minimal engagement and poor interaction with the app’s features. They likely need more targeted recommendations or smoother onboarding to improve their experience.
     - **High Value-Oriented Users** Cluster 3 (7%): Engaged and revenue-contributing users who value personalized offers. Users in this cluster are highly engaged and value the content provided. Strategies to further enhance their experience could include personalized offers or advanced search/filtering features.
     - **Time-Intensive Explorers** Cluster 2 (14%): High engagement but low conversion; need better navigation tools. This cluster consists of users who spend a significant amount of time exploring products but may not always focus on high-value pages. Consider optimizing product categorization or providing better navigation to help them find relevant content faster.
     - **Focused Interactors** Cluster 0 (76%): Efficient engagement; can be encouraged to explore more. These users are focused and interact efficiently with products. Despite their lower engagement duration, they maintain high interaction quality. Encouraging further exploration by suggesting complementary products or related categories could increase their engagement.
  
*Cluster Visualization Based on Engagement Metrics*  
![image](https://github.com/user-attachments/assets/8c3aa975-37e6-487a-ad79-eaa3e42639aa)  
  
*Cluster means for features*  
![image](https://github.com/user-attachments/assets/f389bf46-21d9-4f71-8623-60a0f4155d2d)  


4. **Correlation analysis**:
   - Strong correlations between page counts and durations (e.g., ProductRelated vs. ProductRelated_Duration).
   - Moderate positive correlation between Revenue and PageValues (0.5), indicating high-value pages’ importance in conversions.
   - Negative correlation between product engagement ratio and bounce/exit rates.
![image](https://github.com/user-attachments/assets/9d3706f2-1555-4c13-b071-087eef852867)  

  
5. **Predictive modeling**:
   - **XGBoost** performed best with Average Precision=0.963. It effectively captures nearly all positive cases (with Recall = 0.966), ensuring that we do not miss potential buyers and can target them appropriately.
   - **Random Forest** provided balanced performance with high Recall (0.955) and Precision (0.895). Analysing feature importance the model might be overfitting, because the PageValues is the most dominant feature that affect on 0.3. 
   - **Logistic Regression** showed lower performance, highlighting the need for more complex models.
  
For our target metrics, we prioritized:
- Maximizing Accuracy and AUC to evaluate the overall ability of the model to make correct predictions.
- Maximizing Recall to identify as many true sessions with revenue as possible.
  
Based on models with optimized parameters and thresholds, the following results were obtained:
	
| Metrics | Logistic Regression	| Random Forest	| XGBoost |
|---------|-----------------------|-----------------|---------|
|Accuracy|	0.880|	0.921	|0.895|
|Precision	|0.883	|0.895	|0.846|
|Recall	|0.875	|0.955	|0.966|
|F1-score	|0.879	|0.924	|0.902|
|Avg. Precision	|0.944	|0.974	|0.963|

*Confusion Matrix for 3 models*
![image](https://github.com/user-attachments/assets/c83a6169-850f-4c03-a6b1-a3322758024d)
  
*Precision-Recall Curves for 3 models*
![image](https://github.com/user-attachments/assets/cd4d381a-bedd-4077-9de8-2e9dad80eabf)

Given that **minimizing False Negatives (maximizing Recall** is essential for our use case, **XGBoost is the best choice**. It effectively captures nearly all positive cases (Recall = 0.966 and Average Precision=0.963), ensuring that we do not miss potential buyers and can target them appropriately.  
The analysis highlights the significant impact of specific categorical features such as Region, TrafficType, Operating System, and Browser. These features contribute heavily to the model's ability to make accurate predictions.  
To further improve performance and tailor predictions, it may be beneficial to build region-specific prediction models. This approach could provide deeper insights into the unique characteristics and behaviors within each region, ultimately enhancing our understanding and improving targeting accuracy.  



## Challenges and Solutions

| **Issues**                 | **Challenge**                                      | **Solution**                                      |
|----------------------------|---------------------------------------------------|--------------------------------------------------|
| **Data quality issues**    | Presence of duplicates and potential outliers in the dataset could have skewed the analysis. | Removed 125 duplicate rows to ensure data accuracy. Conducted outlier detection using the IQR method but decided to retain outliers due to their meaningful representation of real-world behavior (e.g., long product-related browsing sessions). For predictive modeling, outliers were capped at the 95th percentile to reduce the impact of extremes. |
| **Skewed feature distributions** | Highly skewed distributions in features like time spent on pages, bounce rates, and page values, making standard statistical approaches less reliable. | Used robust methods like medians and percentiles for summarizing skewed data. Applied transformations (e.g., log or capped outliers) to stabilize the analysis and modeling process. |
| **Understanding user behavior** | Identifying how different features (numerical and categorical) impact purchasing decisions and which to prioritize. | Performed detailed exploratory data analysis to uncover patterns (e.g., high engagement on product-related pages). Used correlation and bivariate analysis to pinpoint strong predictors of revenue (e.g., PageValues, Product_Related features). |
| **Categorical feature dependencies** | Determining which categorical features (e.g., Visitor Type, Traffic Type, Region) were statistically relevant for predicting revenue. | Conducted Chi-Square tests to establish dependencies between categorical features and the target variable (Revenue). Focused on significant features while excluding irrelevant ones (e.g., Region showed no dependency). |
| **Session-level segmentation** | The dataset included diverse user sessions with varying behaviors, requiring segmentation for actionable insights. | Conducted cluster analysis to segment users into meaningful groups (e.g., High Value-Oriented Users, Time-Intensive Explorers). Designed specific strategies for each cluster to optimize engagement and conversion rates. |
| **Balancing model Precision and Recall** | Ensuring the predictive model captures all potential buyers (high recall) while minimizing false positives (precision). | Compared multiple models (Random Forest, XGBoost, Logistic Regression). Selected XGBoost as the final model for its high recall (0.9655), ensuring that nearly all potential buyers are identified. |
| **Handling strong feature correlations** | Highly correlated features (e.g., ProductRelated and Product_Related_Duration) risked redundancy and overfitting in models. | Identified strong correlations and removed redundant features in predictive modeling to simplify the model and improve interpretability. |
| **Behavioral insights and revenue Ggneration** | Linking user behavior (e.g., time on pages, engagement ratios) to revenue generation for actionable insights. | Created new metrics like product engagement ratio and time-per-page to better capture behavioral nuances. Highlighted key differences between revenue-generating sessions and others (e.g., reduced bounce rates, higher engagement). |
| **Seasonal trends and campaign alignment** | Identifying seasonal trends to align marketing campaigns effectively. | Discovered peaks in sessions and revenue during March, May, November, and December, aligning with shopping holidays and promotions. Recommended focusing campaigns during high-traffic months while exploring strategies for off-peak periods. Used new metric to evaluate peak months for predidtion models.|
| **Feature engineering for predictive modeling** | Enhancing predictive power while managing model complexity. | Engineered new features such as product engagement ratio, administrative time per page, and product time per page. Encoded categorical features using One-Hot Encoding and Label Encoding for model compatibility. Adjusted the weights assigned to each class during model training (with SMOTE), that gave higher weight to the minority class and lower weight to the majority class.|











