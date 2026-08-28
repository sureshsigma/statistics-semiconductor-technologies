# Chapter 8 — Linear Curve Fitting: Slope and Intercept

## Learning Objectives

After completing this chapter, students will be able to:

- Explain why experimental data are fitted with mathematical curves.
- Understand the idea of a linear model.
- Write the equation of a straight line.
- Interpret slope and intercept.
- Calculate slope from experimental observations.
- Apply linear fitting to semiconductor measurements.
- Estimate resistance from an I–V characteristic.
- Understand the difference between measured points and a fitted line.
- Interpret fitted parameters physically.
- Understand the basic idea of residuals.

---

## 8.1 Why Do We Fit Experimental Data?

In a semiconductor experiment, we often collect several measurements.

For example, we may measure voltage and current:

| Current $I$ (mA) | Voltage $V$ (V) |
|---:|---:|
| 1.0 | 0.98 |
| 2.0 | 2.01 |
| 3.0 | 3.02 |
| 4.0 | 4.05 |
| 5.0 | 4.98 |

If we plot these observations, the points may approximately follow a straight line.

However, experimental measurements are rarely perfectly aligned.

There may be:

- Instrument noise
- Measurement error
- Device variation
- Environmental effects
- Rounding
- Experimental limitations

Instead of simply connecting every point, we can find a mathematical equation that represents the overall trend.

This process is called **curve fitting**.

> **Curve fitting is the process of finding a mathematical relationship that represents the pattern observed in experimental data.**

---

## 8.2 From Data Points to a Mathematical Model

Suppose we have measurements of two variables:

$$
(x_1,y_1),(x_2,y_2),\ldots,(x_n,y_n)
$$

A scatter plot allows us to see the relationship visually.

If the points approximately follow a straight-line pattern, we can use a **linear model**.

The general equation is:

$$
\boxed{
y=a+bx
}
$$

where:

- $y$ = dependent variable
- $x$ = independent variable
- $a$ = intercept
- $b$ = slope

This equation is one of the most important equations in experimental data analysis.

---

## 8.3 Understanding the Straight-Line Equation

Consider:

$$
y=a+bx
$$

The equation contains two important parameters:

### Intercept

$$
\boxed{a}
$$

### Slope

$$
\boxed{b}
$$

The intercept tells us the predicted value of $y$ when:

$$
x=0
$$

because:

$$
y=a+b(0)
$$

Therefore:

$$
\boxed{y=a}
$$

The slope tells us how much $y$ changes when $x$ changes.

---

## 8.4 What Is Slope?

Slope represents the change in the dependent variable for a given change in the independent variable.

For two points:

$$
(x_1,y_1)
$$

and:

$$
(x_2,y_2)
$$

the slope is:

$$
\boxed{
b=
\frac{y_2-y_1}{x_2-x_1}
}
$$

or:

$$
\boxed{
b=
\frac{\Delta y}{\Delta x}
}
$$

This is often described as:

> **Rise divided by run.**

---

## 8.5 Simple Example of Slope

Suppose:

$$
x_1=2
$$

and:

$$
y_1=5
$$

and another point is:

$$
x_2=6
$$

and:

$$
y_2=13
$$

Then:

$$
b=
\frac{13-5}{6-2}
$$

Therefore:

$$
b=\frac{8}{4}
$$

and:

$$
\boxed{b=2}
$$

This means that, according to the straight-line relationship, $y$ increases by approximately 2 units for every 1-unit increase in $x$.

---

## 8.6 Intercept

The intercept is the value of $y$ when:

$$
x=0
$$

Consider:

$$
y=3+2x
$$

Here:

$$
a=3
$$

and:

$$
b=2
$$

Therefore, when:

$$
x=0
$$

we get:

$$
y=3
$$

Hence:

$$
\boxed{a=3}
$$

is the y-intercept.

---

## 8.7 Semiconductor Example — Ohm's Law

