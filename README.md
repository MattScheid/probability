# probability
Probability and combinatorics

# Probability Cheat Sheet

This document provides a quick reference for probability concepts commonly tested in technical interviews. It covers foundational principles, combinatorics, and selection rules (ordered vs unordered, with vs without replacement).

---

## 1. Probability Basics

- **Probability of an event (A):**  
  $$P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}$$

- **Complement rule:**  
  $$P(A^c) = 1 - P(A)$$

- **Union (Addition rule):**  
  $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

- **Intersection (Multiplication rule):**  
  - If independent:  
    $$P(A \cap B) = P(A) \cdot P(B)e$$
  - If dependent:  
    $$P(A \cap B) = P(A) \cdot P(B|A)$$

- **Conditional probability:**  
  $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

- **Bayes’ theorem:**  
  $$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

---

## 2. Counting & Combinatorics

Combinatorics defines how we count arrangements or selections. The rules depend on **order** and **replacement**.

### Factorials
- Definition:  
  $$n! = n \cdot (n-1) \cdot (n-2) \cdots 1$$
- Special case:  
  $$0! = 1$$

### Permutations (Ordered Selections)
Number of ways to arrange $r$ items from $n$ distinct objects.

- **Without replacement (no repeats):**  
  $$P(n,r) = \frac{n!}{(n-r)!}$$

- **With replacement (repeats allowed):**  
  $$n^r$$

### Combinations (Unordered Selections)
Number of ways to choose $r$ items from $n$, disregarding order.

- **Without replacement:**  
  
