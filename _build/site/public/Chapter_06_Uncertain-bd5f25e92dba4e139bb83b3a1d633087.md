# Chapter 6 — Uncertainty, Accuracy, Precision and Significant Figures

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why uncertainty is associated with experimental measurements.
- Distinguish between error and uncertainty.
- Explain the meaning of accuracy and precision.
- Distinguish between accuracy and precision using semiconductor examples.
- Explain the meaning of significant figures.
- Identify significant and non-significant digits in measured values.
- Apply basic rules for significant figures.
- Round numerical results appropriately.
- Understand the relationship between instrument resolution and reported precision.
- Report semiconductor measurements in a scientifically meaningful form.

---

## 6.1 Why Do We Need Uncertainty?

In the previous chapter, we studied measurement error.

Suppose a semiconductor device is measured and the result is:

$$
V=5.02\text{ V}
$$

A real measurement is never perfectly exact. It may be affected by instrument resolution, calibration, electrical noise, temperature, environmental conditions, measurement procedure, and other factors.

Therefore, a measurement should not automatically be interpreted as an infinitely precise number.

This leads to the concept of **measurement uncertainty**.

---

## 6.2 What Is Measurement Uncertainty?

Measurement uncertainty describes the limited knowledge associated with a measured quantity.

A simple way of reporting a measurement is:

$$
\boxed{x=x_m\pm u}
$$

where:

- $x_m$ = measured value
- $u$ = uncertainty

For example:

$$
\boxed{V=5.00\pm0.02\text{ V}}
$$

A simple interval associated with this statement is:

$$
4.98\text{ V}\leq V\leq5.02\text{ V}
$$

This is an introductory interpretation. Formal uncertainty evaluation can involve several sources and statistical methods.

---

## 6.3 Error and Uncertainty Are Not the Same

### Error

Error compares a measured value with a reference or accepted value:

$$
\boxed{E=x_m-x_r}
$$

### Uncertainty

Uncertainty describes the limited knowledge associated with the measurement:

$$
x=x_m\pm u
$$

The key distinction is:

> **Error describes the difference from a reference value, whereas uncertainty describes the range of values associated with the measurement.**

---

## 6.4 Absolute Uncertainty

A measurement may be reported with an absolute uncertainty.

For example:

$$
R=100.0\pm0.5\Omega
$$

The absolute uncertainty is:

$$
\boxed{u_R=0.5\Omega}
$$

The uncertainty has the same units as the measured quantity.

Examples include:

- Voltage uncertainty → V
- Current uncertainty → A
- Resistance uncertainty → $\Omega$
- Film-thickness uncertainty → nm

---

## 6.5 Relative and Percentage Uncertainty

Relative uncertainty compares the uncertainty with the measured value:

$$
\boxed{
u_r=\frac{u}{|x_m|}
}
$$

Percentage uncertainty is:

$$
\boxed{
u_{\%}=
\frac{u}{|x_m|}\times100
}
$$

### Example

Suppose:

$$
V=5.00\pm0.02\text{ V}
$$

Then:

$$
u_{\%}
=
\frac{0.02}{5.00}\times100
=
0.4\%
$$

Therefore:

$$
\boxed{u_{\%}=0.4\%}
$$

---

## 6.6 Semiconductor Example — Film Thickness

Suppose a semiconductor thin film is measured as:

$$
t=100.0\pm0.5\text{ nm}
$$

The absolute uncertainty is:

$$
\boxed{u_t=0.5\text{ nm}}
$$

The relative uncertainty is:

$$
u_r=\frac{0.5}{100.0}=0.005
$$

Therefore:

$$
\boxed{u_{\%}=0.5\%}
$$

This tells us that the uncertainty is small relative to the measured film thickness.

---

## 6.7 Accuracy

**Accuracy** describes how close a measured value is to the accepted or reference value.

Suppose the accepted threshold voltage is:

$$
V_r=0.70\text{ V}
$$

and an instrument measures:

$$
V_m=0.701\text{ V}
$$

The measurement is close to the reference value and can therefore be described as having good accuracy.

> **Accuracy is about closeness to the target or accepted value.**

---

## 6.8 Precision

**Precision** describes the degree of agreement or consistency among repeated measurements.

