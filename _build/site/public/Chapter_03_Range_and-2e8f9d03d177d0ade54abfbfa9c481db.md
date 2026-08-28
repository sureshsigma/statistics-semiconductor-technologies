# Chapter 3 — Range and Variance

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why a measure of central tendency alone is not sufficient to describe data.
- Explain the meaning of variation or dispersion.
- Calculate and interpret the range of a dataset.
- Identify the advantages and limitations of the range.
- Explain the idea of deviation from the mean.
- Calculate variance for a population.
- Calculate sample variance.
- Distinguish between population variance and sample variance.
- Interpret variance in the context of semiconductor measurements.
- Compare the variability of two groups of semiconductor devices.

---

## 3.1 Why Is Central Tendency Not Enough?

In the previous chapter, we learned about the mean, median and mode.

These measures help us describe the **center** of a dataset.

However, a measure of central tendency does not tell us how much the observations differ from one another.

Consider two groups of semiconductor devices.

### Group A

$$
99,\;100,\;100,\;100,\;101\text{ nm}
$$

### Group B

$$
80,\;90,\;100,\;110,\;120\text{ nm}
$$

The mean of Group A is:

$$
\bar{x}_A
=
\frac{99+100+100+100+101}{5}
=
100\text{ nm}
$$

The mean of Group B is:

$$
\bar{x}_B
=
\frac{80+90+100+110+120}{5}
=
100\text{ nm}
$$

Therefore,

$$
\boxed{\bar{x}_A=\bar{x}_B=100\text{ nm}}
$$

If we only look at the mean, the two groups appear identical.

But clearly they are not.

The measurements in Group A are tightly clustered around 100 nm, while those in Group B are spread much more widely.

This leads to an important question:

> **How can we measure the amount of variation in a dataset?**

This is the purpose of **measures of dispersion**.

---

## 3.2 Understanding Variation

**Variation**, also called **dispersion**, refers to the extent to which observations differ from one another or spread around a central value.

In semiconductor technology, variation can occur:

- Between repeated measurements
- Between individual devices
- Between wafers
- Between manufacturing batches
- Between production runs
- Over time
- Under different environmental conditions

Variation is not necessarily a sign of failure.

The important questions are:

1. How large is the variation?
2. Is the variation acceptable?
3. Is the variation consistent with the expected process?
4. Has the variation changed over time?

Statistical measures allow us to answer these questions quantitatively.

Two measures introduced in this chapter are:

- **Range**
- **Variance**

Standard deviation will be developed in the next chapter.

---

## 3.3 Range

The simplest measure of dispersion is the **range**.

The range is the difference between the largest and smallest observations.

$$
\boxed{
\text{Range}=x_{\max}-x_{\min}
}
$$

where:

- \(x_{\max}\) = largest observation
- \(x_{\min}\) = smallest observation

The range provides a quick indication of the total spread of the data.

---

## 3.4 Semiconductor Example: Range of Threshold Voltage

Consider the threshold voltages of six MOSFETs:

$$
0.68,\;0.71,\;0.69,\;0.67,\;0.70,\;0.72\text{ V}
$$

The largest value is:

$$
x_{\max}=0.72\text{ V}
$$

The smallest value is:

$$
x_{\min}=0.67\text{ V}
$$

Therefore,

$$
\text{Range}
=
0.72-0.67
$$

$$
\boxed{\text{Range}=0.05\text{ V}}
$$

or

$$
\boxed{\text{Range}=50\text{ mV}}
$$

### Interpretation

The threshold voltages in this group span a total interval of 50 mV.

The range does not tell us how the observations are distributed within that interval. It simply tells us the distance between the extreme observations.

---

## 3.5 Another Example: Thin-Film Thickness

Suppose the thickness of a semiconductor film is measured on five wafers:

$$
99.8,\;100.2,\;100.1,\;99.9,\;100.0\text{ nm}
$$

The maximum value is:

$$
100.2\text{ nm}
$$

and the minimum value is:

$$
99.8\text{ nm}
$$

Therefore,

$$
\text{Range}
=
100.2-99.8
$$

$$
\boxed{\text{Range}=0.4\text{ nm}}
$$

This gives a quick indication of the spread in film thickness measurements.

---

## 3.6 Comparing Range Between Two Processes

Suppose two semiconductor manufacturing processes produce the following film-thickness measurements.

### Process A

$$
99.8,\;100.0,\;100.1,\;99.9,\;100.2\text{ nm}
$$

Range:

$$
100.2-99.8=0.4\text{ nm}
$$

### Process B

$$
98.0,\;101.0,\;99.5,\;102.0,\;97.5\text{ nm}
$$

Range:

$$
102.0-97.5=4.5\text{ nm}
$$

Process B has a much larger range.

This suggests that Process B produces substantially more variation in film thickness.

However, we should be careful.

