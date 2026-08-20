# Data Science Learning Journey

This repository documents my practical journey toward improving my **data analysis, statistics, mathematics, and data visualization skills**.

Rather than only studying theory, I use small exercises and datasets to practice each concept with Python and explain what I learn from the results.

The difficulty of the exercises gradually increases as my understanding improves.

## Learning Goals

The main goals of this repository are to strengthen my skills in:

* Python for data analysis
* Pandas
* NumPy
* Matplotlib
* Exploratory Data Analysis (EDA)
* Data cleaning and transformation
* Data visualization
* Descriptive statistics
* Probability
* Statistical inference
* Hypothesis testing

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
12. Probability distributions
13. Normal distribution
14. Z-scores
15. Sampling and sampling distributions
16. Central Limit Theorem
17. Confidence intervals
18. Hypothesis testing
19. Z-tests
20. T-tests
21. Chi-square tests
22. Correlation
23. Basic regression

The goal is not simply to memorize formulas, but to understand **when a statistical method should be used and how to interpret its result**.

## Data Visualization Roadmap

Visualization exercises primarily use **Matplotlib**.

Topics include:

* Bar charts
* Line charts
* Histograms
* Box plots
* Scatter plots
* Distribution visualization
* Outlier visualization
* Time-series visualization
* Correlation visualization
* Statistical visualization
* Choosing the appropriate chart for a problem
* Communicating findings clearly

## Practice 01 — Math, Statistics & Visualization Fundamentals

The first practice focuses on fundamental concepts.

### Mathematics & Statistics

Topics practiced:

* Percentages
* Percentage-point changes
* Percentage increases
* Mean
* Median
* Range
* Quartiles
* Interquartile range (IQR)
* Outlier detection using the 1.5 × IQR rule
* Basic probability
* Complement rule
* Mutually exclusive events
* Independent events

### Visualization

Charts practiced:

* Bar chart
* Line chart
* Histogram
* Box plot
* Scatter plot selection

The exercises also focus on understanding **why a particular visualization is appropriate**, rather than only learning the Matplotlib syntax.

## Key Lessons From Practice 01

Some of the most important concepts I learned were:

### Mean vs Median

The mean can be strongly affected by extreme values, while the median is more resistant to outliers.

### Percentage vs Percentage Points

An increase from 73% to 80% is:

* **7 percentage points**
* approximately **9.6% relative increase**

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

* Q1
* Median
* Q3
* IQR
* Whiskers
* Potential outliers

### Choosing Visualizations

A useful starting point is:

| Question                        | Visualization |
| ------------------------------- | ------------- |
| Compare categories              | Bar chart     |
| Analyze change over time        | Line chart    |
| Examine a distribution          | Histogram     |
| Detect potential outliers       | Box plot      |
| Examine two numerical variables | Scatter plot  |

## Repository Structure

```text
data-science-learning-journey/
│
├── README.md
│
├── eda/
│   ├── practice-01/
│   ├── practice-02/
│   └── ...
│
├── math-statistics/
│   ├── practice-01/
│   ├── practice-02/
│   └── ...
│
├── visualization/
│   ├── practice-01/
│   ├── practice-02/
│   └── ...
│
└── projects/
```

The structure may evolve as the repository grows.

## Tools

The exercises primarily use:

* Python
* Jupyter Lab / Jupyter Notebook
* Pandas
* NumPy
* Matplotlib

Additional statistical libraries may be introduced as the exercises become more advanced.

## Learning Approach

For each exercise I try to:

1. Solve the problem myself.
2. Write the Python implementation.
3. Understand the mathematics behind the result.
4. Visualize the data when appropriate.
5. Explain the result in my own words.
6. Review mistakes and improve the solution.

The notebooks intentionally preserve the progression from beginner exercises toward more advanced statistical and data-analysis problems.

## Current Progress

**Math, Statistics & Visualization**

* [x] Practice 01 — Fundamentals
* [ ] Practice 02 — Variance, standard deviation, probability rules and relationships
* [ ] Practice 03 — Normal distribution and z-scores
* [ ] Sampling and standard error
* [ ] Central Limit Theorem
* [ ] Confidence intervals
* [ ] Z-tests
* [ ] T-tests
* [ ] Chi-square tests

**Exploratory Data Analysis**

* [x] EDA Practice 01 — Hotel-chain dataset
* [ ] Additional beginner EDA practice
* [ ] Intermediate EDA
* [ ] Advanced EDA

## Purpose

This repository is both a **learning journal and practical portfolio**.

It shows not only finished solutions, but the progression of my understanding as I learn how to explore data, apply statistics, choose appropriate visualizations, and communicate conclusions from data.

