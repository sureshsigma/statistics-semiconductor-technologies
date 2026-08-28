# Chapter 8 — Correlation and Relationships Between Semiconductor Variables

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why relationships between variables are important in semiconductor science.
- Identify independent and dependent variables.
- Organize paired semiconductor measurements.
- Interpret scatter plots.
- Explain positive, negative and weak relationships.
- Understand the basic idea of covariance.
- Define the Pearson correlation coefficient.
- Calculate and interpret the correlation coefficient.
- Distinguish strong and weak correlation.
- Distinguish correlation from causation.
- Apply correlation to semiconductor measurements such as voltage, current, temperature and sensor response.

---

## 8.1 Why Do We Study Relationships Between Variables?

In semiconductor science, measurements are rarely studied in isolation.

We often want to understand how one physical quantity changes when another quantity changes.

For example:

- How does drain current change with gate voltage?
- How does leakage current change with temperature?
- How does resistance change with temperature?
- How does photodiode current change with light intensity?
- How does resistivity change with doping concentration?
- How does film thickness change with a process parameter?

These are questions about **relationships between variables**.

Suppose we measure the gate voltage $V_G$ and drain current $I_D$ of a MOSFET.

A simplified dataset might look like:

| Gate Voltage $V_G$ (V) | Drain Current $I_D$ (mA) |
|---:|---:|
| 1.0 | 0.2 |
| 1.5 | 0.8 |
| 2.0 | 1.8 |
| 2.5 | 3.1 |
| 3.0 | 4.7 |

As gate voltage increases, drain current also increases.

This suggests that the two variables are related.

Statistics gives us tools to describe such relationships quantitatively.

---

## 8.2 Two-Variable Data

When two measurements are recorded for the same experimental unit, we obtain **paired data**.

For example, for each MOSFET measurement we record:

$$
(V_G,I_D)
$$

A dataset may be written as:

$$
(V_{G1},I_{D1}),
(V_{G2},I_{D2}),
\ldots,
(V_{Gn},I_{Dn})
$$

Each pair belongs to the same observation.

For example:

$$
(1.0,0.2)
$$

means:

- Gate voltage = $1.0$ V
- Drain current = $0.2$ mA

The pairing is important.

We cannot randomly separate the voltage observations from the current observations because the relationship depends on which values were measured together.

---

## 8.3 Independent and Dependent Variables

In an experiment, one variable is often controlled or changed by the experimenter.

This is commonly called the **independent variable**.

The quantity that responds to the change is commonly called the **dependent variable**.

### Example: MOSFET

Suppose we change gate voltage and observe drain current.

Independent variable:

$$
V_G
$$

Dependent variable:

$$
I_D
$$

We can represent this as:

$$
V_G\rightarrow I_D
$$

However, the terms independent and dependent variables describe the experimental setup. They do not automatically prove a cause-and-effect relationship.

---

## 8.4 Scatter Plot

A **scatter plot** displays paired observations as points on a graph.

For semiconductor data, we might plot:

- $V_G$ on the horizontal axis
- $I_D$ on the vertical axis

Each observation becomes one point:

$$
(V_G,I_D)
$$

A scatter plot helps us visually identify patterns.

For example, if the points generally move upward from left to right, the variables may have a positive relationship.

If the points generally move downward from left to right, they may have a negative relationship.

If the points appear randomly scattered, there may be little or no linear relationship.

---

## 8.5 Semiconductor Example — Gate Voltage and Drain Current

Consider the following simplified measurements:

| $V_G$ (V) | $I_D$ (mA) |
|---:|---:|
| 1.0 | 0.2 |
| 1.5 | 0.8 |
| 2.0 | 1.8 |
| 2.5 | 3.1 |
| 3.0 | 4.7 |

The observations generally increase together.

Therefore, the scatter plot would show an upward pattern.

This is a **positive relationship**.

The important point is:

> **As gate voltage increases, drain current tends to increase in this dataset.**

Correlation allows us to quantify the strength of such a linear relationship.

---

## 8.6 Positive Relationship

A positive relationship means that larger values of one variable tend to be associated with larger values of the other variable.

Symbolically:

$$
X\uparrow
\quad\Rightarrow\quad
Y\uparrow
$$

This does not mean that every single observation must increase perfectly.

There may be measurement noise and experimental variation.