Suppose the same semiconductor parameter is measured five times:

$$
0.700,\;0.701,\;0.700,\;0.699,\;0.700\text{ V}
$$

The measurements are very close to one another.

Therefore, the measurement procedure has high precision.

> **Precision is about consistency among repeated measurements.**

A small standard deviation generally indicates greater precision among repeated observations.

---

## 6.9 Accuracy vs Precision

Accuracy and precision are different concepts.

### High Accuracy and High Precision

Measurements:

$$
0.699,\;0.700,\;0.701,\;0.700\text{ V}
$$

Accepted value:

$$
0.700\text{ V}
$$

The measurements are close to one another and close to the accepted value.

Therefore:

- High precision
- High accuracy

### High Precision but Low Accuracy

Measurements:

$$
0.750,\;0.751,\;0.750,\;0.749,\;0.750\text{ V}
$$

Accepted value:

$$
0.700\text{ V}
$$

The measurements are very close to one another but far from the accepted value.

Therefore:

- High precision
- Low accuracy

This could occur because of a calibration problem.

### Lower Precision

Consider:

$$
0.68,\;0.72,\;0.69,\;0.71,\;0.70\text{ V}
$$

The measurements vary more widely. Their average may still be close to the accepted value, but the repeatability is lower.

---

## 6.10 A Simple Way to Remember

> **Accuracy = closeness to the target.**

> **Precision = closeness to each other.**

This distinction is extremely important in laboratory measurements.

---

## 6.11 Semiconductor Example — Device Testing

Suppose the accepted threshold voltage of a reference device is:

$$
V_T=0.70\text{ V}
$$

### Test A

$$
0.699,\;0.700,\;0.701,\;0.700,\;0.699\text{ V}
$$

These measurements are close to each other and close to the accepted value.

Therefore, Test A shows:

- High precision
- High accuracy

### Test B

$$
0.780,\;0.781,\;0.780,\;0.779,\;0.780\text{ V}
$$

These measurements are very close to each other but far from the accepted value.

Therefore, Test B shows:

- High precision
- Low accuracy

A possible explanation could be an instrument calibration problem.

---

## 6.12 Significant Figures

**Significant figures** are the digits in a measured or calculated value that communicate meaningful information about its precision.

For example:

$$
0.00452\text{ V}
$$

contains three significant figures:

$$
4,\;5,\;2
$$

The zeros before $4$ are not significant because they only locate the decimal point.

Now consider:

$$
4.520\text{ V}
$$

This has four significant figures:

$$
4,\;5,\;2,\;0
$$

The final zero is significant because it communicates the precision of the measurement.

> **Significant figures communicate meaningful numerical precision; they do not guarantee accuracy.**

---

## 6.13 Rules for Significant Figures

### Rule 1 — Non-zero digits are significant

All digits from 1 to 9 are significant.

For example:

$$
3.472
$$

has four significant figures.

### Rule 2 — Zeros between non-zero digits are significant

Consider:

$$
3.05
$$

The zero lies between 3 and 5.

Therefore:

$$
\boxed{3.05\text{ has 3 significant figures}}
$$

### Rule 3 — Leading zeros are not significant

Consider:

$$
0.00452
$$

Therefore:

$$
\boxed{0.00452\text{ has 3 significant figures}}
$$

### Rule 4 — Trailing zeros after a decimal point are significant

Consider:

$$
2.50
$$

Therefore:

$$
\boxed{2.50\text{ has 3 significant figures}}
$$

Similarly:

$$
2.500
$$

has four significant figures.

### Rule 5 — Scientific notation makes significant figures clear

Consider:

$$
5.20\times10^{-3}
$$

This has three significant figures.

---

## 6.14 Significant Figures in Semiconductor Measurements

Consider a semiconductor film thickness reported as:

$$
100\text{ nm}
$$

The number of significant figures may be ambiguous when trailing zeros are present without a decimal point or scientific notation.

Compare:

$$
1.00\times10^2\text{ nm}
$$

This clearly has three significant figures.

Similarly:

$$
1.000\times10^2\text{ nm}
$$

has four significant figures.

Scientific notation therefore provides a clear way to communicate precision.

---

## 6.15 Measurement Resolution and Significant Figures