One of the most useful applications of linear fitting in semiconductor science is the analysis of an approximately **ohmic** region of an I–V characteristic.

Ohm's law is:

$$
\boxed{
V=IR
}
$$

Suppose we plot:

- Current $I$ on the x-axis
- Voltage $V$ on the y-axis

Then:

$$
V=RI
$$

Compare this with:

$$
y=a+bx
$$

We can identify:

$$
y=V
$$

$$
x=I
$$

$$
a=0
$$

and:

$$
\boxed{b=R}
$$

Therefore:

> **When voltage is plotted against current in an ohmic region, the slope of the fitted line represents resistance.**

---

## 8.8 Experimental I–V Data

Suppose an experimental measurement gives:

| Current $I$ (mA) | Voltage $V$ (V) |
|---:|---:|
| 1 | 0.50 |
| 2 | 1.01 |
| 3 | 1.49 |
| 4 | 2.02 |
| 5 | 2.51 |

The points are approximately linear.

We can estimate the slope using two representative points.

Take:

$$
(I_1,V_1)=(1,0.50)
$$

and:

$$
(I_2,V_2)=(5,2.51)
$$

The slope is:

$$
b=
\frac{2.51-0.50}{5-1}
$$

Therefore:

$$
b=\frac{2.01}{4}
$$

$$
\boxed{
b=0.5025\text{ V/mA}
}
$$

Since:

$$
1\text{ V/mA}=1\text{ k}\Omega
$$

we obtain:

$$
\boxed{
R\approx0.503\text{ k}\Omega
}
$$

or approximately:

$$
\boxed{
R\approx503\Omega
}
$$

Thus, the slope gives us a physical device parameter.

---

## 8.9 Why Fit a Line Instead of Joining the Points?

Experimental observations do not usually lie exactly on a single straight line.

If we simply join the points, we obtain a series of line segments.

That does not necessarily provide a useful overall model.

A fitted line instead attempts to represent the **overall trend**.

The purpose is not to force every point onto the line.

Instead:

> **The fitted line summarizes the underlying relationship while allowing for experimental variation.**

---

## 8.10 Slope as a Physical Parameter

One of the most important ideas in experimental science is that the parameters of a fitted equation often have physical meaning.

For:

$$
V=RI
$$

the slope is:

$$
R
$$

Therefore:

$$
\boxed{
\text{slope}=R
}
$$

This allows us to estimate resistance from experimental measurements.

Similarly, depending on the experiment, a slope may represent:

- Sensor sensitivity
- Temperature coefficient
- Gain
- Calibration factor
- Rate of change of a physical quantity

Therefore:

> **Curve fitting is not only about drawing a line. It allows us to estimate meaningful physical parameters from experimental data.**

---

## 8.11 Sensor Calibration Example

Suppose a semiconductor sensor produces an output voltage depending on temperature.

Experimental data:

| Temperature $T$ (°C) | Output $V$ (V) |
|---:|---:|
| 20 | 1.02 |
| 30 | 1.21 |
| 40 | 1.39 |
| 50 | 1.61 |
| 60 | 1.80 |

Suppose the relationship is approximately linear:

$$
V=a+bT
$$

Here:

- $V$ = sensor output
- $T$ = temperature
- $a$ = intercept
- $b$ = sensitivity

The slope has units:

$$
\frac{\text{V}}{^\circ\text{C}}
$$

If the fitted slope is approximately:

$$
b=0.020\text{ V}/^\circ\text{C}
$$

then the sensor output changes by approximately $0.020$ V for every $1^\circ$C increase in temperature.

Thus:

$$
\boxed{
\text{slope}=\text{sensor sensitivity}
}
$$

---

## 8.12 Positive and Negative Slopes

The slope also tells us the direction of the relationship.

### Positive Slope

If:

$$
b>0
$$

then $y$ tends to increase as $x$ increases.

