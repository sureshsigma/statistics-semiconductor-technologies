# Chapter 5 — Percentage Error and Error Analysis

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why error analysis is important in semiconductor measurements.
- Distinguish between a measured value and a reference or accepted value.
- Define absolute error.
- Define relative error.
- Calculate percentage error.
- Understand the relationship between absolute, relative, and percentage error.
- Interpret measurement error in semiconductor experiments.
- Distinguish between measurement error and variation.
- Apply error calculations to voltage, current, resistance, and other semiconductor measurements.

---

## 5.1 Why Do We Study Measurement Error?

Measurements are an essential part of semiconductor science and technology.

Engineers and scientists measure quantities such as:

- Voltage
- Current
- Resistance
- Temperature
- Capacitance
- Film thickness
- Threshold voltage
- Leakage current
- Sensor output

However, a measured value may not be exactly equal to the true or accepted value of the quantity.

For example, suppose the accepted value of a reference voltage is:

$$
V_{\text{ref}}=5.00\text{ V}
$$

and an instrument measures:

$$
V_{\text{measured}}=4.92\text{ V}
$$

The measured value differs from the reference value.

We therefore want to quantify:

> **How large is the difference between the measured value and the reference value?**

This is the purpose of error analysis.

---

## 5.2 Measured Value and Reference Value

Before calculating error, we need to distinguish between two values.

### Measured Value

The **measured value** is the value obtained experimentally using an instrument or measurement procedure.

For example:

$$
V_{\text{measured}}=4.92\text{ V}
$$

### Reference or Accepted Value

The **reference value** is a value against which the measurement is compared.

It may be:

- A calibrated reference
- A standard value
- A theoretical value
- A certified value
- A previously established value
- A value specified by a manufacturer

For example:

$$
V_{\text{reference}}=5.00\text{ V}
$$

The difference between these values provides the basis for calculating measurement error.

---

## 5.3 What Is Measurement Error?

In simple terms, measurement error is the difference between a measured value and a reference or accepted value.

Let:

- $x_m$ = measured value
- $x_r$ = reference value

Then the signed error can be written as:

$$
\boxed{
E=x_m-x_r
}
$$

The sign tells us the direction of the difference.

### Positive Error

If:

$$
x_m>x_r
$$

then:

$$
E>0
$$

The measured value is higher than the reference value.

### Negative Error

If:

$$
x_m<x_r
$$

then:

$$
E<0
$$

The measured value is lower than the reference value.

For many introductory calculations, we are interested in the **magnitude** of the error rather than its direction.

This leads to absolute error.

---

## 5.4 Absolute Error

The **absolute error** is the magnitude of the difference between the measured value and the reference value.

It is given by:

$$
\boxed{
E_{\text{absolute}}
=
\left|x_m-x_r\right|
}
$$

The absolute value symbol ensures that the result is non-negative.

### Example

Suppose the reference voltage is:

$$
V_r=5.00\text{ V}
$$

and the measured voltage is:

$$
V_m=4.92\text{ V}
$$

The absolute error is:

$$
E_{\text{absolute}}
=
|4.92-5.00|
$$

Therefore:

$$
\boxed{
E_{\text{absolute}}=0.08\text{ V}
}
$$

or:

$$
\boxed{
E_{\text{absolute}}=80\text{ mV}
}
$$

### Interpretation

The measurement differs from the reference value by $0.08$ V.

The absolute error has the **same units as the measured quantity**.

---

## 5.5 Semiconductor Example — Voltage Measurement

Suppose a calibrated semiconductor testing system provides a reference voltage of:

$$
V_r=2.500\text{ V}
$$

A laboratory multimeter measures:

$$
V_m=2.475\text{ V}
$$

The absolute error is:

$$
E_{\text{absolute}}
=
|2.475-2.500|
$$

Therefore:

$$
\boxed{
E_{\text{absolute}}=0.025\text{ V}
}
$$

or:

$$
\boxed{
E_{\text{absolute}}=25\text{ mV}
}
$$

The measurement is lower than the reference value, so the **signed error** is:

$$
E=2.475-2.500=-0.025\text{ V}
$$

while the **absolute error** is:

$$
|E|=0.025\text{ V}
$$

This distinction is useful:

- Signed error tells us the direction of the difference.
- Absolute error tells us the magnitude of the difference.

---

## 5.6 Relative Error

Absolute error tells us the difference in the original units.

However, an error of $0.1$ V can have very different meanings depending on the size of the reference value.

For example:

