## Concepts

## TF-IDF matrix
Sentence 1: "Please call the number below"
Sentence 2: "Please do not call us"

If asked for (using both unigrams and bigrams)
UNIGRAMS (8 total):
| please | call | the | number | below | do | not | us

BIGRAMS (8 total):
| please call | call the | the number | number below | please do | do not | not call | call us

Total Features = 16 (8 unigrams + 8 bigrams) [(Number of unigrams + bigrams ..)]
Matrix Dimensions = (2 rows (Number of documents), 16 columns (Total Features) )

## Measuring your Models

### Recall (Sensitivity)
```
Recall = TRUE POSITIVES / (TRUE POSITIVES + FALSE NEGATIVES)
```
- Also known as: Sensitivity, True Positive Rate, Completeness
- Measures: Percentage of positives correctly predicted
- Best used: When false negatives are costly
- Example application: Fraud detection

### Precision
```
Precision = TRUE POSITIVES / (TRUE POSITIVES + FALSE POSITIVES)
```
- Also known as: Correct Positives
- Measures: Percentage of relevant results
- Best used: When false positives are costly
- Example applications: Medical screening, drug testing

### Specificity
```
Specificity = TN / (TN + FP)
```
- Also known as: True Negative Rate

### F1 Score
```
F1 = 2TP / (2TP + FP + FN)
```
- Alternative formula: `2 * (Precision * Recall) / (Precision + Recall)`
- Represents: Harmonic mean of precision and sensitivity
- Best used: When both precision and recall are important
