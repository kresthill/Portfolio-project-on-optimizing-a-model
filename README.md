# Ad Click Prediction Using Bayesian-Optimized LightGBM

This project predicts whether a user will click on an advertisement based on demographic and contextual features such as age, gender, device type, and the time of day the ad is shown. The goal is to support marketing teams in targeting the right users and maximizing campaign efficiency. Using a machine learning model trained on thousands of real-world samples, we can estimate the likelihood of a click and help businesses allocate advertising resources more intelligently.

## DATA
The dataset was sourced from Kaggle. It includes 10,000 customer records with features like age, gender, device type, ad position, and a binary label indicating whether the user clicked on an ad. Some features had missing values which were handled through imputation. Irrelevant fields such as full names and IDs were excluded to preserve privacy and improve model performance.

## MODEL
The model used is LightGBM, a gradient boosting framework that is efficient and well-suited for tabular data with categorical features. It was chosen for its speed, support for missing values, and ability to handle class imbalance effectively. Its native handling of categorical variables and support for regularization make it ideal for this classification problem. 

## HYPERPARAMETER OPTIMSATION
Hyperparameters were optimized using Bayesian Optimization with the optuna library. Parameters tuned include:
- learning_rate
- num_leaves
- max_depth
- min_child_samples
- feature_fraction
- bagging_fraction
- scale_pos_weight
- The optimization maximized the AUC score on the validation set, ensuring better generalization and reducing overfitting.
  
## RESULTS
The final model achieved:
- AUC Score: 0.6777
- F1 Score (Clicked Ads): 0.80
- Recall (Clicked Ads): 0.94
- Accuracy: 0.69
  
This indicates the model is highly effective at identifying users who are likely to click on ads, with a good balance between false positives and missed opportunities. Performance was measured on a held-out test set using threshold-optimized predictions.

**CONTACT**
Feel free to reach out:  
 📨 Email: datafest2000@gmail.com  
 🐤 X or Twitter: @kresthill_07  
 🛍️ LinkedIn: LinkedIn: linkedin.com/in/festus-kresthill-178557330  