### Semiconductor Examples

Possible positive relationships include:

- Light intensity and photodiode current
- Gate voltage and drain current over a suitable operating region
- Temperature and some leakage-current measurements
- Applied voltage and current in an approximately ohmic device region

The actual relationship depends on the device and operating conditions.

---

## 8.7 Negative Relationship

A negative relationship means that larger values of one variable tend to be associated with smaller values of the other variable.

Symbolically:

$$
X\uparrow
\quad\Rightarrow\quad
Y\downarrow
$$

### Semiconductor Example

Suppose a material's mobility decreases as temperature increases over a particular operating range.

Then:

$$
T\uparrow
\quad\Rightarrow\quad
\mu\downarrow
$$

This would represent a negative relationship.

Another example could be a quantity that decreases as a control parameter increases.

The sign of the relationship is important because it tells us the direction in which the variables tend to move together.

---

## 8.8 No Clear Linear Relationship

Sometimes two variables do not show a clear linear pattern.

For example, suppose measurements of two unrelated experimental quantities are:

| $X$ | $Y$ |
|---:|---:|
| 1 | 8 |
| 2 | 3 |
| 3 | 9 |
| 4 | 2 |
| 5 | 7 |

The points may appear scattered without a clear upward or downward trend.

In such a situation, the linear correlation may be close to zero.

However:

> **A correlation close to zero means little or no linear relationship; it does not necessarily mean that no relationship of any kind exists.**

A curved relationship may still exist.

---

## 8.9 Covariance — The Basic Idea

Before defining correlation, it is useful to understand **covariance**.

Suppose we have two variables:

$$
X
$$

and:

$$
Y
$$

We compare each observation with its mean.

For $X$:

$$
x_i-\bar{x}
$$

For $Y$:

$$
y_i-\bar{y}
$$

We then multiply the deviations:

$$
(x_i-\bar{x})(y_i-\bar{y})
$$

If both variables tend to be above their means at the same time, the product is positive.

If both tend to be below their means at the same time, the product is also positive.

If one is above its mean while the other is below its mean, the product is negative.

This gives covariance its basic interpretation.

---

## 8.10 Sample Covariance

For a sample of paired observations, the sample covariance is:

$$
\boxed{
s_{xy}
=
\frac{1}{n-1}
\sum_{i=1}^{n}
(x_i-\bar{x})(y_i-\bar{y})
}
$$

where:

- $s_{xy}$ = sample covariance
- $x_i$ = observation of variable $X$
- $y_i$ = observation of variable $Y$
- $\bar{x}$ = mean of $X$
- $\bar{y}$ = mean of $Y$
- $n$ = number of paired observations

A positive covariance generally indicates that the variables tend to move in the same direction.

A negative covariance generally indicates that they tend to move in opposite directions.

However, covariance depends on the units of measurement.

This makes direct comparison between different datasets difficult.

Correlation solves this problem by standardizing covariance.

---

## 8.11 Pearson Correlation Coefficient

The **Pearson correlation coefficient** measures the strength and direction of a linear relationship between two quantitative variables.

It is usually represented by:

$$
\boxed{r}
$$

The sample correlation coefficient is:

$$
\boxed{
r=
\frac{
\sum_{i=1}^{n}
(x_i-\bar{x})(y_i-\bar{y})
}{
\sqrt{
\sum_{i=1}^{n}(x_i-\bar{x})^2
\sum_{i=1}^{n}(y_i-\bar{y})^2
}
}
}
$$

The value of $r$ lies between:

$$
\boxed{-1\leq r\leq1}
$$

This makes correlation easier to interpret than covariance.

---

## 8.12 Interpreting the Sign of Correlation

The sign of $r$ indicates the direction of the linear relationship.

### Positive Correlation

$$
r>0
$$

As one variable tends to increase, the other also tends to increase.

### Negative Correlation

$$
r<0
$$

As one variable tends to increase, the other tends to decrease.

### No Linear Correlation

If:

$$
r\approx0
$$

there is little or no linear relationship.

The sign tells us the direction.

The magnitude tells us the strength.

---

## 8.13 Interpreting the Magnitude of Correlation

The absolute value:

$$
|r|
$$

indicates the strength of the linear association.

Values close to 1 indicate a strong linear relationship.

Values close to 0 indicate a weak linear relationship.

