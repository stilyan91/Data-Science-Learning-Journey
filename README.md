# Data Science Learning Journey

This repository documents my practical journey toward improving my **data analysis, statistics, mathematics, and data visualization skills**.

Rather than only studying theory, I use small exercises and datasets to practice each concept with Python and explain what I learn from the results.

The difficulty of the exercises gradually increases as my understanding improves.

## Learning Goals

The main goals of this repository are to strengthen my skills in:

- Python for data analysis

- Pandas

- NumPy

- Matplotlib

- Exploratory Data Analysis (EDA)

- Data cleaning and transformation

- Data visualization

- Descriptive statistics

- Probability

- Statistical inference

- Hypothesis testing

## Statistics Roadmap

The statistics exercises will gradually progress through:

1. Percentages and percentage points

2. Mean, median, and mode

3. Range and quartiles

4. Interquartile range (IQR)

5. Variance

6. Standard deviation

7. Outlier detection

8. Basic probability

9. Probability rules

10. Conditional probability

11. Independent events

12. Correlation

13. Probability distributions

14. Normal distribution

15. Z-scores

16. Sampling and sampling distributions

17. Central Limit Theorem

18. Confidence intervals

19. Hypothesis testing

20. Z-tests

21. T-tests

22. Chi-square tests

23. Basic regression

The goal is not simply to memorize formulas, but to understand **when a statistical method should be used and how to interpret its result**.

## Data Visualization Roadmap

Visualization exercises primarily use **Matplotlib**.

Topics include:

- Bar charts

- Line charts

- Histograms

- Box plots

- Scatter plots

- Distribution visualization

- Outlier visualization

- Time-series visualization

- Correlation visualization

- Statistical visualization

- Choosing the appropriate chart for a problem

- Communicating findings clearly


# Practice 01 — Math, Statistics & Visualization Fundamentals

The first practice focused on fundamental descriptive statistics, basic probability, and introductory data visualization.

## Mathematics & Statistics

Topics practiced:

- Percentages

- Percentage-point changes

- Percentage increases

- Mean

- Median

- Range

- Quartiles

- Interquartile range (IQR)

- Outlier detection using the 1.5 × IQR rule

- Basic probability

- Complement rule

- Mutually exclusive events

- Independent events

## Visualization

Charts practiced:

- Bar chart

- Line chart

- Histogram

- Box plot

- Scatter plot selection

The exercises also focused on understanding **why a particular visualization is appropriate**, rather than only learning Matplotlib syntax.

## Key Lessons From Practice 01

### Mean vs Median

The mean can be strongly affected by extreme values, while the median is more resistant to outliers.

### Percentage vs Percentage Points

An increase from 73% to 80% is:

- **7 percentage points**

- approximately **9.6% relative increase**

These describe different types of change.

### IQR and Outliers

The interquartile range describes the spread of the middle 50% of observations.

Potential outliers can be detected using:

`Lower boundary = Q1 - 1.5 × IQR`

`Upper boundary = Q3 + 1.5 × IQR`

### Probability

For an event A:

`P(not A) = 1 - P(A)`

For two independent events A and B:

`P(A and B) = P(A) × P(B)`

Independent events should not be confused with mutually exclusive events.

### Histograms

Changing the number of bins can significantly change how a distribution appears, even though the underlying data remains unchanged.

### Box Plots

A box plot provides a compact representation of:

- Q1

- Median

- Q3

- IQR

- Whiskers

- Potential outliers

### Choosing Visualizations

| **Question** | **Visualization** |
| :-: | :-: |
| Compare categories | Bar chart |
| Analyze change over time | Line chart |
| Examine a distribution | Histogram |
| Detect potential outliers | Box plot |
| Examine two numerical variables | Scatter plot |


# Practice 02 — Variability, Probability & Relationships

Practice 02 expanded on the fundamentals by introducing **variance, standard deviation, conditional probability, and correlation**.

The main goal was to understand not only where data is centered, but also **how much it varies and how variables may be related**.

## Variance and Standard Deviation

Two datasets can have the same mean while behaving very differently.

For example, two hotels may both have an average daily revenue of £15,000, while one has very stable revenue and the other experiences large daily fluctuations.

This demonstrated why the mean alone is not sufficient to describe a dataset.

### Population Variance

Population variance measures the average squared deviation from the population mean:

`variance = sum((x - μ)²) / N`

### Population Standard Deviation

Standard deviation is the square root of variance:

`σ = sqrt(variance)`

Standard deviation is easier to interpret because it uses the **same units as the original data**.

For example, if:

`standard deviation = £3,010`

then daily revenue typically varies on roughly that scale around its mean.

## Why Deviations Are Squared

Simply adding deviations from the mean would cause positive and negative deviations to cancel each other.

Squaring the deviations:

- removes negative signs

- prevents cancellation

- gives greater weight to observations farther from the mean

## Population vs Sample Variance

An important distinction introduced in Practice 02 was:

`Population variance → divide by N`

`Sample variance → divide by n - 1`

When a sample is used to estimate population variability, dividing by `n - 1` helps correct the tendency to underestimate the population variance.

This is known as **Bessel's correction**.

With NumPy:

```
`\# Population`

`np.var(data)`

`np.std(data)`


`\# Sample`

`np.var(data, ddof=1)`

