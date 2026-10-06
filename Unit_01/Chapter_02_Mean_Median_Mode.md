# Chapter 2 — Mean, Median and Mode

## Learning Objectives

After completing this chapter, students will be able to:

- Explain the purpose of measures of central tendency.
- Calculate the arithmetic mean of a set of observations.
- Interpret the mean in the context of semiconductor measurements.
- Calculate the median for odd and even numbers of observations.
- Explain why the median can be useful when observations contain extreme values.
- Identify the mode of a dataset.
- Compare mean, median and mode.
- Select an appropriate measure of central tendency for a given dataset.

---

## 2.1 Why Do We Need a Measure of Central Tendency?

A semiconductor experiment may produce many measurements.

For example, suppose the threshold voltage of five MOSFETs is measured:

| Device | Threshold Voltage (V) |
|---:|---:|
| 1 | 0.68 |
| 2 | 0.71 |
| 3 | 0.69 |
| 4 | 0.67 |
| 5 | 0.70 |

Looking at five numbers individually is possible, but it is often more useful to describe the dataset using a single representative value.

We may ask:

> **What is the typical threshold voltage of these devices?**

A statistical measure that gives an indication of the center or typical location of a dataset is called a **measure of central tendency**.

The three basic measures of central tendency introduced in this chapter are:

- Mean
- Median
- Mode

These measures answer the question:

> **Where is the center of the data?**

However, they do not tell us everything about the data. In particular, they do not tell us how widely the observations vary. Measures of dispersion such as range, variance and standard deviation will be introduced in later chapters.

---

## 2.2 Arithmetic Mean

The arithmetic mean is commonly called the **average**.

For a set of \(n\) observations

$$
x_1,x_2,x_3,\ldots,x_n
$$

the arithmetic mean is given by

$$
\boxed{
\bar{x}=\frac{x_1+x_2+\cdots+x_n}{n}
}
$$

Using summation notation,

$$
\boxed{
\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_i
}
$$

where:

- $\bar{x}$ = arithmetic mean
- \(x_i\) = the \(i\)-th observation
- \(n\) = number of observations

The mean is obtained by:

1. Adding all observations.
2. Dividing the total by the number of observations.

---

## 2.3 Semiconductor Example: Mean Threshold Voltage

Consider the threshold voltages of five MOSFETs:

$$
0.68,\;0.71,\;0.69,\;0.67,\;0.70\text{ V}
$$
There are five observations, so

$$
n=5
$$
The mean is

$$
\bar{x}
=
\frac{0.68+0.71+0.69+0.67+0.70}{5}
$$
First calculate the sum:

$$
0.68+0.71+0.69+0.67+0.70=3.45
$$
Therefore,

$$
\bar{x}=\frac{3.45}{5}
$$
and

$$
\boxed{\bar{x}=0.69\text{ V}}
$$
### Interpretation

The mean threshold voltage of the five tested devices is:

$$
\boxed{0.69\text{ V}}
$$
This does **not** mean that every MOSFET has a threshold voltage of exactly \(0.69\) V.

It means that \(0.69\) V is the arithmetic center of these five observations.

This distinction is important.

> **The mean summarizes a dataset; it does not imply that every observation is equal to the mean.**

---

## 2.4 Mean of Repeated Experimental Measurements

Consider repeated measurements of the forward voltage of a diode:

$$
0.681,\;0.684,\;0.679,\;0.683,\;0.681\text{ V}
$$
The mean is

$$
\bar{x}
=
\frac{0.681+0.684+0.679+0.683+0.681}{5}
$$
The sum is

$$
3.408
$$
Therefore,

$$
\bar{x}
=
\frac{3.408}{5}
=
0.6816\text{ V}
$$
Thus,

$$
\boxed{\bar{x}=0.6816\text{ V}}
$$
Depending on the required measurement precision, this may be reported appropriately after considering significant figures and measurement uncertainty.

The important point is that the five measurements have been summarized by one representative numerical value.

---

## 2.5 Why Does the Mean Use Every Observation?

One important property of the arithmetic mean is that **every observation contributes to its calculation**.

Suppose the threshold voltages are:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$
The mean is

$$
\bar{x}
=
\frac{0.68+0.69+0.70+0.71+0.72}{5}
=
0.70\text{ V}
$$
Now suppose the last observation changes from \(0.72\) V to \(0.80\) V.

The new mean becomes

$$
\bar{x}
=
\frac{0.68+0.69+0.70+0.71+0.80}{5}
$$
$$
\bar{x}
=
\frac{3.58}{5}
=
0.716\text{ V}
$$
The mean has changed because one observation changed.

