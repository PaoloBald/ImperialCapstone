# Datasheet for Credit Card Fraud Detection Dataset

## Motivation

- Purpose: The dataset was created to aid in the development and evaluation of credit card fraud detection algorithms.
- Creator and Funding: The dataset has been collected and analyzed during a research collaboration between Worldline and the Machine Learning Group of ULB (Université Libre de Bruxelles). Funding information is not publicly disclosed.

## Composition

- Instances: Each instance in the dataset represents a credit card transaction.
- Count: The dataset contains 284,807 transactions, out of which 492 are fraudulent.
- Missing Data: No missing data is reported.
- Confidentiality: The dataset is already anonymized and doesn't contain personal information.

## Collection Process

- Acquisition: The data comprises transactions made by European cardholders in September 2013.
- Sampling Strategy: The dataset presents transactions that occurred in two days.
- Time Frame: Transactions from September 2013.

## Preprocessing/Cleaning/Labeling

- Preprocessing: Features V1-V28 are the result of a PCA transformation to protect user identities and sensitive features. Only 'Time' and 'Amount' features are not transformed.
- Raw Data: It is not mentioned whether the raw data is saved. The available dataset is preprocessed.

## Uses

- Other Tasks: Beyond fraud detection, the dataset could potentially be used for anomaly detection, clustering tasks, or cost-sensitive learning.
- Impact on Future Uses: The dataset is highly imbalanced, which should be considered during any kind of future use to avoid biases.
- Mitigation of Risks: Techniques like SMOTE or ADASYN could be used for handling class imbalance.
- Inappropriate Uses: The dataset should not be used for tasks that require identifying any form of demographic bias due to the lack of such information.

## Distribution

- Previous Distribution: The dataset is publicly available and is commonly used for academic purposes and machine learning competitions.
- Copyright/IP/ToU: The dataset comes with a request for citation if used in research projects, but no strict IP or ToU are mentioned.

## Maintenance

- Maintainer: The dataset is maintained by the Machine Learning Group of ULB in collaboration with Worldline.


