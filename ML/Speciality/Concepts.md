## Concepts

### TF-IDF matrix
Sentence 1: "Please call the number below"
Sentence 2: "Please do not call us"

If asked for (using both unigrams and bigrams)
UNIGRAMS (8 total):
| please | call | the | number | below | do | not | us

BIGRAMS (8 total):
| please call | call the | the number | number below | please do | do not | not call | call us

Total Features = 16 (8 unigrams + 8 bigrams) [(Number of unigrams + bigrams ..)]
Matrix Dimensions = (2 rows (Number of documents), 16 columns (Total Features) )

### Measuring your Models - [Never Forget Again! // Precision vs Recall with a Clear Example of Precision and Recall](https://www.youtube.com/watch?v=qWfzIYCvBqo)

#### Recall (Sensitivity)
```
Recall = TRUE POSITIVES / (TRUE POSITIVES + FALSE NEGATIVES)
```
- Also known as: Sensitivity, True Positive Rate, Completeness
- Measures: Percentage of positives correctly predicted
- Best used: When false negatives are costly
- Example application: Fraud detection

#### Precision
```
Precision = TRUE POSITIVES / (TRUE POSITIVES + FALSE POSITIVES)
```
- Also known as: Correct Positives
- Measures: Percentage of relevant results
- Best used: When false positives are costly
- Example applications: Medical screening, drug testing

#### Specificity
```
Specificity = TN / (TN + FP)
```
- Also known as: True Negative Rate

#### F1 Score
```
F1 = 2TP / (2TP + FP + FN)
```
- Alternative formula: `2 * (Precision * Recall) / (Precision + Recall)`
- Represents: Harmonic mean of precision and sensitivity
- Best used: When both precision and recall are important

## How to deal with Imbalanced datasets 

#### Undersampling:
This technique reduces the number of samples in the majority class to balance the dataset. 

    Example: Randomly removing instances from the majority class to match the number of instances in the minority class. 

Pros: Can help prevent models from being biased towards the majority class. 
Cons: Can lead to loss of potentially valuable information if important instances are removed. 

#### Oversampling:
This technique increases the number of samples in the minority class to balance the dataset. 

    Example: Randomly duplicating instances from the minority class or generating synthetic samples. 

Pros: Can help prevent models from being biased towards the majority class. 
Cons: Can lead to overfitting if the minority class is oversampled excessively. 

#### SMOTE (Synthetic Minority Over-sampling Technique):
A specific oversampling technique that generates synthetic samples for the minority class by interpolating between existing minority class instances. 

    How it works: SMOTE identifies the nearest neighbors of each minority class instance and creates new synthetic instances along the line connecting these neighbors. 

Pros: Can help create a more balanced dataset without simply duplicating existing instances. 
Cons: Can potentially introduce noisy samples if not implemented carefully, and may not be suitable for all datasets. 

## How do I handle missing data?

#### KNN: Find K “nearest” (most similar) rows and average their values
- Assumes numerical data, not categorical
- There are ways to handle categorical data (Hamming distance), but categorical data is probably better served by…

#### Deep Learning
- Build a machine learning model to impute data for your machine learning model!
- Works well for categorical data. Really well. But it’s complicated.

#### Regression
- Find linear or non-linear relationships between the missing feature and other features
- Most advanced technique: MICE (Multiple Imputation by Chained Equations)