The number of digits displayed by an instrument does not automatically determine its accuracy.

Suppose a digital instrument displays:

$$
5.0037\text{ V}
$$

The display contains several digits, but this does not automatically mean that the actual voltage is known to that precision.

The instrument may have:

- Limited accuracy
- Calibration error
- Noise
- Environmental sensitivity

Therefore:

> **Displayed digits and meaningful significant figures are not necessarily the same thing.**

The reported result should be consistent with the quality and uncertainty of the measurement.

---

## 6.16 Rounding Measurements

Suppose a calculation produces:

$$
2.73486127\text{ V}
$$

If the measurement uncertainty supports only two decimal places, reporting all the digits would give a false impression of precision.

The value may be rounded to:

$$
\boxed{2.73\text{ V}}
$$

The appropriate number of digits depends on the measurement context and reporting convention.

### Basic Rounding Rule

If the next digit is:

- Less than 5 → retain the preceding digit.
- 5 or greater → increase the preceding digit by 1.

For example:

$$
3.146\rightarrow3.15
$$

to two decimal places.

And:

$$
3.142\rightarrow3.14
$$

to two decimal places.

---

## 6.17 Significant Figures in Calculations

When measured values are used in calculations, the final answer should not generally be reported with unjustified precision.

For example:

$$
V=5.0\text{ V}
$$

and:

$$
R=100\Omega
$$

give:

$$
I=\frac{V}{R}
$$

and therefore:

$$
I=\frac{5.0}{100}=0.05\text{ A}
$$

A common introductory rule is:

> **For multiplication and division, the result should generally have no more significant figures than the input value with the fewest significant figures.**

For addition and subtraction, the usual rule is based on decimal places rather than significant figures.

In advanced scientific work, uncertainty propagation provides a more rigorous basis for determining the precision of a final result.

---

## 6.18 Accuracy, Precision and Significant Figures

These ideas should not be confused.

### Accuracy

How close is the result to the accepted value?

### Precision

How consistent are repeated measurements?

### Significant Figures

How much meaningful numerical precision is communicated by the reported value?

An instrument may report:

$$
0.7000\text{ V}
$$

This contains four significant figures.

But if the instrument is poorly calibrated, the measurement may still have poor accuracy.

Similarly, repeated measurements may be very close to one another, giving high precision, while all of them are offset from the true value.

Therefore:

> **Many significant figures do not guarantee high accuracy.**

---

## 6.19 Error vs Uncertainty vs Accuracy vs Precision

These concepts can be summarized as follows.

| Concept | Main Question |
|---|---|
| Error | How different is the measurement from a reference value? |
| Uncertainty | How much uncertainty is associated with the measurement? |
| Accuracy | How close is the measurement to the accepted value? |
| Precision | How close are repeated measurements to one another? |
| Significant figures | How much meaningful numerical precision is reported? |

This distinction is essential for scientific data analysis.

---

## 6.20 Complete Semiconductor Example

Suppose the accepted threshold voltage is:

$$
V_r=0.700\text{ V}
$$

Five measurements are obtained:

$$
0.699,\;0.700,\;0.701,\;0.700,\;0.699\text{ V}
$$

### Accuracy

The measurements are close to the accepted value.

Therefore, the measurements are accurate.

### Precision

The measurements are also close to one another.

Therefore, the measurements are precise.

### Significant Figures

Each measurement is reported to three decimal places.

### Uncertainty

If the measurement is reported as:

$$
V_T=0.700\pm0.002\text{ V}
$$

then:

$$
u=0.002\text{ V}
$$

The measurement is communicated together with an estimate of its uncertainty.

---

## 6.21 Common Mistakes

### Mistake 1: Assuming precision means accuracy

A measurement can be highly precise but inaccurate.

### Mistake 2: Assuming more decimal places mean greater accuracy

An instrument displaying more digits does not automatically have greater accuracy.

### Mistake 3: Treating uncertainty as the same thing as error

Error compares a measurement with a reference value.

Uncertainty describes the limited knowledge associated with the measurement.

### Mistake 4: Counting leading zeros as significant

For example:

$$
0.00452
$$

has three significant figures, not five.

### Mistake 5: Ignoring trailing zeros after a decimal point