For example:

$$
V=0.5+0.02T
$$

has:

$$
b=0.02
$$

Therefore, voltage increases with temperature.

### Negative Slope

If:

$$
b<0
$$

then $y$ tends to decrease as $x$ increases.

For example:

$$
\mu=1800-2T
$$

has:

$$
b=-2
$$

Therefore, mobility decreases as temperature increases in this simplified model.

---

## 8.13 Units of Slope

The slope always has units:

$$
\boxed{
\frac{\text{units of }y}{\text{units of }x}
}
$$

For example, if:

$$
y=V
$$

and:

$$
x=I
$$

then:

$$
\text{Slope}
=
\frac{\text{V}}{\text{A}}
$$

Therefore:

$$
\boxed{
\text{Slope}=\Omega
}
$$

For a temperature sensor:

$$
y=V
$$

and:

$$
x=T
$$

so:

$$
\boxed{
\text{Slope}=\text{V}/^\circ\text{C}
}
$$

Always check the units of the slope.

They often provide important information about its physical meaning.

---

## 8.14 Calculating the Intercept

Suppose we know the slope and one experimental point.

From:

$$
y=a+bx
$$

we can rearrange:

$$
\boxed{
a=y-bx
}
$$

### Example

Suppose:

$$
b=2
$$

and one point is:

$$
(x,y)=(3,8)
$$

Then:

$$
a=8-(2)(3)
$$

Therefore:

$$
a=2
$$

The fitted equation is:

$$
\boxed{
y=2+2x
}
$$

---

## 8.15 Semiconductor Example — Contact Resistance

Suppose an experimental I–V relationship is approximately:

$$
V=V_0+RI
$$

where:

- $R$ = resistance
- $V_0$ = voltage offset

This has the form:

$$
y=a+bx
$$

Therefore:

$$
a=V_0
$$

and:

$$
b=R
$$

If experimental fitting gives:

$$
V=0.03+500I
$$

then:

$$
\boxed{
R=500\Omega
}
$$

and:

$$
\boxed{
V_0=0.03\text{ V}
}
$$

The intercept may indicate an offset or another experimental effect.

Its physical interpretation must always be based on the actual experimental setup.

---

## 8.16 Measured Points and Fitted Values

Suppose the fitted equation is:

$$
y=a+bx
$$

For each observed value $x_i$, the fitted model gives a predicted value:

$$
\boxed{
\hat{y}_i=a+bx_i
}
$$

The symbol $\hat{y}$ is read as "y-hat."

It represents the value predicted by the fitted line.

The actual measured value is:

$$
y_i
$$

The difference between them is called the **residual**.

---

## 8.17 Residuals

A residual is:

$$
\boxed{
e_i=y_i-\hat{y}_i
}
$$

where:

- $y_i$ = measured value
- $\hat{y}_i$ = fitted value
- $e_i$ = residual

### Example

Suppose the measured voltage is:

$$
V_i=1.02\text{ V}
$$

and the fitted line predicts:

$$
\hat{V}_i=1.00\text{ V}
$$

Then:

$$
e_i=1.02-1.00
$$

Therefore:

$$
\boxed{
e_i=0.02\text{ V}
}
$$

A residual can be positive or negative.

---

## 8.18 Why Are Residuals Useful?

Residuals tell us how far individual observations are from the fitted model.

If residuals are generally small, the line may describe the data reasonably well.

If residuals are large or show a systematic pattern, the linear model may not be appropriate.

For example, if residuals show a curved pattern, the underlying relationship may be nonlinear.

Therefore:

> **Residuals help us evaluate whether a fitted line is an appropriate representation of the data.**

---

## 8.19 Linear Fit Does Not Mean Every Point Must Lie on the Line

Experimental data naturally contain variation.

Suppose:

$$
V=0.5I
$$

is the approximate relationship.

Actual measurements may be:

