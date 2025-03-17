## Concepts

### The Curse of Dimensionality
Too many features can be a problem – leads to sparse data.
Unsupervised dimensionality reduction techniques can also be employed to distill may features to fewer features.
- PCA
- K-Means

## How do I handle missing data?

#### KNN: Find K “nearest” (most similar) rows and average their values
- Assumes numerical data, not categorical
- There are ways to handle categorical data (Hamming distance),

## but categorical data is probably better served by…

#### Deep Learning
- Build a machine learning model to impute data for your machine learning model!
- Works well for categorical data. Really well. But it’s complicated.

#### Regression
- Find linear or non-linear relationships between the missing feature and other features
- Most advanced technique: MICE (Multiple Imputation by Chained Equations)

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

### Choosing an activation function
- For multiple classification, use softmax on the output layer
- RNN’s do well with Tanh
- For everything else
  - Start with ReLU
  - If you need to do better, try Leaky ReLU
  - Last resort: PReLU, Maxout
  - Swish for really deep networks

### Specialized CNN architectures
Defines specific arrangement of layers, padding, and hyperparameters
- LeNet-5: Good for handwriting recognition
- AlexNet: Image classification, deeper than LeNet
- GoogLeNet: Even deeper, but with better performance. Introduces inception modules (groups of convolution layers)
- ResNet (Residual Network): Even deeper – maintains performance via skip connections.

## Tuning Neural Networks
- Small batch sizes tend to not get stuck in local minima
- Large batch sizes can converge on the wrong solution at
random
- Large learning rates can overshoot the correct solution
- Small learning rates increase training time


## Underfitting & Overfitting 

underfitting occurs when a model is too simple to capture the underlying patterns in the data, 
while overfitting happens when a model learns the training data too well, including noise and irrelevant details, leading to poor generalization to new, unseen data


### Regularization techniques to prevent Overfitting:
- Dropout
- Early Stopping (kitna hi train karoge bhai, ab rukh bhi jao)

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

### Ensemble methods
- XGBoost is the latest hotness
- Boosting generally yields better accuracy
- But bagging avoids overfitting
- Bagging is easier to parallelize
- So, depends on your goal

## Neural Topic Model

### Latent Dirichlet Allocation (LDA)
- Cluster customers based on purchases
- Harmonic analysis in music

### K-Nearest-Neighbors
- Find the K closest points to a sample point and return the average value

### K-Means
Divide data into K groups, where members of a group are as similar as possible to each other
- You define what “similar” means
- Measured by Euclidean distance

### Principal Component Analysis
Dimensionality reduction - Project higher-dimensional data (lots of features) into lower-dimensional (like a 2D plot) while minimizing loss of information

### IP Insights
- Identifies suspicious behavior from IP addresses

Markov decision processes (MDPs) provide a decision making mathematical framework for modeling decision making in situations random where outcomes are partly random and partly under the control of a decision maker.
