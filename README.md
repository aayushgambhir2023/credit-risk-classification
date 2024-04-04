# credit-risk-classification
**Beginning of Credit Risk Analysis Report**
- Overview: Lending institutions operate on the premise of loan repayment or asset return, but the specter of Credit Risk looms when borrowers default, leading to financial strain. Employing Machine Learning, I delve into historical lending data to construct a model that gauges borrower creditworthiness. Utilizing Logistic Regression, loans are scrutinized and classified as healthy or non-healthy based on lending data. Despite achieving a commendable 95% accuracy, the model exhibits a disparity in recall rates between healthy (0.99) and non-healthy loans (0.91), primarily stemming from data imbalance favoring healthy loans, which outnumber non-healthy ones substantially. This data imbalance is starkly evident, with healthy loans significantly outnumbering non-healthy ones in a ratio of 75036 to 2500. To mitigate this discrepancy, I implement RandomOverSampler to augment the minority class of non-healthy loans, thereby achieving a balanced dataset. The oversampled Logistic Regression Model boasts a superior 99% accuracy, coupled with an enhanced recall for non-healthy loans (0.99). This approach not only addresses the challenge of imbalance but also substantially improves the model's ability to identify non-healthy loans accurately, as evidenced by the confusion matrix outcomes.

- **Logistic Regression Model fitted with Imbalanced Data:**
  - Accuracy score: 95%
  - Precision score for healthy loans: 100%
  - Precision score for non-healthy loans: 85%
  - Recall score for healthy loans: 99%
  - Recall score for non-healthy loans: 91%
  
  **Logistic Regression Model fitted with Balanced (oversampled) Data:**
  - Accuracy score: 99%
  - Precision score for healthy loans: 100%
  - Precision score for non-healthy loans: 84%
  - Recall score for healthy loans: 99%
  - Recall score for non-healthy loans: 99%
 
- In the realm of lending, accurately categorizing loans as healthy or non-healthy holds immense significance, as misclassifications can incur substantial costs for the lending company. Misidentifying a healthy loan as non-healthy may result in customer loss, impacting the company's reputation and future prospects. Conversely, erroneously labeling a non-healthy loan as healthy could lead to financial losses for the lender, undermining profitability and sustainability. The Logistic Regression model trained on Oversampled data outperformed its Imbalanced counterpart, showcasing superior accuracy and recall rates. This indicates a marked reduction in misclassification errors, particularly crucial in minimizing False Positives, which pose a significant risk of fund loss for the lender. Examination of confusion matrices further elucidates this improvement: while Model 1 (fitted with Imbalanced Data) exhibited 56 False Positives, Model 2 (fitted with Balanced Data) slashed this number to a mere 4. Consequently, based on this comprehensive analysis, I strongly advocate for the adoption of Model 2 as the preferred solution for the lending company's classification needs.

**End of Credit Risk Analysis Report**

**Background**

In this Challenge, you'll employ various techniques to develop and assess a model for loan risk classification. Utilizing a dataset of historical lending activity from a peer-to-peer lending services company, the goal is to construct a model capable of discerning the creditworthiness of borrowers.

**Instructions**

The instructions for this Challenge are segmented as follows:

**Split the Data into Training and Testing Sets**

Open the provided notebook and execute the subsequent tasks:
- Read the lending_data.csv from the Resources folder into a Pandas DataFrame.
- Derive the labels set (y) from the “loan_status” column and form the features (X) DataFrame from the remaining columns.
- Split the dataset into training and testing subsets using train_test_split.

**Create a Logistic Regression Model**

Leverage logistic regression knowledge to accomplish the following:
- Train a logistic regression model using the training data (X_train and y_train).
- Predict the labels for the testing data by utilizing the testing feature data (X_test) and the trained model.
- Evaluate the model’s performance through:
  - Generation of a confusion matrix.
  - Printing of a classification report.
  - Addressing the question regarding the model's effectiveness in predicting both healthy (0) and high-risk (1) loans.

**Write a Credit Risk Analysis Report**

Compose a succinct report encompassing a summary and analysis of the machine learning models employed in this task. This report should be documented as the README.md file within your GitHub repository.
Ensure the report adheres to the provided template from Starter_Code.zip, incorporating the following elements:
- An overview of the analysis detailing its purpose.
- A bulleted list delineating the accuracy score, precision score, and recall score of the machine learning model.
- A summary encapsulating the results of the machine learning model along with justification for recommending or not recommending its use by the company.