For example:

$$
r=0.95
$$

indicates a strong positive linear association.

Similarly:

$$
r=-0.90
$$

indicates a strong negative linear association.

And:

$$
r=0.10
$$

indicates a very weak positive linear association.

A commonly used informal interpretation is:

| $|r|$ | General interpretation |
|---:|---|
| Close to 0 | Very weak linear relationship |
| Around 0.3 | Weak to moderate |
| Around 0.5 | Moderate |
| Around 0.7 | Strong |
| Close to 1 | Very strong |

These are only guidelines.

There is no universal boundary at which a correlation becomes "strong."

The context and scientific application matter.

---

## 8.14 Semiconductor Example — Temperature and Leakage Current

Leakage current in semiconductor devices can change significantly with temperature.

Suppose we measure:

| Temperature $T$ (°C) | Leakage Current $I_L$ (nA) |
|---:|---:|
| 20 | 10 |
| 30 | 14 |
| 40 | 20 |
| 50 | 29 |
| 60 | 42 |

The data show that leakage current generally increases as temperature increases.

Therefore, we expect a positive association.

A scatter plot would show an upward pattern.

The correlation coefficient could be used to quantify the strength of the **linear** association over the measured range.

However, leakage current may have a nonlinear dependence on temperature.

Therefore, a high positive correlation does not mean that the physical relationship is exactly linear.

This is an important distinction.

---

## 8.15 Semiconductor Example — Light Intensity and Photodiode Current

Consider a photodiode.

Suppose the measured light intensity and photocurrent are:

| Light Intensity (arbitrary units) | Photocurrent (µA) |
|---:|---:|
| 10 | 2.1 |
| 20 | 4.0 |
| 30 | 6.2 |
| 40 | 8.1 |
| 50 | 10.3 |

As light intensity increases, photocurrent also tends to increase.

Therefore, we expect:

$$
r>0
$$

A correlation coefficient close to $+1$ would indicate that the measurements have a strong positive linear association.

This is useful when evaluating whether a sensor behaves consistently over a particular operating range.

---

## 8.16 Semiconductor Example — Temperature and Mobility

Suppose measurements show that carrier mobility decreases as temperature increases.

| Temperature (K) | Mobility (cm²/V·s) |
|---:|---:|
| 250 | 1500 |
| 275 | 1380 |
| 300 | 1260 |
| 325 | 1150 |
| 350 | 1060 |

The variables show a downward trend.

Therefore, the correlation is expected to be negative:

$$
r<0
$$

If the points lie close to a straight line, the correlation may be strongly negative.

Again, correlation describes the linear association; it does not establish the physical mechanism responsible for the trend.

---

## 8.17 Calculating Correlation — Small Example

Consider a simplified semiconductor dataset:

| $V_G$ (V) | $I_D$ (mA) |
|---:|---:|
| 1 | 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |
| 5 | 5 |

The means are:

$$
\bar{x}=3
$$

and:

$$
\bar{y}=3
$$

The deviations are:

| $x_i$ | $x_i-\bar{x}$ | $y_i$ | $y_i-\bar{y}$ |
|---:|---:|---:|---:|
| 1 | -2 | 1 | -2 |
| 2 | -1 | 2 | -1 |
| 3 | 0 | 3 | 0 |
| 4 | 1 | 4 | 1 |
| 5 | 2 | 5 | 2 |

The variables move together perfectly in this simplified dataset.

Therefore:

$$
\boxed{r=1}
$$

This is a perfect positive linear correlation.

Real semiconductor measurements are rarely this perfect because of noise, device variation and experimental limitations.

---

## 8.18 What Does $r=1$ Mean?

If:

$$
r=1
$$

there is a perfect positive linear relationship between the two variables.

All observations lie exactly on a straight line with positive slope.

Similarly:

$$
r=-1
$$

represents a perfect negative linear relationship.

If:

$$
r=0
$$

there is no linear correlation.

However, $r=0$ does not prove that the variables are completely unrelated.

---

## 8.19 Correlation Does Not Mean Causation

This is one of the most important ideas in data analysis.

Suppose we find:

$$
r=0.95
$$

between temperature and leakage current.

This tells us that the two variables have a strong positive linear association in the observed data.

It does **not**, by itself, prove causation.

In semiconductor experiments, causal interpretation requires knowledge of:

