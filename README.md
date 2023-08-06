# Credit-Risk-Classification
## Overview of the Analysis

The purpose of this analysis was to train and evaluate a model based on loan risk. Historical lending activity from a peer-to-peer lending services company was used to train the model, and the model was trying to predict the creditworthiness of potential borrowers. Specifically, the model was looking for a value of `0` or `1` in the "loan_status" column of the data, which determined if a loan was healthy (0) or if it had a high risk of defaulting (1).

First, the data was split into training and testing datasets based on the "loan_status" column using `train_test_split`. The trained data was then fit into a `LogisticRegression` model, to which predictions were then made based off the testing data.
>As soon evidenced by the high accuracy, precision, recall and F1-score on this problem, logistic regression achieved a strong predictive performance sufficient for this real-world need. For an initial model on a binary classification task like credit risk assessment, logistic regression was a solid practical choice, especially given the simplicity of the data.

Then the model's performance was evaluated by generating a `confusion matrix` adding significant transparency for error analysis, and printing a `classification report` to complement the confusion matrix to provide a deeper performance profile.


## Results

* Machine Learning Model:
    - For the 0 (healthy loan) class:
        - Precision is 1.00 - the model is very good at predicting only the relevant 0 labels and has no false positives
        - Recall is 0.99 - the model predicts 99% of the actual 0 labels correctly
        - F1-score is 1.00 - also indicating strong performance on the 0 class

    - For the 1 (high-risk loan) class:
        - Precision is 0.85 - lower than 0 class, but still reasonably good at predicting only relevant 1 labels
        - Recall is 0.91 - model predicts 91% of actual 1 labels correctly
        - F1-score is 0.88 - decent performance on the 1 class

    - Accuracy and Macro Avg - the model achieves 99% overall accuracy, with macro avg scores of 0.92 precision, 0.95 recall and 0.94 F1-score.

## Summary

In summary, the model generally predicts both the 0 and 1 classes very well, with slightly better performance on the majority 0 class. The high precision, recall and F1-scores on both indicates the model is successful at predicting each class correctly overall. The model's performance does depend on the specific problem being solved - the characteristics of the problem such as complexity, available data, noise, and the choice of performance metric seem to all interact to determine how well a model can learn to solve that problem. Simpler, cleaner problems with more data appear easier to model effectively.

The high performance on both precision and recall for this model make it potentially well-suited for this use case (assessing credit risk). The high performance across initial metrics is promising for assessing credit risk, but I would recommend further validation on new data, testing across different decision thresholds, and implementing monitoring/retraining before fully deploying the model. But because the initial results look positive, I would recommend the model for further testing.