> **A larger range suggests greater spread, but the range alone does not tell us how all observations are distributed.**

This is one reason why we need more informative measures such as variance and standard deviation.

---

## 3.7 Limitations of the Range

The range is easy to calculate, but it has important limitations.

### Limitation 1: It uses only two observations

The range depends only on:

- The largest observation
- The smallest observation

All other observations are ignored.

For example:

$$
99,\;100,\;100,\;100,\;101
$$

and

$$
99,\;99,\;100,\;101,\;101
$$

have the same range:

$$
101-99=2
$$

but their internal distributions are different.

### Limitation 2: It is sensitive to extreme observations

If one unusual measurement occurs, the range can change substantially.

### Limitation 3: It does not describe the distribution

The range tells us the total span, but not how observations are distributed between the minimum and maximum.

Therefore, range is useful as a quick measure of spread, but it is not sufficient for detailed statistical analysis.

---

## 3.8 From Range to Variance

To develop a more informative measure of variation, we need to consider **every observation**.

Suppose the observations are:

$$
x_1,x_2,\ldots,x_n
$$

and their mean is:

$$
\bar{x}
$$

We can calculate how far each observation is from the mean.

This difference is called the **deviation from the mean**.

For the \(i\)-th observation:

$$
\boxed{
d_i=x_i-\bar{x}
}
$$

The deviation may be:

- Positive, if \(x_i>\bar{x}\)
- Negative, if \(x_i<\bar{x}\)
- Zero, if \(x_i=\bar{x}\)

---

## 3.9 Example: Deviations from the Mean

Consider the following threshold-voltage measurements:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

The mean is:

$$
\bar{x}=0.70\text{ V}
$$

Now calculate the deviations.

| \(x_i\) (V) | \(x_i-\bar{x}\) (V) |
|---:|---:|
| 0.68 | -0.02 |
| 0.69 | -0.01 |
| 0.70 | 0.00 |
| 0.71 | +0.01 |
| 0.72 | +0.02 |

Notice something interesting:

$$
(-0.02)+(-0.01)+0+(0.01)+(0.02)=0
$$

In general,

$$
\boxed{
\sum_{i=1}^{n}(x_i-\bar{x})=0
}
$$

This happens because the mean is the balancing point of the observations.

If we simply add the deviations, the positive and negative deviations cancel.

Therefore, we need another way to combine the deviations so that they do not cancel.

---

## 3.10 Squared Deviations

A common solution is to square each deviation.

For the previous example:

| \(x_i\) (V) | Deviation (V) | Squared Deviation (V²) |
|---:|---:|---:|
| 0.68 | -0.02 | 0.0004 |
| 0.69 | -0.01 | 0.0001 |
| 0.70 | 0.00 | 0.0000 |
| 0.71 | +0.01 | 0.0001 |
| 0.72 | +0.02 | 0.0004 |

The squared deviations are all non-negative.

Their sum is:

$$
0.0004+0.0001+0+0.0001+0.0004
=
0.0010
$$

This provides the basis for calculating **variance**.

---

## 3.11 Population Variance

If the dataset contains the entire population of interest, the **population variance** is:

