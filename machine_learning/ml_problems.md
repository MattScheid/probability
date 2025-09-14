## Problem 1: Bias Variance Tradeoff

### Question  
Explain the bias–variance tradeoff.

### Answer  

**Description:**  
- **Bias** measures error introduced by oversimplifying the model. High-bias models tend to underfit because they make strong assumptions and fail to capture the underlying patterns.  
- **Variance** measures error introduced by sensitivity to small fluctuations in the training data. High-variance models tend to overfit because they learn noise rather than the true signal.  

**Formulas (conceptual):**  
- Expected squared error can be decomposed as:  
  $\text{Error} = \text{Bias}^2 + \text{Variance} + \text{Irreducible Noise}$

**Importance:**  
- Bias and variance capture two fundamental sources of prediction error.  
- Understanding the tradeoff helps in selecting models and tuning complexity: too simple → high bias, too complex → high variance.  

**Tradeoff:**  
- Reducing bias typically increases variance, and reducing variance typically increases bias.  
- The goal is to find the *sweet spot* where both are balanced to minimize total error.  
- Example:  
  - A linear regression on a highly nonlinear dataset → high bias, low variance.  
  - A very deep decision tree → low bias, high variance.  
  - A well-regularized model (e.g., random forest or ridge regression) can balance both.  


## Problem 2: Precision and Recall

### Question  
Describe precision and recall and give their formulas. What is their importance and what is the nature of the tradeoff between the two?

### Answer  

**Description:**  
- **Precision** is the fraction of predicted positives that are actually correct. A model with high precision rarely makes false positive errors.  
- **Recall** is the fraction of actual positives that the model successfully identifies. A model with high recall rarely misses positive cases (few false negatives).  

**Formulas:**  
- $\text{Precision} = \frac{TP}{TP + FP}$
- $\text{Recall} = \frac{TP}{TP + FN}$

**Importance:**  
- Precision tells us *how reliable* the positive predictions are.  
- Recall tells us *how complete* the positive predictions are.  
- Both are needed because in many applications, the costs of false positives and false negatives are very different.  

**Tradeoff:**  
- Precision and recall often move in opposite directions: if you increase recall (by predicting positive more often), precision tends to drop, and vice versa.  
- The right balance depends on the application. For example, in cancer detection we may prioritize recall (catch every possible case), whereas in spam filtering we may prioritize precision (avoid flagging legitimate emails).  

#### Todo:
- F1 Score