`np.std(data, ddof=1)`
```

## Probability — Union and Intersection

Two important probability symbols were introduced:

`A ∩ B` → A **AND** B

`A ∪ B` → A **OR** B

For events that can overlap:

`P(A ∪ B) = P(A) + P(B) - P(A ∩ B)`

The intersection must be subtracted because otherwise observations belonging to both groups would be counted twice.

If two events are mutually exclusive:

`P(A ∩ B) = 0`

and therefore:

`P(A ∪ B) = P(A) + P(B)`

## Conditional Probability

Conditional probability asks for the probability of an event when some information is already known.

For example:

`P(Cancelled | Mobile)`

means:

> What is the probability that a booking is cancelled, given that we already know it was made on mobile?

The important lesson was that the denominator changes.

Instead of considering every booking, we only consider bookings satisfying the given condition.

Example:

`120 cancelled mobile bookings / 600 mobile bookings = 0.20`

Therefore:

`P(Cancelled | Mobile) = 20%`

## Independence

If two events A and B are independent:

`P(A | B) = P(A)`

Knowing that B occurred does not change the probability of A.

This provides a useful way of thinking about whether two variables may be related.

The concepts of conditional probability and independence will later connect to **chi-square tests of independence**.

## Scatter Plots

Scatter plots were introduced for examining relationships between two numerical variables.

Example:

`Occupancy (%) → x-axis`

`Revenue (GBP) → y-axis`

A scatter plot can help identify:

- Positive relationships

- Negative relationships

- Weak relationships

- Strong relationships

- Potential outliers

- Nonlinear patterns

## Correlation

Pearson's correlation coefficient was introduced to quantify the strength and direction of a **linear relationship** between two numerical variables.

The coefficient ranges from:

`-1 ≤ r ≤ +1`

General interpretation:

| Correlation | **Interpretation** |
| -: | :-: |
| close to +1 | Strong positive linear relationship |
| close to 0 | Weak or no linear relationship |
| close to -1 | Strong negative linear relationship |

The **sign** indicates direction.

The **absolute value** indicates strength.

Therefore:

`r = -0.95`

represents a stronger linear relationship than:

`r = +0.70`

even though the first correlation is negative.

With NumPy:

```
`correlation\_matrix = np.corrcoef(x, y)`

`correlation = correlation\_matrix\[0, 1\]`
```

The diagonal of the correlation matrix contains `1` because every variable is perfectly correlated with itself.

## Correlation Does Not Imply Causation

One of the most important lessons from Practice 02 was:

> **Correlation does not imply causation.**

If occupancy and revenue have a strong positive correlation, we can say:

> Higher occupancy is **associated with** higher revenue.

We cannot conclude from correlation alone that:

> Higher occupancy **causes** higher revenue.

Other variables such as season, room prices, hotel size, promotions, holidays, and events could influence both variables.


# Key Lessons From Practice 02

- Mean describes the center but does not describe variability.

- Range gives a simple measure of spread but only considers the minimum and maximum.

- Variance measures average squared deviation from the mean.

- Standard deviation expresses variability in the original unit of measurement.

- Population variance uses `N`.

- Sample variance uses `n - 1`.

- `∩` means intersection / AND.

- `∪` means union / OR.

- Overlapping events must not be counted twice.

- Conditional probability changes the population being considered.

- Independent events do not change each other's probabilities.

- Scatter plots are useful for examining relationships between numerical variables.

- Correlation measures the direction and strength of a linear relationship.

- The sign of correlation determines direction.

- The absolute value of correlation determines strength.

- A correlation close to zero means little or no **linear** relationship.

- Correlation does not prove causation.

- Small datasets should be interpreted cautiously when assessing distributions.


# Repository Structure

```
`data-science-learning-journey/`

`│`

`├── README.md`

`│`

`├── eda/`

`│   ├── practice-01/`

`│   ├── practice-02/`

`│   └── ...`

`│`

`├── math-statistics/`

`│   ├── practice-01.ipynb`

`│   ├── practice-02.ipynb`

`│   └── ...`

`│`

`├── visualization/`

`│   └── ...`

`│`

`└── projects/`
```

The structure may evolve as the repository grows.

## Tools

The exercises primarily use:

- Python

- Jupyter Lab / Jupyter Notebook

- Pandas

- NumPy

- Matplotlib

Additional statistical libraries will be introduced as the exercises become more advanced.

## Learning Approach

For each exercise I try to:

1. Solve the problem myself.

2. Write the Python implementation.

3. Understand the mathematics behind the result.

4. Visualize the data when appropriate.

5. Explain the result in my own words.

6. Identify and understand mistakes.

7. Correct the solution rather than simply replacing it.

8. Connect new concepts to previously learned concepts.

The notebooks intentionally preserve the progression from beginner exercises toward more advanced statistical and data-analysis problems.

## Current Progress

### Math, Statistics & Visualization

- Practice 01 — Fundamentals

- Practice 02 — Variance, standard deviation, probability rules and relationships

- Practice 03 — Normal distribution and z-scores

- Sampling and standard error

- Central Limit Theorem

- Confidence intervals

- Z-tests

- T-tests

- Chi-square tests

### Exploratory Data Analysis

- EDA Practice 01 — Hotel-chain dataset

- Additional beginner EDA practice

- Intermediate EDA

- Advanced EDA

## Next Step

The next statistics practice will focus on:

**Normal Distribution and Z-Scores**

This will introduce:

- Properties of the normal distribution

- Mean and standard deviation in a normal distribution

- The 68–95–99.7 rule

- Standardization

- Z-scores

- Interpreting positive and negative z-scores

- Comparing observations from different distributions

- Visualizing normal distributions

These concepts will form the foundation for later topics:

`Normal Distribution → Z-Scores → Sampling Distributions → Central Limit Theorem → Confidence Intervals → Hypothesis Testing`

## Purpose

This repository is both a **learning journal and practical portfolio**.

It shows not only finished solutions, but the progression of my understanding as I learn how to explore data, apply statistics, choose appropriate visualizations, identify mistakes, and communicate conclusions from data.

