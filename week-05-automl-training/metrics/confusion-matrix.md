# Confusion Matrix

|                     | Predicted: Phishing | Predicted: Legitimate |
|---------------------|--------------------|-----------------------|
| Actual: Phishing    | TP = 5             | FN = 0                |
| Actual: Legitimate  | FP = 0             | TN = 5                |

# Metrics

- Accuracy: 100%
- Precision: 100%
- Recall: 100%
- F1 Score: 100%

# Interpretation

The model correctly classified all phishing and legitimate email screenshots in the test dataset. This resulted in perfect accuracy, precision, recall, and F1 score for the limited sample size used in testing. However, because the dataset was relatively small, additional training data and more diverse phishing examples would likely be necessary for reliable real-world deployment.