- Experimental design
- Physical theory
- Controlled variables
- Measurement conditions
- Possible confounding factors

For example, two device parameters may both change with temperature.

A strong correlation may arise because temperature influences both.

Therefore:

> **Correlation describes association; experimental evidence and physical reasoning are needed to establish causation.**

---

## 8.20 Correlation and Nonlinear Relationships

Pearson correlation measures **linear** association.

Consider a curved relationship such as:

$$
Y=X^2
$$

There is a clear relationship between $X$ and $Y$, but the relationship is not linear over a symmetric range around zero.

Therefore, correlation may not fully describe the relationship.

This is particularly important in semiconductor applications.

Examples of nonlinear behavior can occur in:

- Diode I–V characteristics
- MOSFET characteristics
- Temperature-dependent leakage
- Exponential sensor responses
- Semiconductor carrier concentration relationships

Therefore:

> **Always look at the data or scatter plot before interpreting a correlation coefficient.**

---

## 8.21 Correlation and Outliers

An **outlier** is an observation that is unusually far from the general pattern.

Correlation can be strongly affected by outliers.

Suppose most semiconductor measurements follow a clear trend, but one measurement is caused by:

- Instrument malfunction
- Incorrect sample preparation
- Data-entry error
- Unusual experimental conditions

That single observation can change the calculated correlation.

Therefore, before calculating or interpreting correlation, we should inspect the data.

This is one reason why **exploratory data analysis** is important.

---

## 8.22 Correlation Does Not Measure Agreement

Correlation measures whether two variables move together.

It does not necessarily mean that their numerical values are close.

For example, suppose:

$$
Y=2X
$$

The variables have a perfect positive linear relationship:

$$
r=1
$$

But $X$ and $Y$ are not equal.

This distinction matters in measurement science.

Two instruments may show a very high correlation while one consistently gives readings higher than the other.

Therefore:

> **High correlation does not automatically mean that two measurement systems agree perfectly.**

---

## 8.23 Correlation in Semiconductor Process Monitoring

Suppose a manufacturing team records:

- Process temperature
- Film thickness

for several production batches.

A correlation analysis may help answer:

> Is film thickness associated with process temperature?

Similarly, engineers may investigate relationships between:

- Deposition time and film thickness
- Temperature and resistance
- Doping concentration and resistivity
- Gate voltage and drain current
- Light intensity and photocurrent

Correlation can therefore serve as an initial data-analysis tool before more detailed modelling.

---

## 8.24 Common Mistakes

### Mistake 1: Thinking correlation proves causation

Correlation only measures association.

### Mistake 2: Ignoring the sign

The sign tells us the direction of the linear relationship.

### Mistake 3: Thinking $r=0$ means no relationship at all

It means no linear relationship, not necessarily no relationship.

### Mistake 4: Assuming $r$ can be greater than 1

The Pearson correlation coefficient satisfies:

$$
-1\leq r\leq1
$$

### Mistake 5: Interpreting correlation without looking at the data

Always examine a scatter plot where possible.

### Mistake 6: Ignoring outliers

A single unusual observation can strongly influence correlation.

### Mistake 7: Assuming high correlation means agreement

Two variables can be highly correlated but systematically different.

---

## 8.25 Summary

Semiconductor experiments often involve pairs of measurements.

Examples include:

$$
(V_G,I_D)
$$

$$
(T,I_L)
$$

$$
(\text{Light Intensity},I_{\text{photo}})
$$

Relationships between variables can be explored using:

- Tables
- Scatter plots
- Covariance
- Correlation

Covariance describes whether two variables tend to move together, but it depends on the measurement units.

Pearson correlation standardizes this relationship:

$$
\boxed{
-1\leq r\leq1
}
$$

The sign indicates direction:

$$
r>0
$$

for positive association, and:

$$
r<0
$$

for negative association.

The magnitude indicates the strength of the linear association.

The key idea is:

> **Correlation quantifies the strength and direction of a linear relationship between two variables.**

But:

> **Correlation does not by itself prove causation.**

---

## 8.26 Key Formulae

### Sample Covariance

$$
\boxed{
s_{xy}
=
\frac{1}{n-1}
\sum_{i=1}^{n}
(x_i-\bar{x})(y_i-\bar{y})
}
$$

### Pearson Correlation Coefficient