This is a useful property, but it also creates an important limitation:

> **The mean can be strongly affected by an unusually large or unusually small observation.**

---

## 2.6 Effect of an Unusual Observation

Consider the following leakage-current measurements:

$$
4,\;5,\;5,\;6,\;5\;\mu\text{A}
$$
The mean is

$$
\bar{x}
=
\frac{4+5+5+6+5}{5}
=
5\;\mu\text{A}
$$
Now suppose one measurement is affected by an abnormal condition and becomes:

$$
40\;\mu\text{A}
$$
The new dataset is:

$$
4,\;5,\;5,\;6,\;40\;\mu\text{A}
$$
The mean becomes

$$
\bar{x}
=
\frac{4+5+5+6+40}{5}
=
\frac{60}{5}
=
12\;\mu\text{A}
$$
The mean has increased from \(5\) \(\mu\text{A}\) to \(12\) \(\mu\text{A}\).

However, most observations are still close to \(5\) \(\mu\text{A}\).

This illustrates why an extreme observation can strongly influence the mean.

Such an observation may be caused by:

- An instrument problem
- A measurement error
- A genuine abnormal device
- A special experimental condition

We should **not automatically remove an unusual observation**. First, we should investigate why it occurred.

---

## 2.7 Median

The **median** is the middle value of an ordered dataset.

To find the median:

1. Arrange the observations in ascending or descending order.
2. Identify the middle position.

The calculation depends on whether the number of observations is odd or even.

---

## 2.8 Median for an Odd Number of Observations

Consider five threshold-voltage measurements:

$$
0.68,\;0.71,\;0.69,\;0.67,\;0.70
$$
First arrange them in ascending order:

$$
0.67,\;0.68,\;0.69,\;0.70,\;0.71
$$
There are five observations.

The middle observation is the third observation.

Therefore,

$$
\boxed{\text{Median}=0.69\text{ V}}
$$
### Position of the Median

For \(n\) observations, when \(n\) is odd, the position of the median is

$$
\boxed{
\frac{n+1}{2}
}
$$
For \(n=5\),

$$
\frac{5+1}{2}=3
$$
Therefore, the third observation is the median.

---

## 2.9 Median for an Even Number of Observations

Now consider six measurements:

$$
0.67,\;0.68,\;0.69,\;0.70,\;0.71,\;0.72
$$
There is no single middle observation.

The two middle observations are:

$$
0.69,\quad0.70
$$
The median is their average:

$$
\text{Median}
=
\frac{0.69+0.70}{2}
$$
$$
\boxed{\text{Median}=0.695\text{ V}}
$$
For an even number of observations, the median is therefore the average of the two middle observations after arranging the data in order.

---

## 2.10 Mean and Median in the Presence of an Extreme Value

Consider leakage-current measurements:

$$
4,\;5,\;5,\;6,\;40\;\mu\text{A}
$$
The mean is:

$$
\bar{x}=12\;\mu\text{A}
$$
The data are already arranged in ascending order, so the median is:

$$
\boxed{\text{Median}=5\;\mu\text{A}}
$$
Notice the difference:

$$
\text{Mean}=12\;\mu\text{A}
$$
$$
\text{Median}=5\;\mu\text{A}
$$
Most measurements are around \(5\;\mu\text{A}\), while one observation is much larger.

The median is not affected as strongly by the extreme observation.

Therefore:

> **The median is often useful when a dataset contains extreme observations or is strongly skewed.**

However, this does not mean that the median is always better than the mean. The appropriate measure depends on the purpose and characteristics of the data.

---

## 2.11 Mode

The **mode** is the value that occurs most frequently in a dataset.

Consider the following number of defective devices observed across several test runs:

$$
2,\;3,\;3,\;4,\;3,\;5,\;3
$$
The value \(3\) occurs four times.

Therefore,

$$
\boxed{\text{Mode}=3}
$$
The mode can be useful when the most frequently occurring value is important.

---

## 2.12 Semiconductor Example of Mode

Suppose the number of devices failing a particular screening test is recorded for several production lots:

$$
2,\;4,\;3,\;4,\;5,\;4,\;3,\;4
$$
The value \(4\) occurs most frequently.

Therefore,

$$
\boxed{\text{Mode}=4}
$$
In this example, the mode tells us the most frequently observed number of failures per lot.

### Important Limitation

For continuous physical measurements such as:

- Voltage
- Current
- Temperature
- Film thickness

