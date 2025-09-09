## Problem 1: High Value on 4th Roll

### Question:

A fair die is rolled repeatedly until a number larger than 4 is observed.

*What's the probability that it takes you 4 rolls to roll a number greater than 4?*

### Answer:

What is the probability of 3 rolls less than or equal to 4, followed by 1 roll greater than 4?
- $P(\text{<=4}) = 2/3$
- $P(\text{>4}) = 1/3$

Probability:
$$P(\text{3 low, 1 high}) = \left( \frac{2}{3} \right)^3 * \frac{1}{3} = \frac{8}{81}$$

## Problem 2: Two Consecutive Sixes

### Question:
Say you roll a die three times. 

*What is the probability of getting two sixes in a row?*

### Answer (specific):
**Favorable Cases:**
- 6, 6, 6 (1)
- 6, 6, X (5 because X can be 1-5)
- X, 6, 6 (5 because X can be 1-5)

$$\text{Favorable Cases} = 11$$

**Total Cases:**
- Permutations, ordered with replacement: $n^r $
- $n=6, r=3$

$$\text{total cases} = 6^3 = 216$$

**Probability:**

$$P(\text{Two 6's in a row}) = \frac{11}{216}$$

### Answer (general):

There are only two ways for 6's to be consecutive:
- Pair happens on rolls 1 and 2
- Pair happens on rolls 2 and 3
- All three are 6's

In the first case with exactly two 6's:

$$2 * \left( \frac{1}{6} \right) ^2 + \left(\frac{5}{6} \right) = \frac{10}{216}$$

In the special case with all three 6's:

$$\left( \frac{1}{6} \right) ^3 = \frac{1}{216}$$

Altogether:

$$P(\text{Two 6's in a row}) = \frac{11}{216}$$

## Problem 3: Seven Game Series

### Question:

Two teams play a series of games (best of 7) in which each team has a 50% chance of winning any given round. 

*What is the probability that the series goes to 7 games?*

### Answer:

**Favorable Outcomes:**
- Each team needs to win 3 games of 6
- We can think of this as a binomial series
    - Outcome 1 = team A, 0 = team B
- Not removing outcomes, repeatedly sampling
- Position doesn't matter of team A winning
- Use combination without replacement

$$\text{favorable} = \binom{6}{3} = 20$$

**Total Outcomes**
- two possible outcomes
- order does matter because distinct sequence of outcomes

$$\text{total} = 2^6$$

**Probability**

$$P(\text{7 game series}) = \frac{\binom{6}{3}}{2^6} = \frac{20}{64}$$

## Problem 4: Increasing Dice Rolls

### Question:
You roll three dice, one after another. 

*What is the probability that you obtain three numbers in a strictly increasing order?*


### Answer (Specific):
Favorable cases based on first roll:
- 6 = 0
- 5 = 0
- 4 = 1, (4,5,6)
- 3 = 3, (3,4,5), (3,4,6), +1
- 2 = 6, (2,3,4),(2,3,5),(2,3,6),+ 3
- 1 = 10, (1,2,3), (1,2,4), (1,2,5), (1,2,6) + 6

$$ \text{favorable} = 20$$

Total cases:
- Ordered with Replacement: $n^r$
- $n=6, r=3$

$$\text{total} = 216$$

**Probability:**

$$P(\text{increasing dice rolls}) = \frac{20}{216}$$

### Answer (General):

In order to be increasing, the three rolls must all yield different numbers.

$$P(\text{different}) = \left( \frac{6}{6} \right) * \left( \frac{5}{6} \right) * \left( \frac{4}{6} \right) = \frac{20}{36} = \frac{5}{9}$$

There are $3!$ ways to order 3 numbers:

$$3! = 3 * 2 * 1 = 6$$

Since the numbers are unique, there is only one way to order them in ascending order.

$$P(\text{ascending}) = \frac{1}{6}$$

**Probability:**

$$P(\text{increasing dice rolls}) = \frac{5}{9} * \frac{1}{6} = \frac{5}{54} = \frac{20}{216}$$

## Problem 5: Lazy Reviewers

### Question:
Suppose 80% of Netflix users rate movies thumbs up 60% of the time, and thumbs down 40% of the time. However, 20% of Netflix users are "lazy": they rate 100% of the movies they watch as good!

*Given that someone gives 3 movies IN A ROW a thumbs up, what's the probability they are a "lazy" rater?*

### Answer:

**Bayes Theorem:**

$$P(\text{lazy } | \text{ 3 good}) = \frac{P(\text{3 good } | \text{ lazy}) * P(\text{lazy})}{P(\text{3 good})}$$

**Priors:**
- $P(\text{lazy}) = 0.2$
- $P(\text{normal}) = 0.8$

**Likelihood:**
- $P(\text{good } | \text{ normal}) = 0.6$
- $P(\text{good } | \text{ lazy}) = 1.0$
- $P(\text{3 good } | \text{ lazy}) = 1^3 = 1$
- $P(\text{3 good } | \text{ normal}) = 0.6^3 = 0.216$

**Probability of Evidence**
- $P(\text{3 good}) = P(\text{3 good } | \text{ lazy}) * P(\text{lazy}) + P(\text{3 good } | \text{ normal}) * P(\text{normal})$

$$P(\text{3 good}) = (1.0 * 0.2) + (0.216 * 0.8) \approx{0.3728}$$

**Solution:**

$$P(\text{lazy } | \text{ 3 good}) = \frac{1.0 * 0.2}{0.3728} \approx{0.536}$$

## Problem 6: Intersecting Chords

### Question:

You draw a circle and choose two chords at random. 

*What is the probability that those chords will intersect?*

### Answer (Specific):

Assume there are 4 points: $A_1, B_1, A_2, B_2$.

The $A_1$ and $A_2$ points are connected as a chord, and the $B_1$ and $B_2$ points are connected as a chord.

The chords will intersect only if the points alternate as one goes along the circle clockwise. For example: $(A_1, B_2, A_2, B_1)$

**Total combinations of points:**

$$\text{total combinations} = 4! = 4 * 3 * 2 * 1 = 24$$

**Alternating combinations:**
- $(A_1,B_1,A_2,B_2)$
- $(A_2,B_1,A_1,B_2)$
- $(A_2,B_2,A_1,B_1)$
- $(A_1,B_2,A_2,B_1)$
- $(B_1,A_1,B_2,A_2)$
- $(B_2,A_1,B_1,A_2)$
- $(B_2,A_2,B_1,A_1)$
- $(B_1,A_2,B_2,A_1)$

$$\text{favorable combinations} = 8$$

**Solution:**

$$P(\text{intersect}) = \frac{8}{24} = \frac{1}{3}$$

### Answer (General):

**Step 1: Total ways to choose chords**

We have 4 points on the circle. Label the 4 points clockwise as $P_1, P_2, P_3, P_4$.  

To form two chords, we need to pair these 4 points into 2 pairs.  

The number of distinct pairings is:  

$$
\frac{1}{2} \binom{4}{2} = \frac{1}{2} \cdot 6 = 3
$$

- First chord: choose any 2 of the 4 points
- Second chord is then determined by the remaining 2 points
- The $\frac{1}{2}$ is because the order of the pairs doesn't matter

**Step 2: When do chords intersect?**

- Chords $(P_1,P_2)$ and $(P_3,P_4)$: do **not** intersect  
- Chords $(P_1,P_3)$ and $(P_2,P_4)$: **do** intersect  
- Chords $(P_1,P_4)$ and $(P_2,P_3)$: do **not** intersect  

So out of 3 possible pairings, exactly 1 leads to intersection.

**Step 3: Probability**

$$P(\text{intersect}) = \frac{1}{3}$$

## Problem 7: Consecutive 5's

### Question:

Say you’re rolling a fair six-sided die. 

*What is the expected number of rolls until you get two consecutive 5s?*

### Answer (Specific):
- Warning this solution only works for length 2 patterns (e.g. 5,5 4,5 etc.).
- For length 3+, a Markov Chain approach is necessary

The probability of rolling a five is $1/6$
- $P(5) = \frac{1}{6}$

The expected number of rolls to roll a 5 is 6
- Geometric distribution
- $E[5] = \frac{1}{p} = \frac{1}{\frac{1}{6}} = 6$

The expected number of rolls to complete a trial is 7
- A trial is a set of rolls until a 5 is rolled, followed by the attempt at a second 5 
- $E[\text{rolls in trial}] = E[5] + 1 = 6 + 1 = 7$
 
The probability of a trial succeeding is also $1/6$
- Geometric Distribution
- $E[\text{num trials}] = \frac{1}{p} = \frac{1}{\frac{1}{6}} = 6$

The expected number of rolls is 42
- $6 \text{ trials} * 7 \text{ rolls per trial} = 42 \text{ rolls}$

### Answer (General)

We model this as a Markov chain.

We want the expected number of rolls of a fair die until the sequence **(5,5)** appears.

#### Step 1. Define states

States:
- **$S_0$**: No progress (last roll not a 5).  
- **$S_1$**: One 5 has been rolled (waiting for another 5).  
- **$S_2$**: Success (two consecutive 5s).  

Let $E_0$ and $E_1$ be the expected rolls to reach $S_2$ starting from $S_0$ and $S_1$, respectively. We want $E_0$.

#### Step 2. Define Expected Values

**From $S_0$:**
$$
E_0 = 1 + \tfrac{1}{6}E_1 + \tfrac{5}{6}E_0
$$

- One roll is spent resulting in a $5/6$ chance of re-entering $S_0$, or a $1/6$ chance of entering $S_1$
- By entering $S_0$ or $S_1$, you will accumulate the additional expected value of $E_0$ or $E_1$

Rearrange:
$$
E_0 = 6 + E_1
$$

**From $S_1$:**
$$
E_1 = 1 + \tfrac{1}{6}(0) + \tfrac{5}{6}E_0
$$

One roll is spent resulting in a $5/6$ chance of entering $S_0$ and a $1/6$ chance of entering $S_2$ (success).

So:
$$
E_1 = 1 + \tfrac{5}{6}E_0
$$

#### Step 3. Solve system

Substitute into $E_0 = 6 + E_1$:
$$
E_0 = 6 + \Big(1 + \tfrac{5}{6}E_0\Big)
$$

$$
E_0 = 7 + \tfrac{5}{6}E_0
$$

$$
E_0 - \tfrac{5}{6}E_0 = 7
$$

$$
\tfrac{1}{6}E_0 = 7
$$

$$
E_0 = 42
$$