$$
\boxed{
\sigma^2=
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
$$

where:

- \(\sigma^2\) = population variance
- \(N\) = population size
- \(x_i\) = population observation
- \(\mu\) = population mean

The population variance measures the average squared deviation from the population mean.

---

## 3.12 Worked Example: Population Variance

Consider five semiconductor measurements:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

We already know that:

$$
\mu=0.70\text{ V}
$$

The deviations are:

$$
-0.02,\;-0.01,\;0,\;+0.01,\;+0.02
$$

The squared deviations are:

$$
0.0004,\;0.0001,\;0,\;0.0001,\;0.0004
$$

Therefore:

$$
\sum(x_i-\mu)^2=0.0010
$$

Since there are five observations:

$$
N=5
$$

Therefore,

$$
\sigma^2
=
\frac{0.0010}{5}
$$

$$
\boxed{
\sigma^2=0.0002\text{ V}^2
}
$$

The unit of variance is the **square of the original unit**.

Since the original measurements are in volts, variance is expressed in:

$$
\text{V}^2
$$

This squared unit can make variance less intuitive to interpret directly.

That is one reason standard deviation, which will be introduced in the next chapter, is so useful.

---

## 3.13 Sample Variance

In many real situations, we do not measure the entire population.

Instead, we measure a sample.

Suppose a sample contains \(n\) observations.

The **sample variance** is:

$$
\boxed{
s^2=
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
$$

where:

- \(s^2\) = sample variance
- \(n\) = sample size
- \(x_i\) = sample observation
- \(\bar{x}\) = sample mean

Notice that the denominator is:

$$
n-1
$$

rather than:

$$
n
$$

This distinction is important.

---

## 3.14 Why Do We Use \(n-1\) for Sample Variance?

Suppose we want to learn about a large population of semiconductor devices, but we test only a sample of devices.

The sample mean is calculated from the same observations used to calculate the variance.

Because the population mean is not known, the sample variance uses:

$$
n-1
$$

in the denominator.

The quantity \(n-1\) is called the **degrees of freedom** in this context.

For this introductory course, the practical rule is:

> **Use \(N\) when calculating variance for the complete population, and use \(n-1\) when calculating variance from a sample to estimate population variability.**

Students should not simply memorize the denominator. They should first identify whether the data represent a population or a sample.

---

## 3.15 Worked Example: Sample Variance

Suppose five MOSFETs are selected from a much larger production batch.

Their threshold voltages are:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

Because these five devices represent a sample from a larger population, we use sample variance.

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
0.0010
$$

The sample size is:

$$
n=5
$$

Therefore,

$$
s^2
=
\frac{0.0010}{5-1}
$$

$$
s^2
=
\frac{0.0010}{4}
$$

Hence,

$$
\boxed{
s^2=0.00025\text{ V}^2
}
$$

Notice that this is slightly larger than the population variance calculated earlier:

$$
\sigma^2=0.0002\text{ V}^2
$$

The difference occurs because the denominators are different.

---

## 3.16 Population Variance vs Sample Variance

The two formulas can be compared as follows.

### Population variance

$$
\boxed{
\sigma^2=
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
$$

### Sample variance

$$
\boxed{
s^2=
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
$$

| Situation | Mean | Denominator |
|---|---|---:|
| Population | \(\mu\) | \(N\) |
| Sample | \(\bar{x}\) | \(n-1\) |

### Practical Semiconductor Example

If we have measurements for **every device in the population being studied**, population variance may be appropriate.

If we test **100 devices selected from 100,000 manufactured devices**, those 100 devices are a sample, and sample variance is generally used when estimating population variability.

---

## 3.17 Comparing Two Device Groups Using Variance

Consider two groups of semiconductor devices.

### Group A

$$
99,\;100,\;100,\;100,\;101\text{ nm}
$$

### Group B

$$
80,\;90,\;100,\;110,\;120\text{ nm}
$$

Both have mean:

$$
100\text{ nm}
$$

But the deviations from the mean are very different.

For Group A:

$$
-1,\;0,\;0,\;0,\;+1
$$

For Group B:

$$
-20,\;-10,\;0,\;+10,\;+20
$$

The squared deviations for Group B are much larger.

Therefore, the variance of Group B is much larger.

This confirms what we could already see from the data:

> **Group B has substantially greater variability than Group A.**

Variance gives us a numerical way to express this difference.

---

## 3.18 Interpretation of Variance

Variance measures the average squared distance of observations from their mean.

A smaller variance generally indicates that observations are more tightly clustered around the mean.

A larger variance indicates greater spread.

For semiconductor measurements:

### Small variance

May indicate:

- Consistent device characteristics
- Stable experimental measurements
- Good process uniformity

### Large variance

May indicate:

- Greater device-to-device variation
- An unstable process
- Increased measurement variation
- Different operating conditions
- Possible manufacturing issues

However, variance must always be interpreted in context.

A "large" variance for one physical quantity may be small for another.

Therefore, comparison should consider:

- The units
- The scale of the measurement
- The target specification
- The engineering application

---

## 3.19 Range vs Variance

Range and variance both measure dispersion, but they use the data differently.

| Feature | Range | Variance |
|---|---|---|
| Uses all observations? | No | Yes |
| Based on extreme values? | Yes | No, all observations contribute |
| Easy to calculate? | Very easy | More calculation required |
| Sensitive to extreme values? | Yes | Yes, because deviations are squared |
| Units | Same as data | Squared units |
| Describes overall variation? | Limited | More informative |

The range is useful for a quick assessment.

Variance provides a more systematic measure because it considers every observation.

---

## 3.20 Why Are Deviations Squared?

Students often ask why we use:

$$
(x_i-\bar{x})^2
$$

instead of simply:

$$
x_i-\bar{x}
$$

The main reason is that deviations from the mean add to zero:

$$
\sum(x_i-\bar{x})=0
$$

If we used the raw deviations, positive and negative differences would cancel.

Squaring solves this problem:

$$
(x_i-\bar{x})^2\geq0
$$

Therefore, all observations contribute non-negative quantities to the variance.

Squaring also gives greater weight to observations that are farther from the mean.

For example:

$$
1^2=1
$$

but

$$
3^2=9
$$

Therefore, a deviation of 3 contributes much more to the variance than a deviation of 1.

---

## 3.21 Common Mistakes

### Mistake 1: Confusing range with variance

Range is:

$$
x_{\max}-x_{\min}
$$

Variance involves squared deviations from the mean.

### Mistake 2: Forgetting to calculate the mean first

Variance requires deviations from the mean.

### Mistake 3: Using \(n\) instead of \(n-1\) for sample variance

Always identify whether the data represent a population or a sample.

### Mistake 4: Forgetting to square deviations

Negative deviations must become positive through squaring.

### Mistake 5: Interpreting variance as having the same units as the original data

If measurements are in volts, variance is in:

$$
\text{V}^2
$$

not volts.

### Mistake 6: Assuming larger variance automatically means poor quality

Variance must be compared with the engineering specification and the intended application.

---

## 3.22 Summary

A measure of central tendency tells us about the center of a dataset, but it does not describe how widely the observations are spread.

**Dispersion** describes the variation among observations.

### Range

$$
\boxed{
\text{Range}=x_{\max}-x_{\min}
}
$$

The range is simple and useful for a quick assessment of spread, but it uses only the minimum and maximum observations.

### Variance

Variance considers the squared deviations of all observations from their mean.

For a population:

$$
\boxed{
\sigma^2=
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
$$

For a sample:

$$
\boxed{
s^2=
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
$$

The main idea is:

> **Range gives a quick measure of total spread, while variance uses all observations to quantify their squared deviations from the mean.**

In semiconductor applications, these measures help quantify:

- Device-to-device variation
- Experimental variation
- Process variation
- Measurement consistency

Variance is expressed in squared units, so we need another measure that returns to the original units of measurement.

That measure is **standard deviation**, which will be studied in the next chapter.

---

## 3.23 Key Formulae

### Range

$$
\boxed{
R=x_{\max}-x_{\min}
}
$$

### Deviation from the Mean

$$
\boxed{
d_i=x_i-\bar{x}
}
$$

### Population Variance

$$
\boxed{
\sigma^2=
\frac{1}{N}
\sum_{i=1}^{N}(x_i-\mu)^2
}
$$

### Sample Variance

$$
\boxed{
s^2=
\frac{1}{n-1}
\sum_{i=1}^{n}(x_i-\bar{x})^2
}
$$

---

## 3.24 Review Questions

### Conceptual Questions

1. Why is a measure of central tendency not sufficient to describe a dataset?
2. What is meant by dispersion?
3. Define the range.
4. What are the limitations of the range?
5. What is a deviation from the mean?
6. Why are deviations squared when calculating variance?
7. Define population variance.
8. Define sample variance.
9. Why is \(n-1\) used in the sample variance formula?
10. Why is variance expressed in squared units?

### Semiconductor Application Questions

11. Why is variation in threshold voltage important in semiconductor device manufacturing?
12. How can range be used to compare two batches of semiconductor devices?
13. Why might variance be more informative than range when studying process variation?
14. What could a large variance in film thickness measurements indicate?
15. Explain why a small variance may be desirable in a semiconductor manufacturing process.

---

## 3.25 Practice Problems

### Problem 1 — Range

The threshold voltages of six MOSFETs are:

$$
0.68,\;0.71,\;0.69,\;0.67,\;0.70,\;0.72\text{ V}
$$

Calculate the range.

### Problem 2 — Range of Film Thickness

The following film-thickness measurements are obtained:

$$
99.8,\;100.2,\;100.1,\;99.9,\;100.0\text{ nm}
$$

Calculate the range.

### Problem 3 — Deviations

The forward voltages of five diodes are:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

1. Calculate the mean.
2. Calculate the deviation of each observation from the mean.
3. Verify that the sum of deviations is zero.

### Problem 4 — Population Variance

The complete set of measurements from a small experiment is:

$$
9,\;10,\;10,\;11,\;10
$$

Calculate:

1. Mean
2. Deviations from the mean
3. Squared deviations
4. Population variance

### Problem 5 — Sample Variance

A sample of five semiconductor devices has threshold voltages:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

Calculate the sample variance.

### Problem 6 — Compare Two Processes

Two processes produce the following film-thickness measurements.

**Process A**

$$
99,\;100,\;100,\;100,\;101\text{ nm}
$$

**Process B**

$$
80,\;90,\;100,\;110,\;120\text{ nm}
$$

1. Calculate the mean for each process.
2. Calculate the range for each process.
3. Calculate the population variance for each process.
4. Which process shows greater variation?
5. Explain your conclusion in the context of semiconductor manufacturing.

---

## 3.26 Looking Ahead

In this chapter, we learned how to quantify the spread of observations using range and variance.

Variance is useful, but its units are squared.

For example, if threshold voltage is measured in volts, variance is measured in:

$$
\text{V}^2
$$

This makes direct interpretation less intuitive.

The next question is:

> **Can we express the variation in the same units as the original measurements?**

Yes.

Taking the square root of variance gives us the **standard deviation**.

The next chapter will develop:

$$
\boxed{\text{Standard Deviation and Coefficient of Variation}}
$$