- $0.1$ V error for a $1$ V measurement is relatively large.
- $0.1$ V error for a $100$ V measurement is relatively small.

To account for the scale of the measurement, we use **relative error**.

Relative error is defined as:

$$
\boxed{
E_{\text{relative}}
=
\frac{|x_m-x_r|}{|x_r|}
}
$$

The relative error is dimensionless because the units in the numerator and denominator cancel.

---

## 5.7 Semiconductor Example — Relative Error

Suppose:

$$
V_r=5.00\text{ V}
$$

and:

$$
V_m=4.92\text{ V}
$$

The absolute error is:

$$
|4.92-5.00|=0.08\text{ V}
$$

Therefore, the relative error is:

$$
E_{\text{relative}}
=
\frac{0.08}{5.00}
$$

Hence:

$$
\boxed{
E_{\text{relative}}=0.016
}
$$

The relative error has no units.

---

## 5.8 Percentage Error

Relative error is often converted into a percentage because percentages are easier to interpret.

The percentage error is:

$$
\boxed{
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}
\times100
}
$$

Therefore:

$$
E_{\%}
=
E_{\text{relative}}\times100
$$

Using the previous example:

$$
E_{\%}
=
\frac{0.08}{5.00}\times100
$$

Therefore:

$$
\boxed{
E_{\%}=1.6\%
}
$$

### Interpretation

The measured voltage differs from the reference voltage by:

$$
1.6\%
$$

in magnitude.

---

## 5.9 Relationship Between Absolute, Relative and Percentage Error

The three quantities are related.

### Absolute Error

$$
\boxed{
E_{\text{absolute}}
=
|x_m-x_r|
}
$$

### Relative Error

$$
\boxed{
E_{\text{relative}}
=
\frac{|x_m-x_r|}{|x_r|}
}
$$

### Percentage Error

$$
\boxed{
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}\times100
}
$$

Therefore:

$$
\boxed{
E_{\%}=E_{\text{relative}}\times100
}
$$

The sequence can be remembered as:

$$
\text{Absolute Error}
\rightarrow
\text{Relative Error}
\rightarrow
\text{Percentage Error}
$$

---

## 5.10 Worked Example — Semiconductor Current Measurement

A reference current is:

$$
I_r=10.00\text{ mA}
$$

An instrument measures:

$$
I_m=9.80\text{ mA}
$$

### Step 1: Absolute Error

$$
E_{\text{absolute}}
=
|9.80-10.00|
$$

$$
\boxed{
E_{\text{absolute}}=0.20\text{ mA}
}
$$

### Step 2: Relative Error

$$
E_{\text{relative}}
=
\frac{0.20}{10.00}
$$

Therefore:

$$
\boxed{
E_{\text{relative}}=0.02
}
$$

### Step 3: Percentage Error

$$
E_{\%}
=
0.02\times100
$$

Therefore:

$$
\boxed{
E_{\%}=2\%
}
$$

### Interpretation

The current measurement differs from the reference value by:

$$
0.20\text{ mA}
$$

which corresponds to a percentage error of:

$$
2\%
$$

---

## 5.11 Worked Example — Resistance Measurement

Suppose the reference resistance of a semiconductor component is:

$$
R_r=1000\Omega
$$

The measured resistance is:

$$
R_m=985\Omega
$$

### Absolute Error

$$
E_{\text{absolute}}
=
|985-1000|
=
15\Omega
$$

Therefore:

$$
\boxed{
E_{\text{absolute}}=15\Omega
}
$$

### Relative Error

$$
E_{\text{relative}}
=
\frac{15}{1000}
=
0.015
$$

### Percentage Error

$$
E_{\%}
=
0.015\times100
$$

Therefore:

$$
\boxed{
E_{\%}=1.5\%
}
$$

---

## 5.12 Why Percentage Error Is Useful

Percentage error allows measurements of different scales to be compared more meaningfully.

Consider two measurements.

### Measurement A

Reference:

$$
1\text{ V}
$$

Absolute error:

$$
0.05\text{ V}
$$

Percentage error:

$$
\frac{0.05}{1}\times100=5\%
$$

### Measurement B

Reference:

$$
100\text{ V}
$$

Absolute error:

$$
0.5\text{ V}
$$

Percentage error:

$$
\frac{0.5}{100}\times100=0.5\%
$$

Measurement B has a larger absolute error:

$$
0.5\text{ V}>0.05\text{ V}
$$

but a smaller percentage error:

$$
0.5\%<5\%
$$

Therefore, absolute error alone can sometimes be misleading when comparing measurements of different magnitudes.

---

