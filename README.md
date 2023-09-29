# PROJECT TITLE 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

This project employs advanced machine learning algorithms to enhance credit card security by accurately detecting fraudulent transactions. It analyzes a vast array of transaction data in real-time to identify patterns indicative of fraud. The model has been rigorously tested and optimized to ensure a high level of accuracy, even when dealing with imbalanced data where fraudulent transactions are rare compared to legitimate ones. This technology aims to protect cardholders and financial institutions from financial loss due to fraud, while also minimizing false alarms that can cause unnecessary inconvenience.



## DATA

The data for this project consists of credit card transactions from September 2013, focusing on European cardholders. It was sourced from Kaggle and originally collected during a research collaboration between Worldline and the Machine Learning Group of ULB (Université Libre de Bruxelles). 

The dataset is highly imbalanced, containing 492 fraudulent transactions out of a total of 284,807, representing just 0.172% of all transactions. It includes features that are the result of a Principal Component Analysis (PCA) transformation, which means the original features have been mathematically transformed to protect confidentiality. Only the 'Time' and 'Amount' features retain their original form.

**Citations:**

- Andrea Dal Pozzolo, Olivier Caelen, Reid A. Johnson and Gianluca Bontempi. Calibrating Probability with Undersampling for Unbalanced Classification. In Symposium on Computational Intelligence and Data Mining (CIDM), IEEE, 2015.
- Dal Pozzolo, Andrea; Caelen, Olivier; Le Borgne, Yann-Ael; Waterschoot, Serge; Bontempi, Gianluca. Learned lessons in credit card fraud detection from a practitioner perspective, Expert systems with applications,41,10,4915-4928,2014, Pergamon.



## MODEL 

For this project, we employed a combination of machine learning models to tackle the problem of credit card fraud detection. Specifically, we used Logistic Regression, Random Forest, and an Ensemble model that combines multiple Random Forest classifiers. Additionally, we utilized Bayesian Optimization for hyperparameter tuning to achieve optimal model performance.

Why These Models?

- Logistic Regression: It serves as a baseline model, offering interpretability and quick training. It's often used in binary classification problems like fraud detection.

- Random Forest: This model is known for its high accuracy, ability to handle imbalanced datasets, and its feature importance capabilities. It's well-suited for complex classification tasks and can handle both categorical and numerical features effectively.

- Ensemble Model: We used a soft-voting ensemble of Random Forest classifiers to further boost the performance. Ensembles often perform better than individual models as they combine multiple perspectives.

- Bayesian Optimization: Given the high dimensional feature space and multiple hyperparameters, Bayesian optimization was chosen for more efficient and effective tuning compared to traditional methods like grid search.


## HYPERPARAMETER OPTIMSATION

For each model, I considered the following hyperparameters:

- Logistic Regression: 
  - `C`: Inverse of regularization strength
  - `max_iter`: Maximum number of iterations for the solver to converge

- Random Forest: 
  - `n_estimators`: Number of trees in the forest
  - `max_depth`: Maximum depth of each tree
  - `max_features`: Number of features to consider for the best split
  - `min_samples_split`: Minimum number of samples required to split a node

- Ensemble Model: 
  - Combined hyperparameters from the individual Random Forest models

Optimization Method:

I employed different techniques for hyperparameter tuning:

- Randomized Search: For Logistic Regression and the initial Random Forest model, I used Randomized Search CV with a predefined parameter grid. This method performs a random search over the parameter space, which is computationally less expensive than Grid Search.

- Bayesian Optimization: For fine-tuning the Random Forest and Ensemble models, I used Bayesian Optimization. This approach is more efficient than grid search and random search for a high-dimensional hyperparameter space. It builds a probabilistic model of the objective function and uses it to select the most promising hyperparameters to evaluate in the true objective function.

By using a combination of these methods, I was able to efficiently explore the hyperparameter space and optimize the models for better performance.


## RESULTS

Key Metrics:

- Recall Score: Our ensemble model achieved a recall score of approximately 0.798 on the test set, indicating a high ability to correctly identify fraudulent transactions.
  
- AUPRC: The Area Under the Precision-Recall Curve was 0.865, confirming the model's strong performance in a class-imbalanced scenario.

- Confusion Matrix: The confusion matrix showed that the model has a balanced performance in terms of false positives and false negatives, further validating its effectiveness in fraud detection.

What I Can Learn:

Feature Importance: Random Forest allowed us to assess feature importances, providing insights into which transaction attributes are most indicative of fraud.

Model Efficacy: The high recall score suggests that the model is effective in identifying the majority of fraudulent transactions, thereby minimizing financial loss.

Hyperparameter Sensitivity: Bayesian optimization showed that the model's performance is sensitive to certain hyperparameters, reinforcing the need for meticulous tuning.

Class Imbalance Handling: Techniques like SMOTE for oversampling proved beneficial in handling class imbalance, significantly improving model performance.

Ensemble Benefits: The ensemble model combined the strengths of multiple models, demonstrating an improvement in overall performance metrics.

By synthesizing these results and insights, I have not only created a robust fraud detection system but also gained valuable knowledge that can be applied to similar problems in the future.


You can include images of plots using the code below:
![Screenshot](image.png)
![Precision-Recall Curve](file:///C:/Paolo/Reworth/Corso%20AI/Lezioni/modulo%2023/precision_recall_curve.png)


## (OPTIONAL: CONTACT DETAILS)
If you are planning on making your github repo public you may wish to include some contact information such as a link to your twitter or an email address. 