For example:

$$
2.50
$$

has three significant figures.

### Mistake 6: Reporting excessive digits

A calculated result should not imply greater precision than the underlying measurements justify.

---

## 6.22 Summary

Experimental measurements are not perfectly exact.

Uncertainty describes the limited knowledge associated with a measurement.

A simple representation is:

$$
\boxed{x=x_m\pm u}
$$

Relative uncertainty is:

$$
\boxed{
u_r=\frac{u}{|x_m|}
}
$$

Percentage uncertainty is:

$$
\boxed{
u_{\%}
=
\frac{u}{|x_m|}
\times100
}
$$

Accuracy describes closeness to an accepted or reference value.

Precision describes consistency among repeated measurements.

The essential distinction is:

$$
\boxed{
\text{Accuracy}=\text{closeness to target}
}
$$

and:

$$
\boxed{
\text{Precision}=\text{consistency among measurements}
}
$$

Significant figures communicate the meaningful precision of a numerical measurement.

The key idea is:

> **A scientifically meaningful measurement should communicate not only a numerical value but also an appropriate level of precision and uncertainty.**

---

## 6.23 Key Formulae

### Measurement with Uncertainty

$$
\boxed{
x=x_m\pm u
}
$$

### Relative Uncertainty

$$
\boxed{
u_r=\frac{u}{|x_m|}
}
$$

### Percentage Uncertainty

$$
\boxed{
u_{\%}
=
\frac{u}{|x_m|}
\times100
}
$$

---

## 6.24 Review Questions

### Conceptual Questions

1. Why is uncertainty associated with experimental measurements?
2. Define measurement uncertainty.
3. What is the difference between error and uncertainty?
4. Define accuracy.
5. Define precision.
6. What is the difference between accuracy and precision?
7. What are significant figures?
8. Why are leading zeros generally not significant?
9. Why can trailing zeros after a decimal point be significant?
10. Why does displaying more digits not necessarily mean greater accuracy?

### Semiconductor Application Questions

11. Explain accuracy and precision using threshold-voltage measurements.
12. Why is uncertainty important when reporting film thickness?
13. How can uncertainty be expressed in a semiconductor measurement?
14. Why might a highly precise instrument still produce inaccurate results?
15. Why should semiconductor measurements not be reported with unjustified decimal places?

---

## 6.25 Practice Problems

### Problem 1 — Uncertainty

A voltage measurement is reported as:

$$
V=5.00\pm0.02\text{ V}
$$

Calculate the percentage uncertainty.

### Problem 2 — Film Thickness

A semiconductor film is measured as:

$$
t=100.0\pm0.5\text{ nm}
$$

Calculate:

1. Absolute uncertainty
2. Relative uncertainty
3. Percentage uncertainty

### Problem 3 — Accuracy and Precision

The accepted threshold voltage is:

$$
V_T=0.70\text{ V}
$$

Two measurement sets are:

**Set A**

$$
0.699,\;0.700,\;0.701,\;0.700,\;0.699
$$

**Set B**

$$
0.750,\;0.751,\;0.750,\;0.749,\;0.750
$$

Which set is more accurate?

Which set is more precise?

Explain your answer.

### Problem 4 — Significant Figures

Determine the number of significant figures in:

1. $0.00452$
2. $4.520$
3. $0.0500$
4. $100.0$
5. $5.20\times10^{-3}$

### Problem 5 — Rounding

Round the following to three significant figures:

1. $2.734$
2. $0.004567$
3. $105.78$
4. $0.9996$

### Problem 6 — Conceptual Interpretation

An instrument displays:

$$
5.00372\text{ V}
$$

Explain why it would be incorrect to conclude automatically that the measurement is accurate to six significant figures.

---

## 6.26 Looking Ahead

We now have the basic language needed to describe experimental measurements:

- Central tendency
- Dispersion
- Error
- Uncertainty
- Accuracy
- Precision
- Significant figures

The next step is to understand how uncertainty behaves when measured quantities are combined mathematically.

For example, if:

$$
R=\frac{V}{I}
$$

and both $V$ and $I$ have uncertainty, how uncertain is the calculated resistance?

This leads to:

$$
\boxed{
\text{Propagation of Errors}
}
$$