## 5.13 Error in Semiconductor Device Parameters

Error analysis is not limited to voltage and current.

It can be applied to many semiconductor parameters.

Examples include:

### Threshold Voltage

$$
V_T
$$

### Leakage Current

$$
I_{\text{leak}}
$$

### Film Thickness

$$
t
$$

### Carrier Mobility

$$
\mu
$$

### Resistance

$$
R
$$

### Capacitance

$$
C
$$

For any measured quantity $x$, the basic percentage-error formula is:

$$
\boxed{
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}
\times100
}
$$

The meaning of the result depends on the physical quantity and the reference value.

---

## 5.14 Example — Film Thickness Measurement

Suppose the target or reference film thickness is:

$$
t_r=100\text{ nm}
$$

A measurement gives:

$$
t_m=98.5\text{ nm}
$$

The absolute error is:

$$
E_{\text{absolute}}
=
|98.5-100|
=
1.5\text{ nm}
$$

The relative error is:

$$
E_{\text{relative}}
=
\frac{1.5}{100}
=
0.015
$$

Therefore:

$$
E_{\%}
=
0.015\times100
$$

\[
\boxed{
E_{\%}=1.5\%
}
\]

The measured film thickness is therefore $1.5\%$ lower than the reference value in magnitude.

---

## 5.15 Error in Calibration

Calibration involves comparing an instrument's measurement with a known reference.

For example, suppose a voltage measurement instrument is tested at several reference values.

| Reference Voltage (V) | Measured Voltage (V) |
|---:|---:|
| 1.00 | 1.02 |
| 2.00 | 2.03 |
| 3.00 | 2.96 |
| 4.00 | 3.98 |
| 5.00 | 4.94 |

For each measurement, absolute and percentage errors can be calculated.

This allows the engineer to determine:

- Whether the instrument is systematically high or low
- How large the error is
- Whether the instrument meets its accuracy specification
- Whether calibration or adjustment is required

Thus, error analysis is an important part of measurement system evaluation.

---

## 5.16 Signed Error vs Absolute Error

It is useful to distinguish between the direction and magnitude of an error.

Suppose:

$$
x_r=10.00
$$

and:

$$
x_m=9.80
$$

The signed error is:

$$
E=x_m-x_r
$$

Therefore:

$$
E=9.80-10.00=-0.20
$$

The negative sign indicates that the measured value is **below** the reference value.

The absolute error is:

$$
|E|=0.20
$$

Therefore:

- Signed error: $-0.20$
- Absolute error: $0.20$

The signed value is useful when direction matters, while absolute error is useful when we are interested only in the magnitude of the difference.

---

## 5.17 Error Does Not Automatically Mean Mistake

The word "error" can sometimes be misunderstood.

In measurement science, error does not necessarily mean that the experimenter made a mistake.

A measurement may differ from a reference value because of:

- Instrument limitations
- Calibration effects
- Environmental conditions
- Resolution limitations
- Electrical noise
- Experimental conditions
- Imperfect measurement procedures

Therefore:

> **Measurement error is a quantitative difference between a measured value and a reference value; it does not automatically mean that someone made a mistake.**

This distinction is important in scientific and engineering measurements.

---

## 5.18 Error vs Variation

Error and variation are related but different concepts.

### Variation

Variation describes differences **among observations**.

For example:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

The values vary from device to device.

### Error

Error describes the difference between a measured value and a reference value.

For example:

Reference:

$$
0.70\text{ V}
$$

Measured:

$$
0.72\text{ V}
$$

Absolute error:

$$
|0.72-0.70|=0.02\text{ V}
$$

Therefore:

> **Variation compares observations with each other; error compares a measurement with a reference value.**

This distinction is fundamental.

---

## 5.19 Common Mistakes

### Mistake 1: Using the measured value in the denominator

Percentage error is normally calculated relative to the reference value:

$$
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}
\times100
$$

### Mistake 2: Forgetting the absolute value

If the question asks for the magnitude of error, use:

$$
|x_m-x_r|
$$

### Mistake 3: Confusing relative error and percentage error

Relative error is a ratio:

$$
E_{\text{relative}}
=
\frac{|x_m-x_r|}{|x_r|}
$$

Percentage error is:

$$
E_{\%}
=
E_{\text{relative}}\times100
$$

### Mistake 4: Confusing error with variation

Error compares a measurement with a reference.

Variation describes differences among observations.

### Mistake 5: Assuming a non-zero error means the instrument is unusable

Whether an error is acceptable depends on:

