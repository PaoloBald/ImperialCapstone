# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description


Input: 
- Numerical features from credit card transactions (28 PCA-transformed features along with 'Time' and 'Amount').

Output: 
- Binary classification output indicating whether a transaction is fraudulent (1) or not (0).

Model Architecture: 
- Random Forest Classifier
- Logistic Regression with Hyperparameter Tuning
- Ensemble methods (Voting Classifier)

Performance Metrics

Primary Metric: 
- Recall

Secondary Metrics: 
- Area Under the Precision-Recall Curve (AUPRC)
- Confusion Matrix

Limitations

- The model is trained on a highly specific and imbalanced dataset.
- Due to the lack of demographic information in the dataset, the model has not been evaluated for fairness across different demographic groups.

Trade-offs

- The model uses recall as the primary metric, which may overlook the precision aspect.
- Hyperparameter tuning is computationally intensive, especially with ensemble methods.



Model Details

- Model Name: Ensemble of Random Forest and Logistic Regression
- Date: 20.09.2023
- Version: 1.0
- Model Type: Classification

Intended Use

- Primary Use Case: Credit card fraud detection
- Secondary Use Cases: Anomaly detection, cost-sensitive learning

Model Performance

- Recall: Approximately 0.755 on the test set.
- AUPRC: 0.865
  
Training Data

- Source: Credit Card Transactions Dataset
- Features Used: All features in the dataset, including PCA-transformed features and two non-transformed features ('Time' and 'Amount').

Evaluation Data

- Source: Split from the original dataset
- Method of Data Splitting: Random split with a test size of 0.2

Ethical Considerations

- Fairness: Not evaluated for fairness due to lack of demographic data.
- Bias: Potential bias towards the majority class due to the imbalanced dataset.

Caveats and Recommendations

- Generalization: Caution should be exercised when applying the model to different contexts.
- Imbalance Handling: Further techniques like SMOTE or ADASYN could be used for dealing with class imbalance.