exact repeated values may be uncommon.

Therefore, the mode may not always be useful for raw continuous measurement data.

The mode is more useful when:

- Values repeat frequently
- Data are discrete
- Measurements have been grouped into categories or intervals
- The most common category is of interest

---

## 2.13 Mean, Median and Mode — Comparison

The three measures describe the center of a dataset in different ways.

| Measure | Meaning | Main characteristic |
|---|---|---|
| **Mean** | Arithmetic average | Uses every observation |
| **Median** | Middle value | Less affected by extreme observations |
| **Mode** | Most frequently occurring value | Identifies the most common value |

Consider the dataset:

$$
4,\;5,\;5,\;6,\;40
$$
Mean:

$$
\bar{x}=12
$$
Median:

$$
\text{Median}=5
$$
Mode:

$$
\text{Mode}=5
$$
The three measures provide different information.

The mean is influenced strongly by the value \(40\).

The median identifies the middle observation.

The mode identifies the most frequently occurring value.

---

## 2.14 When Should We Use Mean, Median or Mode?

There is no single measure that is always best.

### Mean

The mean is useful when:

- All observations are important.
- The data are reasonably balanced.
- We want an arithmetic average.
- Mathematical calculations based on all observations are required.

### Median

The median is useful when:

- Extreme observations are present.
- The distribution is strongly skewed.
- We want the middle observation.
- A typical value should not be strongly influenced by extreme observations.

### Mode

The mode is useful when:

- Repeated values occur.
- The most common value is important.
- Data are discrete or categorical.

---

## 2.15 A Semiconductor Data Comparison

Suppose the thickness of a semiconductor layer is measured:

$$
98,\;99,\;100,\;100,\;101,\;102,\;100\text{ nm}
$$
The mean is:

$$
\bar{x}
=
\frac{98+99+100+100+101+102+100}{7}
$$
$$
\bar{x}
=
\frac{700}{7}
=
100\text{ nm}
$$
The ordered data are already:

$$
98,\;99,\;100,\;100,\;100,\;101,\;102
$$
Therefore,

$$
\text{Median}=100\text{ nm}
$$
The value \(100\) occurs three times, so:

$$
\text{Mode}=100\text{ nm}
$$
Thus:

$$
\boxed{
\text{Mean}=\text{Median}=\text{Mode}=100\text{ nm}
}
$$
When these measures are close to one another, the dataset may be relatively balanced around its center.

---

## 2.16 Worked Example — Comparing Two Device Groups

Two groups of devices have the following threshold-voltage measurements.

### Group A

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$
The mean is:

$$
\bar{x}_A
=
\frac{0.68+0.69+0.70+0.71+0.72}{5}
=
0.70\text{ V}
$$
The median is:

$$
\boxed{\text{Median}_A=0.70\text{ V}}
$$
### Group B

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.90\text{ V}
$$
The mean is:

$$
\bar{x}_B
=
\frac{0.68+0.69+0.70+0.71+0.90}{5}
$$
$$
\bar{x}_B
=
\frac{3.68}{5}
=
0.736\text{ V}
$$
The median is:

$$
\boxed{\text{Median}_B=0.70\text{ V}}
$$
Notice that the median remains \(0.70\) V, while the mean increases to \(0.736\) V because of the \(0.90\) V observation.

This example demonstrates why engineers should examine the data rather than relying on a single summary number.

---

## 2.17 Important Points About the Mean

The arithmetic mean has several useful properties.

### Property 1: Every observation contributes to the mean

Changing any observation generally changes the mean.

### Property 2: The mean is sensitive to extreme observations

Very large or very small observations can pull the mean toward them.

### Property 3: The mean is expressed in the same unit as the observations

If threshold voltage is measured in volts, the mean is also measured in volts.

If film thickness is measured in nanometres, the mean is also measured in nanometres.

### Property 4: The mean is useful for further mathematical analysis

The arithmetic mean is widely used in statistical calculations and forms the basis for measures such as variance and standard deviation.

---

## 2.18 Common Mistakes

### Mistake 1: Forgetting to arrange data before finding the median

The median must be determined from the ordered data.

### Mistake 2: Dividing by the wrong number

For the arithmetic mean, divide by the number of observations.

If there are \(n\) observations:

$$
\bar{x}=\frac{\sum x_i}{n}
$$
### Mistake 3: Assuming the mean is always the "best" typical value

The mean can be strongly influenced by extreme observations.

### Mistake 4: Confusing median with average

The median is the middle value after ordering the data.

