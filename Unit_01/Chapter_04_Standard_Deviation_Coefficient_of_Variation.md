# Chapter 4 — Standard Deviation and Coefficient of Variation

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why standard deviation is used as a measure of dispersion.
- Explain the relationship between variance and standard deviation.
- Calculate population standard deviation.
- Calculate sample standard deviation.
- Interpret standard deviation in the original units of measurement.
- Explain how standard deviation describes measurement consistency.
- Define the coefficient of variation.
- Calculate the coefficient of variation.
- Use the coefficient of variation to compare relative variability.
- Apply standard deviation and coefficient of variation to semiconductor data.

---

## 4.1 Why Do We Need Standard Deviation?

In the previous chapter, we introduced variance as a measure of dispersion.

Variance is calculated using squared deviations from the mean.

For a population:

$$
\sigma^2=
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
$$

For a sample:

$$
s^2=
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
$$

Variance is useful because it considers every observation.

However, there is one practical difficulty.

If the original measurement is expressed in volts, variance is expressed in square volts:

$$
\text{V}^2
$$

If film thickness is measured in nanometres, variance is expressed in:

$$
\text{nm}^2
$$

These squared units are mathematically correct, but they are not always easy to interpret physically.

This leads to the idea of **standard deviation**.

---

## 4.2 Standard Deviation as the Square Root of Variance

The standard deviation is the positive square root of the variance.

For a population:

$$
\boxed{
\sigma=\sqrt{\sigma^2}
}
$$

For a sample:

$$
\boxed{
s=\sqrt{s^2}
}
$$

Because the square root is taken, standard deviation has the **same units as the original measurements**.

For example:

- Voltage → standard deviation in volts
- Current → standard deviation in amperes
- Film thickness → standard deviation in nanometres
- Temperature → standard deviation in degrees Celsius

This makes standard deviation easier to interpret than variance.

> **Variance measures squared deviation; standard deviation expresses the spread in the same units as the original data.**

---

## 4.3 Population Standard Deviation

When the data represent the complete population of interest, the population standard deviation is:

