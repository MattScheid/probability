# Probability & Statistics Symbols Cheat Sheet

This sheet translates common mathematical symbols into plain English. Useful for quickly refreshing notation while preparing for technical interviews.

---

## 1. Probability & Logic Symbols

- **Event probability:**  
  `P(A)` → Probability of event **A**
  $$P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}$$

- **Conditional probability:**  
  `P(A | B)` → Probability of **A given B**
  $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

- **Intersection (AND):**  
  `A ∩ B` → Both events **A and B** occur
  - If independent
  $$P(A \cap B) = P(A) \cdot P(B)$$
  - If dependent:
  $$P(A \cap B) = P(A) \cdot P(B|A)$$

- **Union (OR):**  
  `A ∪ B` → Event **A or B or both** occur

- **Complement:**  
  `A^c` or `¬A` → Event **A does not occur**

- **Mutual exclusivity:**  
  `A ∩ B = ∅` → Events **A and B cannot happen together**

- **Sample space:**  
  `Ω` → Set of all possible outcomes

- **Element of:**  
  `x ∈ A` → **x is an element of set A**

---

## 2. Random Variables & Expectation

- **Random variable (capital letter):**  
  `X` → A variable representing outcomes of a random process

- **Specific value of random variable (lowercase):**  
  `x` → Realized value of **X**

- **Expectation / Mean:**  
  `E[X]` → Expected value (average) of random variable **X**

- **Variance:**  
  `Var(X) = E[(X - E[X])^2]` → Spread of **X** around its mean

- **Standard deviation:**  
  `σ_X = sqrt(Var(X))` → Typical deviation of **X** from its mean

- **Covariance:**  
  `Cov(X,Y) = E[(X - E[X])(Y - E[Y])]` → How **X** and **Y** vary together

- **Correlation:**  
  `ρ_{X,Y} = Cov(X,Y) / (σ_X σ_Y)` → Strength of linear relationship between **X** and **Y**

---

## 3. Probability Distributions

- **Probability mass function (PMF):**  
  `P(X=x)` → Probability that discrete random variable **X** equals **x**

- **Probability density function (PDF):**  
  `f(x)` → Likelihood of **X** taking values near **x** (continuous)

- **Cumulative distribution function (CDF):**  
  `F(x) = P(X ≤ x)` → Probability that **X** is less than or equal to **x**

- **Quantile function (inverse CDF):**  
  `F^{-1}(p)` → Value **x** such that `P(X ≤ x) = p`

---

## 4. Summation & Products

- **Summation:**  
  `Σ_{i=1}^n a_i` → Add up terms `a_1 + a_2 + ... + a_n`

- **Product:**  
  `Π_{i=1}^n a_i` → Multiply terms `a_1 * a_2 * ... * a_n`

---

## 5. Combinatorics & Factorials

- **Factorial:**  
  `n! = n * (n-1) * (n-2) ... * 1` → Number of ways to arrange **n*

## 6. Bayes Theorem
- **Bayes’ theorem:**  
  $$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$