$$
\boxed{
r=
\frac{
\sum_{i=1}^{n}
(x_i-\bar{x})(y_i-\bar{y})
}{
\sqrt{
\sum_{i=1}^{n}(x_i-\bar{x})^2
\sum_{i=1}^{n}(y_i-\bar{y})^2
}
}
}
$$

### Range of Correlation

$$
\boxed{
-1\leq r\leq1
}
$$

---

## 8.27 Review Questions

### Conceptual Questions

1. What is meant by a relationship between two variables?
2. What are paired observations?
3. Define independent and dependent variables.
4. What is a scatter plot?
5. What is a positive relationship?
6. What is a negative relationship?
7. What is covariance?
8. What is the Pearson correlation coefficient?
9. What does the sign of $r$ indicate?
10. What does the magnitude of $r$ indicate?
11. What does $r=1$ mean?
12. What does $r=-1$ mean?
13. What does $r\approx0$ mean?
14. Why does correlation not prove causation?
15. Why can an outlier affect correlation?

### Semiconductor Application Questions

16. Why might a semiconductor engineer study gate voltage and drain current together?
17. Why might temperature and leakage current be correlated?
18. How could correlation be useful in sensor analysis?
19. Why should a scatter plot be examined before interpreting correlation?
20. Give three examples of variable pairs that could be studied in semiconductor experiments.

---

## 8.28 Practice Problems

### Problem 1 — Identify Variables

In a MOSFET experiment, gate voltage is changed and drain current is measured.

Identify:

1. Independent variable
2. Dependent variable
3. A suitable scatter plot arrangement

### Problem 2 — Direction of Relationship

State whether each relationship is likely to be positive or negative over the stated operating range:

1. Light intensity and photodiode current
2. Temperature and carrier mobility
3. Gate voltage and drain current in an increasing operating region
4. Temperature and leakage current

Explain your answers.

### Problem 3 — Interpretation of $r$

Interpret each of the following:

1. $r=0.92$
2. $r=-0.87$
3. $r=0.08$
4. $r=-0.05$

### Problem 4 — MOSFET Data

Consider:

| $V_G$ (V) | $I_D$ (mA) |
|---:|---:|
| 1.0 | 0.5 |
| 1.5 | 1.1 |
| 2.0 | 1.9 |
| 2.5 | 2.8 |
| 3.0 | 3.9 |

1. Identify the independent variable.
2. Identify the dependent variable.
3. Describe the direction of the relationship.
4. Would you expect $r$ to be positive or negative?
5. Would you expect the relationship to be perfectly linear? Explain.

### Problem 5 — Temperature and Leakage Current

Consider:

| Temperature (°C) | Leakage Current (nA) |
|---:|---:|
| 20 | 10 |
| 30 | 14 |
| 40 | 20 |
| 50 | 29 |
| 60 | 42 |

1. Describe the relationship.
2. Is it positive or negative?
3. Would Pearson correlation be useful?
4. Why might the physical relationship still be nonlinear even if correlation is high?

### Problem 6 — Correlation vs Causation

A study finds a strong positive correlation between temperature and leakage current.

Explain why this result alone does not prove that temperature is the only cause of the observed leakage-current changes.

### Problem 7 — Photodiode

A photodiode is tested at different light intensities.

| Light Intensity | Photocurrent (µA) |
|---:|---:|
| 10 | 2.1 |
| 20 | 4.0 |
| 30 | 6.2 |
| 40 | 8.1 |
| 50 | 10.3 |

1. Describe the relationship.
2. Would you expect a positive or negative correlation?
3. What would a value of $r$ close to $+1$ indicate?
4. Does a high $r$ prove that the relationship is exactly linear for all light intensities?

---

## 8.29 Looking Ahead

Correlation tells us that two variables are related, and it gives us a measure of the strength and direction of their linear association.

The next question is:

> **Can we describe the relationship using an equation?**

For example, can we describe a relationship between voltage and current using:

$$
y=a+bx
$$

where:

- $a$ = intercept
- $b$ = slope

This leads to the next chapter:

$$
\boxed{
\text{Linear Curve Fitting — Slope and Intercept}
}
$$

We will apply it to semiconductor examples such as:

- Linear regions of I–V characteristics
- Sensor calibration
- Resistance estimation
- Process calibration
