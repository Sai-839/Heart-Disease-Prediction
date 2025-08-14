Heart Disease Prediction using Machine Learning
This project uses machine learning techniques to predict the likelihood of a patient having heart disease. The analysis is based on the "Personal Key Indicators of Heart Disease" dataset, which originates from the CDC's Behavioral Risk Factor Surveillance System (BRFSS). The primary goal is to build an accurate classification model and identify the most significant factors contributing to heart disease.

The project workflow was managed using Tableau for data visualization and SAS E-Miner for predictive modeling.

📊 Data Exploration & Key Findings
Initial data exploration was conducted in Tableau to identify relationships between various health indicators and the presence of heart disease.

Key Insights:
Age: The risk of heart disease increases significantly with age, with the highest prevalence observed in the 60-69 age group.

Smoking: A clear correlation was found between smoking habits and a higher incidence of heart disease.

BMI: Patients with heart disease tend to have a higher average Body Mass Index (BMI).

Gender: Male patients showed a higher prevalence of heart disease compared to female patients in this dataset.

Physical Activity: Difficulty in walking was identified as a contributing factor.

A Chi-Square analysis in SAS E-Miner further confirmed that General Health, Age Category, Difficulty Walking, Stroke, and Diabetic Status are the most influential predictors in the dataset.

🤖 Modeling & Evaluation
The core modeling process was performed in SAS E-Miner. The dataset was partitioned into training (80%), validation (10%), and testing (10%) sets.

Models Developed:
Four classification models were built and compared:

Decision Tree 1: (Max branch=3, Max depth=5, Criterion=Entropy)

Decision Tree 2: (Max branch=5, Subtree=Largest)

Decision Tree 3: (Max branch=5, Criterion=Gini, Subtree=Largest)

Logistic Regression

Model Comparison & Final Selection:
The models were evaluated based on their misclassification rate on the validation dataset, with a special focus on correctly identifying true positives (patients with heart disease) due to the severe class imbalance in the data.

While the Decision Tree models struggled with the imbalanced classes, the Logistic Regression model performed the best. It achieved the lowest misclassification rate and, more importantly, correctly classified the highest number of patients who actually had heart disease.

Therefore, Logistic Regression was selected as the final model.

💡 Conclusion & Recommendations
This project successfully developed a Logistic Regression model to predict heart disease. The analysis confirmed that lifestyle and demographic factors like age, general health, BMI, and smoking are critical indicators.

Lessons Learned:
Predictive modeling with heavily imbalanced datasets is challenging and can lead to biased results if not handled carefully.

Logistic Regression can be a robust baseline model for binary classification tasks, even outperforming tree-based models in certain scenarios.

Feature exploration is crucial for understanding key drivers before building complex models.

Recommendations for Future Work:
Address Class Imbalance: Employ techniques like SMOTE (Synthetic Minority Over-sampling Technique) or adjust class weights to create a more balanced dataset for training.

Expand Feature Set: Incorporate other clinically relevant data, such as cholesterol levels and blood pressure readings, for a more comprehensive analysis.

Explore Advanced Models: Implement more complex algorithms like Gradient Boosting, Random Forests, or Neural Networks, which may yield higher accuracy.

Hyperparameter Tuning: Conduct systematic tuning of model parameters to optimize performance further.