- The application
- Required accuracy
- Specification limits
- Measurement uncertainty
- Purpose of the experiment

---

## 5.20 Summary

Measurement error describes the difference between a measured value and a reference or accepted value.

The signed error is:

$$
\boxed{
E=x_m-x_r
}
$$

The absolute error is:

$$
\boxed{
E_{\text{absolute}}
=
|x_m-x_r|
}
$$

The relative error is:

$$
\boxed{
E_{\text{relative}}
=
\frac{|x_m-x_r|}{|x_r|}
}
$$

The percentage error is:

$$
\boxed{
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}
\times100
}
$$

These measures are useful in semiconductor applications such as:

- Voltage measurement
- Current measurement
- Resistance measurement
- Film-thickness measurement
- Instrument calibration
- Device characterization

A key distinction is:

> **Variation describes differences among measurements, whereas error describes the difference between a measurement and a reference value.**

---

## 5.21 Key Formulae

### Signed Error

$$
\boxed{
E=x_m-x_r
}
$$

### Absolute Error

$$
\boxed{
E_{\text{absolute}}
=
|x_m-x_r|
}
$$

### Relative Error

$$
\boxed{
E_{\text{relative}}
=
\frac{|x_m-x_r|}{|x_r|}
}
$$

### Percentage Error

$$
\boxed{
E_{\%}
=
\frac{|x_m-x_r|}{|x_r|}
\times100
}
$$

---

## 5.22 Review Questions

### Conceptual Questions

1. What is measurement error?
2. What is the difference between measured value and reference value?
3. Define absolute error.
4. Define relative error.
5. Define percentage error.
6. Why is the reference value used in the denominator of percentage error?
7. What is the difference between signed error and absolute error?
8. Does measurement error necessarily mean that an experimenter made a mistake?
9. What is the difference between error and variation?
10. Why is percentage error useful when comparing measurements of different magnitudes?

### Semiconductor Application Questions

11. Why is error analysis important when calibrating semiconductor measurement instruments?
12. A measured threshold voltage differs slightly from a reference threshold voltage. How can the error be quantified?
13. Why might absolute error be insufficient when comparing measurements of different scales?
14. Give two examples of semiconductor measurements for which percentage error could be calculated.
15. Explain how error analysis can help determine whether an instrument meets its specification.

---

## 5.23 Practice Problems

### Problem 1 — Voltage Measurement

A reference voltage is:

$$
V_r=5.00\text{ V}
$$

A multimeter measures:

$$
V_m=4.92\text{ V}
$$

Calculate:

1. Signed error
2. Absolute error
3. Relative error
4. Percentage error

### Problem 2 — Current Measurement

The reference current is:

$$
I_r=10.00\text{ mA}
$$

The measured current is:

$$
I_m=9.80\text{ mA}
$$

Calculate the absolute, relative and percentage errors.

### Problem 3 — Resistance Measurement

A semiconductor component has a reference resistance of:

$$
R_r=1000\Omega
$$

The measured resistance is:

$$
R_m=985\Omega
$$

Calculate the percentage error.

### Problem 4 — Film Thickness

The target film thickness is:

$$
100\text{ nm}
$$

The measured thickness is:

$$
98.5\text{ nm}
$$

Calculate:

1. Absolute error
2. Relative error
3. Percentage error

### Problem 5 — Compare Two Measurements

Measurement A has:

$$
x_r=1\text{ V},\qquad x_m=0.95\text{ V}
$$

Measurement B has:

$$
x_r=100\text{ V},\qquad x_m=99.5\text{ V}
$$

Calculate the absolute and percentage error for each measurement.

Which measurement has the larger absolute error?

Which has the larger percentage error?

### Problem 6 — Error vs Variation

Five measurements of a semiconductor parameter are:

$$
0.68,\;0.69,\;0.70,\;0.71,\;0.72\text{ V}
$$

The accepted value is:

$$
0.70\text{ V}
$$

Explain the difference between:

1. Variation among the five measurements
2. Error of an individual measurement relative to the accepted value

---

## 5.24 Looking Ahead

In this chapter, we learned how to quantify the difference between a measured value and a reference value.

We introduced:

- Signed error
- Absolute error
- Relative error
- Percentage error

However, experimental measurements are often reported with statements such as:

$$
5.00\pm0.02\text{ V}
$$

What does the $\pm0.02$ V represent?

Is it an error?

Is it uncertainty?

How is uncertainty different from accuracy and precision?

These questions lead to the next chapter:

$$
\boxed{
\text{Uncertainty, Accuracy and Precision}
}
$$