$$
0.49,\;1.01,\;1.48,\;2.03,\;2.51
$$

rather than:

$$
0.50,\;1.00,\;1.50,\;2.00,\;2.50
$$

The fitted line attempts to represent the overall pattern.

Therefore:

> **A good fitted line does not necessarily pass through every experimental point.**

---

## 8.20 Linear Fit and Correlation

Chapter 8 introduced correlation.

Correlation answers:

> **How strongly are two variables linearly associated?**

Linear fitting answers:

> **What equation can represent that linear relationship?**

For example:

$$
r\approx0.98
$$

may indicate a strong positive linear association.

A fitted model might be:

$$
y=0.20+1.50x
$$

The two techniques therefore provide different information.

### Correlation

Describes strength and direction.

### Linear fitting

Provides an equation and estimates parameters such as slope and intercept.

---

## 8.21 A Complete Semiconductor Example

Suppose we measure an approximately ohmic device:

| $I$ (mA) | $V$ (V) |
|---:|---:|
| 1 | 0.48 |
| 2 | 1.01 |
| 3 | 1.49 |
| 4 | 2.02 |
| 5 | 2.51 |

We want to model:

$$
V=a+bI
$$

If the fitted line gives:

$$
\boxed{
V=0.01+0.50I
}
$$

then the slope is:

$$
b=0.50\text{ V/mA}
$$

Since:

$$
1\text{ V/mA}=1\text{ k}\Omega
$$

we obtain:

$$
\boxed{
R=0.50\text{ k}\Omega
}
$$

or:

$$
\boxed{
R=500\Omega
}
$$

The intercept is:

$$
\boxed{
a=0.01\text{ V}
}
$$

This may represent a small experimental offset.

The fitted equation therefore converts a set of experimental measurements into a simple mathematical model with physically interpretable parameters.

---

## 8.22 Why Curve Fitting Is Useful in Semiconductor Technology

Curve fitting is useful because semiconductor experiments generate large amounts of measurement data.

Examples include:

### I–V Characterization

$$
V\text{ vs }I
$$

Used to estimate resistance in suitable linear regions.

### Sensor Calibration

$$
\text{Output}\text{ vs }\text{Input}
$$

Used to estimate sensitivity.

### Temperature Measurements

$$
\text{Parameter}\text{ vs }T
$$

Used to study temperature dependence.

### Process Monitoring

$$
\text{Process Variable}\text{ vs }\text{Device Parameter}
$$

Used to identify trends.

### Material Characterization

$$
\text{Measured Property}\text{ vs }\text{Experimental Condition}
$$

Used to estimate parameters and compare samples.

Thus:

> **Curve fitting converts experimental observations into a mathematical model that can be interpreted and used for prediction.**

---

## 8.23 Common Mistakes

### Mistake 1: Confusing slope and intercept

In:

$$
y=a+bx
$$

the intercept is:

$$
a
$$

and the slope is:

$$
b
$$

### Mistake 2: Forgetting the units of slope

Slope always has:

$$
\frac{\text{units of }y}{\text{units of }x}
$$

### Mistake 3: Assuming every relationship is linear

A scatter plot should be examined before choosing a linear model.

### Mistake 4: Joining experimental points instead of fitting a model

Joining points describes the sequence of observations but does not necessarily provide an overall model.

### Mistake 5: Assuming the intercept must always be zero

Some physical relationships pass through the origin, but experimental offsets can produce a non-zero intercept.

### Mistake 6: Assuming a high correlation proves the model is physically correct

A strong correlation does not automatically establish a physical law.

---

## 8.24 Summary

A linear model has the form:

$$
\boxed{
y=a+bx
}
$$

where:

- $a$ = intercept
- $b$ = slope

The slope is:

$$
\boxed{
b=\frac{\Delta y}{\Delta x}
}
$$

The intercept is:

$$
\boxed{
a=y-bx
}
$$

The fitted value is:

