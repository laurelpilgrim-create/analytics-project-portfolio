Modeling Diabetes Progression: A Comparison of Linear Regression, K-means, and PCA 

Problem Description

The goal of this project is to analyze the Scikit-learn Diabetes Dataset to evaluate how well different machine learning techniques can model or describe the data. This study applies Linear Regression, which is a supervised learning model to predict diabetes progression and compares it with a K-means clustering with and without Principal Component Analysis (PCA), which is an unsupervised learning method. The objective is to determine which approach best fits the dataset. Based on performance metrics such as Mean Squared Error (MSE), R-squared, inertia, and silhouette score. 

Data Description 

The dataset used in this project is the Scikit-learn Diabetes dataset, which is commonly used for regression tasks. It contains 442 samples of patient data with 10 features. The variables include age, sex, body mass index (BMI), blood pressure and blood serum measurements. The target variable represents a quantitative measure of diabetes disease progression one year after baseline. The dataset is already preprocessed and standardized, making it suitable for machine learning models without additional scaling. 

Methods Used and Reason for Selection 

Linear Regression was selected for this analysis because the target variable, diabetes progression, is continuous rather than categorical. This makes Linear Regression an appropriate and effective baseline model for prediction. Linear Regression models are easy to interpret and widely used in regression tasks. They are clear and easy to understand and show how input features influence the outcome. The dataset was divided into a training set of 353 samples and a testing set of 89 samples. The model was trained on the training data and then evaluated on the testing data to measure its predictive performance. 

K-Means clustering was used to explore whether the dataset naturally forms groups or patterns among the data points (Zhang et al., 2023). K-Means is an unsupervised learning method which means it does not use the target variable during training. The purpose of using this method was to identify hidden structures in the data and to compare any discovered clusters with actual diabetes progression levels.  In this analysis, the number of clusters was set to k=3, allowing the model to group the data into three distinct segments based on feature similarities. 

Principal Component Analysis (PCA) was applied to reduce the dimensionality of the dataset from 10 features down to 2 and 3 components. The 2-component version was primarily used for visualization. The 3-component version provided improved clustering visualization in a higher-dimensional space. PCA was chosen to simplify the dataset, reduce noise, and highlight the most important patterns withing the data. The dimensionality reduction also helped to improve the performance of K-Means clustering and made it easier to visualize relationships withing the dataset. 

Evaluation Metrics 

The Linear Regression model’s performance was evaluated by using Mean Squared Error (MSE) and R-squared (R2). MSE measures the average prediction error.  R2 shows the strength of the relationship between the model and the dependent variable. The results showed an MSE of 2900.19 and an R² value of 0.45. Cross-validation was performed to ensure the model’s reliability. These results suggest that the model explains approximately 45-48% of the variance in the diabetes progression, which indicates a moderate fit. 

The K-Means clustering used inertia and silhouette score as its metrics. Inertia measures how tight the clusters are. Using the original dataset, the model produced an inertia of 6.51 and a silhouette score of 0.15. After applying PCA, the inertia decreased to 2.08 and the silhouette score increased to 0.33. These results show that PCA significantly improved clustering quality by creating more compact and better separated clusters. 

When comparing Linear Regression with and without PCA, the results show that important predictive information was lost during dimensionality reduction. Using PCA reduced model performance for regression. When PCA was applied, the model using 2 components had a MSE of 2534.24 and an R² of 0.33, and when using 3 components had an MSE of 3677.67 and a R² of 0.31. This indicates that PCA reduced the effectiveness of the regression model. The likely reason is that important predictive information was lost when the data was compressed into fewer components, and it negatively impacted the model’s ability to accurately predict diabetes progression. 