$$
\boxed{
\sigma=
\sqrt{
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
}
$$

where:

- $\sigma$ = population standard deviation
- $N$ = population size
- $x_i$ = population observation
- $\mu$ = population mean

The calculation follows these steps:

1. Calculate the population mean.
2. Calculate each deviation from the mean.
3. Square each deviation.
4. Add the squared deviations.
5. Divide by $N$.
6. Take the square root.

---

## 4.4 Worked Example: Population Standard Deviation

Consider the complete set of threshold-voltage measurements from a small experimental population:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

The population mean is:

$$
\mu=0.70\text{ V}
$$

The deviations are:

| $x_i$ (V) | $x_i-\mu$ (V) | $(x_i-\mu)^2$ (V²) |
|---:|---:|---:|
| 0.68 | -0.02 | 0.0004 |
| 0.69 | -0.01 | 0.0001 |
| 0.70 | 0.00 | 0.0000 |
| 0.71 | +0.01 | 0.0001 |
| 0.72 | +0.02 | 0.0004 |

The sum of squared deviations is:

$$
0.0004+0.0001+0+0.0001+0.0004=0.0010
$$

Therefore, the population variance is:

$$
\sigma^2=
\frac{0.0010}{5}
=0.0002\text{ V}^2
$$

The standard deviation is:

$$
\sigma
=\sqrt{0.0002}
$$

Therefore,

$$
\boxed{
\sigma\approx0.01414\text{ V}
}
$$

or approximately:

$$
\boxed{
\sigma\approx14.14\text{ mV}
}
$$

### Interpretation

The threshold-voltage measurements have a standard deviation of approximately $14.14$ mV.

The important advantage is that the result is expressed in the original unit:

$$
\text{mV}
$$

rather than:

$$
\text{mV}^2
$$

---

## 4.5 Sample Standard Deviation

In many practical semiconductor applications, we measure a sample rather than the complete population.

The sample standard deviation is:

$$
\boxed{
s=
\sqrt{
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
}
$$

where:

- $s$ = sample standard deviation
- $n$ = sample size
- $x_i$ = sample observation
- $\bar{x}$ = sample mean

The denominator is $n-1$, just as it was for sample variance.

### Practical Rule

Use:

$$
\boxed{
\sigma
\text{ for a population}
}
$$

and

$$
\boxed{
s
\text{ for a sample}
}
$$

The distinction between population and sample should be made before selecting the formula.

---

## 4.6 Worked Example: Sample Standard Deviation

Suppose five MOSFETs are selected from a much larger manufacturing batch.

Their threshold voltages are:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

The sample mean is:

$$
\bar{x}=0.70\text{ V}
$$

The squared deviations are:

$$
0.0004,\;0.0001,\;0,\;0.0001,\;0.0004
$$

Their sum is:

$$
\sum_{i=1}^{5}(x_i-\bar{x})^2=0.0010
$$

Since the data are a sample:

$$
n=5
$$

Therefore:

$$
s^2=\frac{0.0010}{5-1}
=0.00025\text{ V}^2
$$

Taking the square root:

$$
s=\sqrt{0.00025}
$$

Therefore,

$$
\boxed{
s\approx0.01581\text{ V}
}
$$

or:

$$
\boxed{
s\approx15.81\text{ mV}
}
$$

---

## 4.7 Interpreting Standard Deviation

Standard deviation provides an indication of how widely observations are distributed around their mean.

A small standard deviation generally indicates that measurements are relatively close to the mean.

A large standard deviation indicates greater spread.

Consider two semiconductor measurement groups.

### Group A

$$
0.698,\;0.699,\;0.700,\;0.701,\;0.702\text{ V}
$$

### Group B

$$
0.60,\;0.65,\;0.70,\;0.75,\;0.80\text{ V}
$$

Both may have a mean near:

$$
0.70\text{ V}
$$

but Group B clearly has greater variation.

Therefore, standard deviation helps distinguish between:

- A tightly controlled set of measurements
- A highly variable set of measurements

---

## 4.8 Standard Deviation and Measurement Consistency

Suppose a laboratory measures the same semiconductor parameter repeatedly.

### Experiment A

$$
10.01,\;10.00,\;9.99,\;10.00,\;10.01
$$

### Experiment B

$$
9.2,\;10.8,\;9.5,\;10.7,\;9.8
$$

The means may be similar, but Experiment A has much smaller variation.

A small standard deviation may indicate:

- Good measurement repeatability
- Stable experimental conditions
- Low measurement variation

A larger standard deviation may indicate:

- Greater measurement variation
- Environmental changes
- Instrument noise
- Device variation
- Unstable experimental conditions

However, standard deviation alone does not identify the cause of variation.

It only quantifies the amount of variation.

> **Statistical analysis measures variation; engineering investigation is required to determine its cause.**

---

## 4.9 Standard Deviation in Semiconductor Process Control

Suppose a semiconductor manufacturing process targets a film thickness of:

$$
100\text{ nm}
$$

Two production processes produce the following results.

### Process A

$$
99.8,\;100.0,\;100.1,\;99.9,\;100.2\text{ nm}
$$

### Process B

$$
96,\;98,\;100,\;102,\;104\text{ nm}
$$

Both processes may have approximately the same average.

However, Process B has much greater spread.

A process engineer would therefore want to compare their standard deviations.

A process with smaller standard deviation may indicate greater consistency, provided that the process is also centered appropriately around the desired target.

This last point is important:

> **Low variation is desirable, but low variation around the wrong target is still a problem.**

For example, a process that consistently produces 95 nm when the target is 100 nm may have low variation but poor accuracy relative to the target.

---

## 4.10 Coefficient of Variation

Standard deviation is expressed in the same units as the original data.

This is useful, but it creates a problem when we want to compare the relative variability of quantities having very different means.

The **coefficient of variation (CV)** expresses standard deviation relative to the mean.

For a sample:

$$
\boxed{
CV=
\frac{s}{\bar{x}}\times100
}
$$

For a population:

$$
\boxed{
CV=
\frac{\sigma}{\mu}\times100
}
$$

The coefficient of variation is usually expressed as a percentage.

It is a **relative measure of dispersion**.

---

## 4.11 Why Do We Need Coefficient of Variation?

Consider two semiconductor measurements.

### Measurement A

Mean:

$$
\bar{x}_A=10\text{ mA}
$$

Standard deviation:

$$
s_A=1\text{ mA}
$$

### Measurement B

Mean:

$$
\bar{x}_B=100\text{ mA}
$$

Standard deviation:

$$
s_B=5\text{ mA}
$$

If we only compare standard deviation:

$$
5\text{mA}>1\text{mA}
$$

we might conclude that Measurement B is more variable.

But this ignores the scale of the measurements.

Calculate the coefficient of variation.

For A:

$$
CV_A=\frac{1}{10}\times100=10\%
$$

For B:

$$
CV_B=\frac{5}{100}\times100=5\%
$$

Therefore:

$$
\boxed{CV_A = 10\%}
$$

and

$$
\boxed{CV_B = 5\%}
$$


Although B has a larger standard deviation in absolute units, A has greater **relative variability**.

This is one of the main reasons for using the coefficient of variation.

---

## 4.12 Semiconductor Example: Comparing Relative Variation

Suppose two sensors are tested.

### Sensor A

Mean output:

$$
\bar{x}_A=20\text{ mV}
$$

Standard deviation:

$$
s_A=1\text{ mV}
$$

Therefore:

$$
CV_A=\frac{1}{20}\times100=5\%
$$

### Sensor B

Mean output:

$$
\bar{x}_B=200\text{ mV}
$$

Standard deviation:

$$
s_B=5\text{ mV}
$$

Therefore:

$$
CV_B=\frac{5}{200}\times100=2.5\%
$$

Although Sensor B has a larger standard deviation:

$$
5\text{ mV}>1\text{ mV}
$$

its relative variation is smaller:

$$
2.5\%<5\%
$$

Therefore, Sensor B shows lower relative variability.

---

## 4.13 Coefficient of Variation and Process Comparison

Suppose two semiconductor processes produce components with different target resistance values.

### Process A

Mean resistance:

$$
\bar{x}_A=100\ \Omega
$$

Standard deviation:

$$
s_A=2\ \Omega
$$

Therefore:

$$
CV_A=\frac{2}{100}\times100=2\%
$$

### Process B

Mean resistance:

$$
\bar{x}_B=1000\ \Omega
$$

Standard deviation:

$$
s_B=10\ \Omega
$$

Therefore:

$$
CV_B=\frac{10}{1000}\times100=1\%
$$

Process B has a larger absolute standard deviation:

$$
10\Omega>2\Omega
$$

but a smaller relative variation:

$$
1\%<2\%
$$

Therefore, coefficient of variation allows a more meaningful comparison of relative consistency.

---

## 4.14 Standard Deviation vs Coefficient of Variation

The two measures answer slightly different questions.

| Measure | Question answered | Unit |
|---|---|---|
| Standard deviation | How much do observations vary in the original units? | Same as data |
| Coefficient of variation | How large is the variation relative to the mean? | Percentage |

### Standard Deviation

Useful when:

- The original measurement unit is important.
- We need an absolute measure of variation.
- We are analyzing repeated measurements of the same quantity and scale.

### Coefficient of Variation

Useful when:

- Comparing variability between datasets with different means.
- Comparing measurements on different scales.
- Relative variation is more important than absolute variation.

---

## 4.15 Important Limitation of Coefficient of Variation

The coefficient of variation is based on the mean:

$$
CV=\frac{s}{\bar{x}}\times100
$$

Therefore, it can become very large or unstable when the mean is close to zero.

For example, if:

$$
\bar{x}\approx0
$$

then dividing by the mean can produce an extremely large value.

Therefore, CV should not be used automatically for every dataset.

It is most meaningful when:

- The variable has a meaningful zero.
- The mean is sufficiently far from zero.
- Relative variation is scientifically meaningful.

For measurements such as some voltage, current, concentration, or size variables, the suitability of CV should be considered in context.

---

## 4.16 A Complete Semiconductor Example

Suppose two production lines manufacture a component with different nominal resistance values.

### Production Line A

Mean resistance:

$$
\bar{x}_A=100\Omega
$$

Standard deviation:

$$
s_A=3\Omega
$$

### Production Line B

Mean resistance:

$$
\bar{x}_B=500\Omega
$$

Standard deviation:

$$
s_B=8\Omega
$$

At first glance:

$$
8\Omega>3\Omega
$$

so Line B appears more variable.

Calculate the coefficient of variation.

For Line A:

$$
CV_A=\frac{3}{100}\times100=3\%
$$

For Line B:

$$
CV_B=\frac{8}{500}\times100=1.6\%
$$

Therefore:

$$
\boxed{CV_A=3\%}
$$

and

$$
\boxed{CV_B=1.6\%}
$$

### Interpretation

Line B has greater absolute variation, but lower relative variation.

Therefore, if the objective is to compare **relative consistency**, Line B performs better according to CV.

However, an engineer should also consider:

- Specification limits
- Target values
- Measurement uncertainty
- Functional requirements
- Cost and manufacturing constraints

A statistical measure should support engineering judgment, not replace it.

---

## 4.17 Common Mistakes

### Mistake 1: Confusing variance and standard deviation

Variance is:

$$
s^2
$$

Standard deviation is:

$$
s=\sqrt{s^2}
$$

### Mistake 2: Forgetting to take the square root

Variance is not standard deviation.

### Mistake 3: Using the wrong denominator

For population standard deviation:

$$
N
$$

For sample standard deviation:

$$
n-1
$$

### Mistake 4: Thinking a larger standard deviation always means worse performance

Standard deviation must be interpreted relative to:

- The mean
- The target
- Specification limits
- The engineering application

### Mistake 5: Comparing standard deviations without considering scale

A standard deviation of 5 units may be small for a mean of 1,000 units but large for a mean of 10 units.

This is where coefficient of variation can be useful.

### Mistake 6: Using CV when the mean is close to zero

CV can become unstable when the mean is near zero.

---

## 4.18 Summary

Standard deviation is one of the most widely used measures of dispersion.

It is obtained by taking the square root of variance.

For a population:

$$
\boxed{
\sigma=
\sqrt{
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
}
$$

For a sample:

$$
\boxed{
s=
\sqrt{
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
}
$$

Unlike variance, standard deviation has the same units as the original observations.

The coefficient of variation expresses standard deviation relative to the mean.

For a sample:

$$
\boxed{
CV=
\frac{s}{\bar{x}}\times100
}
$$

For a population:

$$
\boxed{
CV=
\frac{\sigma}{\mu}\times100
}
$$

The key distinction is:

> **Standard deviation measures absolute variation; coefficient of variation measures relative variation.**

In semiconductor applications, these measures can help assess:

- Device-to-device consistency
- Experimental repeatability
- Process variation
- Sensor consistency
- Manufacturing uniformity

---

## 4.19 Key Formulae

### Population Standard Deviation

$$
\boxed{
\sigma=
\sqrt{
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
}
$$

### Sample Standard Deviation

$$
\boxed{
s=
\sqrt{
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
}
$$

### Population Coefficient of Variation

$$
\boxed{
CV=
\frac{\sigma}{\mu}\times100
}
$$

### Sample Coefficient of Variation

$$
\boxed{
CV=
\frac{s}{\bar{x}}\times100
}
$$

---

## 4.20 Review Questions

### Conceptual Questions

1. Why is standard deviation useful when variance is already available?
2. What is the relationship between variance and standard deviation?
3. Why does standard deviation have the same units as the original measurements?
4. Distinguish between population standard deviation and sample standard deviation.
5. What does a small standard deviation indicate?
6. What does a large standard deviation indicate?
7. Define coefficient of variation.
8. Why is coefficient of variation called a relative measure of dispersion?
9. When might coefficient of variation be more useful than standard deviation?
10. Why should CV be used carefully when the mean is close to zero?

### Semiconductor Application Questions

11. Why is standard deviation useful when analyzing threshold-voltage measurements?
12. How can standard deviation help a semiconductor process engineer?
13. Why might two processes with different means need to be compared using coefficient of variation?
14. Explain why a process with a larger standard deviation can still have a smaller coefficient of variation.
15. Why is low variation around an incorrect target still a problem?

---

## 4.21 Practice Problems

### Problem 1 — Population Standard Deviation

The complete set of threshold-voltage measurements from an experiment is:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

Calculate:

1. The mean
2. The population variance
3. The population standard deviation

### Problem 2 — Sample Standard Deviation

A sample of five semiconductor devices has threshold voltages:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

Calculate:

1. The sample mean
2. The sample variance
3. The sample standard deviation

### Problem 3 — Coefficient of Variation

A semiconductor sensor has:

$$
\bar{x}=20\text{ mV}
$$

and

$$
s=1\text{ mV}
$$

Calculate the coefficient of variation.

### Problem 4 — Compare Relative Variation

Sensor A has:

$$
\bar{x}_A=20\text{ mV},\qquad s_A=1\text{ mV}
$$

Sensor B has:

$$
\bar{x}_B=200\text{ mV},\qquad s_B=5\text{ mV}
$$

Calculate the CV of each sensor and determine which has lower relative variation.

### Problem 5 — Manufacturing Process

Two production processes have:

**Process A**

$$
\bar{x}_A=100\text{ nm},\qquad s_A=2\text{ nm}
$$

**Process B**

$$
\bar{x}_B=500\text{ nm},\qquad s_B=8\text{ nm}
$$

Calculate the CV for each process and compare their relative variability.

### Problem 6 — Interpretation

A manufacturing process has a very small standard deviation but its mean is substantially different from the target value.

Explain why the process cannot automatically be considered satisfactory.

---

## 4.22 Looking Ahead

In this chapter, we learned how to measure variation using standard deviation and coefficient of variation.

We can now describe both:

- The center of a dataset using mean, median and mode
- The spread of a dataset using range, variance and standard deviation
- The relative spread using coefficient of variation

The next part of the unit focuses on **measurement error**.

The next question is:

> **How close is a measured value to a reference or accepted value?**

This leads to the study of:

$$
\boxed{\text{Absolute Error, Relative Error and Percentage Error}}
$$