$$
\boxed{
\hat{y}=a+bx
}
$$

The residual is:

$$
\boxed{
e=y-\hat{y}
}
$$

In semiconductor applications, the slope of a fitted line can have direct physical meaning.

For example:

$$
V=RI
$$

gives:

$$
\boxed{
R=\text{slope of the }V\text{-}I\text{ plot}
}
$$

The central idea is:

> **Linear fitting allows us to convert experimental data into a mathematical relationship whose parameters can often be interpreted physically.**

---

## 8.25 Key Formulae

### Linear Model

$$
\boxed{
y=a+bx
}
$$

### Slope

$$
\boxed{
b=\frac{y_2-y_1}{x_2-x_1}
}
$$

### Intercept

$$
\boxed{
a=y-bx
}
$$

### Fitted Value

$$
\boxed{
\hat{y}=a+bx
}
$$

### Residual

$$
\boxed{
e=y-\hat{y}
}
$$

---

## 8.26 Review Questions

1. What is curve fitting?
2. Why is curve fitting useful for experimental data?
3. What is a linear model?
4. Write the equation of a straight line.
5. What is the meaning of slope?
6. What is the meaning of intercept?
7. What are the units of slope?
8. What is a residual?
9. Why do experimental points not necessarily lie exactly on the fitted line?
10. What is the difference between correlation and linear fitting?

### Semiconductor Application Questions

11. Why is linear fitting useful for an approximately ohmic I–V characteristic?
12. What does the slope represent when voltage is plotted against current?
13. How can linear fitting be used for sensor calibration?
14. What might a non-zero intercept indicate in an experimental I–V measurement?
15. Why should the physical meaning of a fitted parameter always be considered in context?

---

## 9.27 Practice Problems

### Problem 1 — Basic Slope

Two experimental points are:

$$
(x_1,y_1)=(2,5)
$$

and:

$$
(x_2,y_2)=(6,13)
$$

Calculate the slope.

### Problem 2 — Semiconductor I–V

An approximately ohmic device gives:

| $I$ (mA) | $V$ (V) |
|---:|---:|
| 1 | 0.50 |
| 2 | 1.00 |
| 3 | 1.51 |
| 4 | 2.00 |
| 5 | 2.49 |

Estimate the resistance using two representative points.

### Problem 3 — Sensor Calibration

A sensor produces the following output:

| Temperature (°C) | Output (V) |
|---:|---:|
| 20 | 1.02 |
| 30 | 1.21 |
| 40 | 1.39 |
| 50 | 1.61 |
| 60 | 1.80 |

Estimate the slope using the first and last observations.

Interpret the slope physically.

### Problem 4 — Equation of a Line

A fitted semiconductor relationship has:

$$
b=0.5
$$

and passes through:

$$
(x,y)=(4,2.1)
$$

Calculate the intercept and write the fitted equation.

### Problem 5 — Residual

A fitted equation is:

$$
\hat{y}=1+2x
$$

For:

$$
x=3
$$

the measured value is:

$$
y=7.2
$$

Calculate the fitted value and residual.

### Problem 6 — Interpretation

A fitted I–V equation is:

$$
V=0.02+0.48I
$$

where $V$ is in volts and $I$ is in mA.

Determine:

1. Slope
2. Intercept
3. Resistance represented by the slope
4. Physical interpretation of the intercept

---

## 9.28 Looking Ahead

Linear fitting provides an equation for the relationship between two variables.

However, calculating a line from just two points is not sufficient when we have many experimental observations.

For a complete dataset, we need a systematic method for finding the **best-fitting line**.

Before moving to full regression, the next chapter will introduce another important type of relationship found frequently in semiconductor science:

$$
\boxed{
\text{Exponential Curve Fitting}
}
$$

Examples include:

- Diode current–voltage characteristics
- Thermally activated processes
- Leakage current and temperature
- Arrhenius-type relationships