For an even number of observations, it is the average of the two middle values.

### Mistake 5: Assuming an unusual observation should automatically be removed

An unusual value should be investigated before deciding whether it is an error, a valid observation, or evidence of an unusual device or condition.

---

## 2.19 Summary

Measures of central tendency provide numerical descriptions of the center or typical location of a dataset.

The three basic measures introduced in this chapter are:

### Mean

$$
\boxed{
\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_i
}
$$
The mean uses every observation but can be affected by extreme values.

### Median

The median is the middle value after arranging the observations in order.

For odd \(n\):

$$
\boxed{
\text{Median position}=\frac{n+1}{2}
}
$$
For even \(n\), the median is the average of the two middle observations.

### Mode

The mode is the most frequently occurring value.

The key distinction is:

> **Mean uses all observations, median identifies the middle observation, and mode identifies the most frequently occurring observation.**

In semiconductor applications, these measures can be used to summarize quantities such as threshold voltage, leakage current, film thickness, resistance, sensor output, and other measurements.

However, central tendency alone does not tell us how much the observations vary.

That leads to the next group of statistical concepts: **measures of dispersion**.

---

## 2.20 Key Formulae

### Arithmetic Mean

$$
\boxed{
\bar{x}=\frac{x_1+x_2+\cdots+x_n}{n}
}
$$
or

$$
\boxed{
\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_i
}
$$
### Median for Odd \(n\)

$$
\boxed{
\text{Median position}=\frac{n+1}{2}
}
$$
### Median for Even \(n\)

$$
\boxed{
\text{Median}
=
\frac{\text{two middle observations}}{2}
}
$$
### Mode

$$
\boxed{
\text{Mode}=\text{most frequently occurring value}
}
$$
---

## 2.21 Review Questions

### Conceptual Questions

1. What is meant by a measure of central tendency?
2. Why do we need measures of central tendency?
3. Define the arithmetic mean.
4. Why is the mean affected by extreme observations?
5. Define the median.
6. What is the difference between the median for an odd and even number of observations?
7. Define the mode.
8. Why may the mode be less useful for continuous semiconductor measurements?
9. Why is the mean not always sufficient to describe a dataset?
10. Compare mean, median and mode.

### Semiconductor Application Questions

11. Why might the mean threshold voltage of a batch of MOSFETs be useful?
12. Why might the median leakage current be more informative than the mean when one device has an unusually high leakage current?
13. Give two examples of semiconductor measurements for which the mean would be useful.
14. Give an example where the mode could be useful in semiconductor manufacturing or testing.
15. Explain why an unusual measurement should not automatically be removed from a dataset.

---

## 2.22 Practice Problems

### Problem 1 — Mean of Device Measurements

The threshold voltages of six MOSFETs are:

$$
0.68,\;0.71,\;0.69,\;0.70,\;0.72,\;0.70\text{ V}
$$
Calculate the arithmetic mean.

### Problem 2 — Median

The forward voltages of seven diodes are:

$$
0.69,\;0.68,\;0.71,\;0.70,\;0.68,\;0.69,\;0.72\text{ V}
$$
1. Arrange the data in ascending order.
2. Find the median.

### Problem 3 — Even Number of Observations

The resistance measurements of six components are:

$$
98,\;101,\;100,\;99,\;103,\;102\;\Omega
$$
Calculate the median.

### Problem 4 — Mode

The number of defective devices detected in eight production lots is:

$$
2,\;3,\;4,\;3,\;5,\;3,\;4,\;3
$$
Find the mode.

### Problem 5 — Effect of an Extreme Observation

The leakage currents of five devices are:

$$
4,\;5,\;5,\;6,\;40\;\mu\text{A}
$$
1. Calculate the mean.
2. Find the median.
3. Compare the two values.
4. Explain why they are substantially different.

### Problem 6 — Interpretation

Two device batches have the following threshold voltages:

**Batch A**

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72
$$
**Batch B**

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.90
$$
Calculate the mean and median for both batches and explain what the results suggest.

---

## 2.23 Looking Ahead

In this chapter, we learned how to describe the **center** of a dataset.

But two datasets can have the same mean and very different amounts of variation.

For example, consider:

$$
99,\;100,\;100,\;100,\;101
$$
and

$$
80,\;90,\;100,\;110,\;120
$$
Both have a mean of:

$$
100
$$
but their variability is clearly different.

Therefore, our next question is:

> **How can we measure the amount of variation in a dataset?**

This leads to the study of **range, variance and standard deviation**.
