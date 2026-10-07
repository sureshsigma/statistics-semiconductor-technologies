# Chapter 12 — Regression Analysis

## Learning Objectives

After completing this chapter, students will be able to:

- Explain the purpose of regression analysis.
- Distinguish regression from simple curve fitting.
- Identify independent and dependent variables.
- Construct and interpret a simple linear regression model.
- Interpret regression slope and intercept.
- Calculate fitted or predicted values.
- Calculate and interpret residuals.
- Understand the least-squares principle.
- Calculate the regression slope and intercept for a small dataset.
- Understand SSE, MSE, RMSE and $R^2$.
- Apply regression to semiconductor experimental data.
- Estimate physical parameters such as resistance and sensor sensitivity.
- Interpret residuals and identify possible problems with a fitted model.
- Understand interpolation and extrapolation.
- Recognize important limitations of regression analysis.

---

## 12.1 Why Do We Need Regression Analysis?

In real semiconductor experiments, we usually collect many observations. Experimental points rarely lie exactly on a straight line because of measurement noise, instrument limitations, device variation, temperature variation and other experimental effects.

We therefore need a systematic method to find the line that best represents the overall relationship.

This method is called **regression analysis**.

> **Regression analysis is a statistical method used to describe and quantify the relationship between variables and, when appropriate, make predictions.**

---

## 12.2 From Experimental Data to a Model

Suppose we have paired observations:

$$
(x_1,y_1),(x_2,y_2),\ldots,(x_n,y_n)
$$

If a scatter plot shows an approximately linear pattern, we can consider a linear regression model:

$$
\boxed{\hat y=b_0+b_1x}
$$

where:

- $\hat y$ = predicted value of $y$
- $x$ = independent variable
- $b_0$ = regression intercept
- $b_1$ = regression slope

---

## 12.3 Independent and Dependent Variables

The **independent variable** is the variable used to explain or predict changes in another variable.

The **dependent variable** is the variable being predicted or explained.

### Semiconductor Example

If current is used to predict voltage:

$$
I \rightarrow V
$$

then:

- Independent variable: $I$
- Dependent variable: $V$

The regression model becomes:

$$
\boxed{
\hat V=b_0+b_1I
}
$$

The direction matters. Regression of $V$ on $I$ is not the same as regression of $I$ on $V$.

---

## 12.4 Regression vs Simply Drawing a Line

Many different lines can be drawn near a set of experimental points.

Regression provides a mathematical rule for selecting the line that best represents the data.

For ordinary linear regression, the criterion is based on minimizing the sum of squared residuals.

> **Regression gives us a systematic method for determining the best-fitting relationship from many observations.**

---

## 12.5 Simple Linear Regression Model

The simple linear regression model is:

$$
\boxed{
\hat y=b_0+b_1x
}
$$

### Regression Intercept

$b_0$ represents the predicted value of $y$ when:

$$
x=0
$$

### Regression Slope

$b_1$ represents the predicted change in $y$ for a one-unit increase in $x$.

---

## 12.6 Semiconductor Example — I–V Regression

Suppose:

| Current $I$ (mA) | Voltage $V$ (V) |
|---:|---:|
| 1 | 0.49 |
| 2 | 1.02 |
| 3 | 1.48 |
| 4 | 2.03 |
| 5 | 2.51 |

We want to estimate:

$$
\hat V=b_0+b_1I
$$

Here $I$ is the independent variable and $V$ is the dependent variable.

In an approximately ohmic region, the regression slope has the physical meaning of resistance.

---

## 12.7 Regression Slope

For simple linear regression:

$$
\boxed{
b_1=
rac{
\sum_{i=1}^{n}(x_i-ar{x})(y_i-ar{y})
}{
\sum_{i=1}^{n}(x_i-ar{x})^2
}
}
$$

where:

- $x_i$ = observation of $x$
- $y_i$ = observation of $y$
- $\bar{x}$ = mean of $x$
- $\bar{y}$ = mean of $y$
- $n$ = number of observations

The numerator measures how the two variables vary together, while the denominator measures the variation in $x$.

---

## 12.8 Regression Intercept

Once $b_1$ has been calculated:

$$
\boxed{
b_0=\bar y-b_1\bar x
}
$$

Therefore:

$$
\boxed{
\hat y=b_0+b_1x
}
$$

The important difference from the simple two-point calculation is that regression estimates the slope and intercept using **all observations**.

---

## 12.9 Fitted or Predicted Values

Once the regression equation is known:

$$
\hat y=b_0+b_1x
$$

we can calculate a predicted value for each observation.

For example, if:

$$
\hat y=1+2x
$$

and:

$$
x=3
$$

then:

$$
\hat y=1+(2)(3)=7
$$

Therefore:

$$
\boxed{\hat y=7}
$$

---

## 12.10 Observed Value and Predicted Value

The observed value is:

$$
y_i
$$

The regression model produces:

$$
\hat y_i
$$

These values are usually not exactly equal.

The difference is called the **residual**.

---

## 12.11 Residuals

A residual is:

$$
\boxed{
e_i=y_i-\hat y_i
}
$$

where:

- $y_i$ = observed value
- $\hat y_i$ = predicted value
- $e_i$ = residual

A positive residual means the observed value is above the fitted value.

A negative residual means the observed value is below the fitted value.

### Semiconductor Example

Suppose:

$$
\hat V=0.02+0.50I
$$

For:

$$
I=3	ext{ mA}
$$

the fitted voltage is:

$$
\hat V=0.02+(0.50)(3)=1.52	ext{ V}
$$

If the measured voltage is:

$$
V=1.48	ext{ V}
$$

then:

$$
e=1.48-1.52
$$

so:

$$
\boxed{e=-0.04	ext{ V}}
$$

---

## 12.12 Why Do We Square Residuals?

Residuals can be positive or negative. If we simply add them, they can cancel.

Instead, we square them:

$$
e_i^2
$$

and add them.

This gives the **sum of squared errors**:

$$
\boxed{
SSE=
\sum_{i=1}^{n}(y_i-\hat y_i)^2
}
$$

The least-squares regression line is the line that minimizes $SSE$.

---

## 12.13 Least-Squares Principle

The central idea is:

> **Choose the line that produces the smallest possible sum of squared residuals.**

Mathematically:

$$
\boxed{
	ext{Choose }b_0,b_1
	ext{ to minimize }
\sum_{i=1}^{n}[y_i-(b_0+b_1x_i)]^2
}
$$

This is the mathematical foundation of ordinary least-squares linear regression.

---

## 12.14 Sum of Squared Errors — SSE

$$
\boxed{
SSE=
\sum_{i=1}^{n}(y_i-\hat y_i)^2
}
$$

A smaller SSE means that the observations are, in total, closer to the fitted values.

SSE depends on the scale and units of the dependent variable, so other measures are also useful.

---

## 12.15 Mean Squared Error — MSE

For simple linear regression:

$$
\boxed{
MSE=rac{SSE}{n-2}
}
$$

The $n-2$ appears because two parameters, slope and intercept, have been estimated.

MSE represents the average squared error after accounting for the fitted parameters.

---

## 12.16 Root Mean Squared Error — RMSE

$$
\boxed{
RMSE=\sqrt{MSE}
}
$$

RMSE has the same units as the dependent variable.

For example, if the dependent variable is voltage, RMSE is measured in volts.

It can therefore be interpreted as a typical scale of prediction error.

---

## 12.17 Total Variation

The total variation in the dependent variable is:

$$
\boxed{
SST=
\sum_{i=1}^{n}(y_i-ar y)^2
}
$$

SST represents the total variation of observed values around their mean.

---

## 12.18 Explained and Unexplained Variation

The unexplained variation is represented by:

$$
SSE
$$

The explained variation is:

$$
SSR=SST-SSE
$$

Therefore:

$$
\boxed{
SST=SSR+SSE
}
$$

---

## 12.19 Coefficient of Determination — $R^2$

The coefficient of determination is:

$$
\boxed{
R^2=1-rac{SSE}{SST}
}
$$

It tells us how much of the observed variation in the dependent variable is accounted for by the fitted regression model.

For example:

$$
R^2=0.90
$$

means that about 90% of the observed variation is accounted for by the linear model for that dataset.

A high $R^2$ does not automatically prove that the physical theory is correct.

---

## 12.20 Semiconductor Example — Interpreting $R^2$

Suppose we fit:

$$
\hat V=b_0+b_1I
$$

to an approximately ohmic semiconductor device and obtain:

$$
R^2=0.98
$$

This indicates that the linear model explains a very large proportion of the variation in voltage in the observed dataset.

However, we should still examine:

- Scatter plot
- Residuals
- Operating range
- Measurement conditions
- Physical expectations

A high $R^2$ alone does not prove that the device is linear under all conditions.

---

## 12.21 Regression and Resistance

Suppose:

$$
\hat V=b_0+b_1I
$$

If $V$ is measured in volts and $I$ in amperes:

$$
b_1=rac{	ext{V}}{	ext{A}}
$$

Therefore:

$$
\boxed{
b_1=\Omega
}
$$

For an approximately ohmic region:

$$
\boxed{
R pprox b_1
}
$$

Regression therefore estimates resistance using all experimental observations.

---

## 12.22 Semiconductor Example — Sensor Calibration

Suppose a semiconductor temperature sensor produces:

| Temperature $T$ (°C) | Output $V$ (V) |
|---:|---:|
| 20 | 1.02 |
| 30 | 1.21 |
| 40 | 1.39 |
| 50 | 1.61 |
| 60 | 1.80 |

We fit:

$$
\boxed{
\hat V=b_0+b_1T
}
$$

Suppose the fitted equation is:

$$
\hat V=0.62+0.0195T
$$

Then:

$$
\boxed{
b_1=0.0195	ext{ V}/^\circ	ext{C}
}
$$

Therefore:

$$
\boxed{
	ext{Sensor sensitivity}=0.0195	ext{ V}/^\circ	ext{C}
}
$$

---

## 12.23 Prediction

Suppose:

$$
\hat V=0.62+0.0195T
$$

At:

$$
T=45^\circ	ext{C}
$$

we obtain:

$$
\hat V=0.62+(0.0195)(45)
$$

Therefore:

$$
\boxed{
\hat V pprox1.50	ext{ V}
}
$$

This is prediction using regression.

---

## 12.24 Interpolation and Extrapolation

### Interpolation

Prediction within the observed range.

If the calibration data cover:

$$
20^\circ	ext{C}	ext{ to }60^\circ	ext{C}
$$

then predicting at:

$$
45^\circ	ext{C}
$$

is interpolation.

### Extrapolation

Prediction outside the observed range.

Predicting at:

$$
100^\circ	ext{C}
$$

would be extrapolation.

Extrapolation can be risky because the relationship may change outside the measured range.

> **A regression model should not automatically be assumed valid outside the range of data used to build it.**

---

## 12.25 Correlation vs Regression

| Correlation | Regression |
|---|---|
| Measures strength and direction of linear association | Builds a mathematical relationship |
| Uses correlation coefficient $r$ | Uses regression coefficients |
| Symmetric between variables | Has a specified dependent variable |
| Does not directly provide a prediction equation | Provides a prediction equation |
| $r$ has no units | Regression coefficients have units |
| Does not by itself establish causation | Does not by itself establish causation |

For example:

$$
r=0.95
$$

indicates a strong positive linear association.

Regression may give:

$$
\hat V=0.02+0.50I
$$

which provides an equation and allows prediction.

---

## 12.26 Relationship Between Correlation and Regression

For simple linear regression with an intercept, the sign of the regression slope is the same as the sign of the Pearson correlation coefficient.

If:

$$
r>0
$$

then:

$$
b_1>0
$$

If:

$$
r<0
$$

then:

$$
b_1<0
$$

Also, in standard simple linear regression:

$$
\boxed{
R^2=r^2
}
$$

This relationship is specific to the standard simple linear regression setting.

---

## 12.27 Residual Analysis

Residuals help us decide whether the regression model is appropriate.

A useful residual plot should ideally show residuals scattered around zero without a systematic pattern.

### Good pattern

Residuals are approximately randomly scattered around:

$$
e=0
$$

### Warning signs

A curved pattern may indicate nonlinearity.

A widening pattern may indicate changing variability.

An isolated large residual may indicate an outlier.

Therefore:

> **Residual analysis is an important part of evaluating a regression model.**

---

## 12.28 Semiconductor Example — Residual Pattern

Suppose a semiconductor I–V characteristic is fitted using a straight line.

At low and medium current, residuals may be small.

At high current, residuals may become increasingly positive.

This could indicate:

- The relationship is no longer linear.
- Series resistance effects are becoming important.
- The chosen operating range is too wide for a simple linear model.

Residuals can therefore provide useful information about device behavior.

---

## 12.29 Outliers

An outlier is an observation that is unusually far from the general pattern.

In semiconductor experiments, an outlier may occur because of:

- Instrument malfunction
- Incorrect connection
- Data-entry error
- Device damage
- Sudden environmental change
- Unusual physical behavior

An outlier should not automatically be deleted.

First investigate why it occurred.

> **Statistical analysis should help us investigate unusual observations, not simply remove them.**

---

## 12.30 Assumptions of Simple Linear Regression

A simple linear regression model works best when the following conditions are reasonably satisfied.

### 1. Linearity

The relationship between the variables should be approximately linear.

### 2. Independent observations

One observation should not improperly depend on another.

### 3. Reasonably constant variability

The spread of residuals should not change dramatically across the range of $x$.

### 4. No extreme influential observations

A small number of unusual observations should not completely determine the fitted model.

---

## 12.31 Regression Does Not Prove Causation

Suppose we find:

$$
R^2=0.95
$$

between two semiconductor process variables.

This does not automatically prove that one variable causes the other.

Regression describes the relationship observed in the data.

Causal conclusions require:

- Experimental design
- Physical theory
- Controlled conditions
- Knowledge of possible confounding factors

Therefore:

> **A good regression model is evidence of a relationship in the observed data, not automatic proof of causation.**

---

## 12.32 Limitations of Linear Regression

Linear regression is not appropriate for every problem.

Problems may occur when:

- The relationship is nonlinear.
- The operating range is too large.
- Important variables are missing.
- Measurement errors are substantial.
- Outliers strongly influence the model.
- Extrapolation is performed too far beyond the observed data.

For example, a semiconductor diode has an exponential I–V relationship over an appropriate region.

A direct linear regression of $I$ on $V$ would not be appropriate over that exponential region.

An appropriate transformation or nonlinear model may be required.

---

## 12.33 Complete Semiconductor Example

Consider:

| $I$ (mA) | $V$ (V) |
|---:|---:|
| 1 | 0.49 |
| 2 | 1.02 |
| 3 | 1.48 |
| 4 | 2.03 |
| 5 | 2.51 |

We want to fit:

$$
\hat V=b_0+b_1I
$$

### Step 1 — Examine the data

The observations show an approximately increasing linear pattern.

### Step 2 — Calculate the regression slope

Use:

$$
b_1=
rac{
\sum(I_i-\bar I)(V_i-\bar V)
}{
\sum(I_i-\bar I)^2
}
$$

### Step 3 — Calculate the intercept

Use:

$$
b_0=\bar V-b_1\bar I
$$

### Step 4 — Write the regression equation

$$
\boxed{
\hat V=b_0+b_1I
}
$$

### Step 5 — Interpret the slope

Because voltage is measured in volts and current in amperes:

$$
b_1=rac{	ext{V}}{	ext{A}}=\Omega
$$

Therefore:

$$
\boxed{
b_1 pprox R
}
$$

for the approximately ohmic region.

### Step 6 — Calculate fitted values

For each current:

$$
\hat V_i=b_0+b_1I_i
$$

### Step 7 — Calculate residuals

$$
e_i=V_i-\hat V_i
$$

### Step 8 — Evaluate the fit

Use:

- Residuals
- SSE
- RMSE
- $R^2$

### Step 9 — Physical interpretation

The regression model provides an estimate of device resistance and indicates how well a straight-line model represents the measured region.

---

## 12.34 Regression Workflow

A practical regression analysis can be summarized as:

$$
\boxed{
	ext{Collect Data}
}
$$

↓

$$
\boxed{
	ext{Explore Data}
}
$$

↓

$$
\boxed{
	ext{Scatter Plot}
}
$$

↓

$$
\boxed{
	ext{Choose Appropriate Model}
}
$$

↓

$$
\boxed{
	ext{Estimate Parameters}
}
$$

↓

$$
\boxed{
	ext{Calculate Fitted Values}
}
$$

↓

$$
\boxed{
	ext{Analyze Residuals}
}
$$

↓

$$
\boxed{
	ext{Evaluate Fit}
}
$$

↓

$$
\boxed{
	ext{Interpret Physically}
}
$$

↓

$$
\boxed{
	ext{Predict if Appropriate}
}
$$

This workflow is more important than memorizing individual formulas.

---

## 12.35 Common Mistakes

### Mistake 1 — Using only two points

Regression uses the entire dataset.

### Mistake 2 — Confusing correlation with regression

Correlation measures association; regression builds a model.

### Mistake 3 — Assuming high $R^2$ proves causation

It does not.

### Mistake 4 — Ignoring residuals

A high $R^2$ does not guarantee that the model is appropriate.

### Mistake 5 — Extrapolating without caution

A model valid over one range may fail outside that range.

### Mistake 6 — Ignoring units

Regression coefficients have units determined by the variables.

### Mistake 7 — Removing outliers without investigation

An unusual observation may contain important scientific information.

---

## 12.36 Summary

Regression analysis provides a systematic way to model relationships between variables using experimental data.

The simple linear regression model is:

$$
\boxed{
\hat y=b_0+b_1x
}
$$

The slope is:

$$
\boxed{
b_1=
rac{
\sum(x_i-ar{x})(y_i-ar{y})
}{
\sum(x_i-ar{x})^2
}
}
$$

The intercept is:

$$
\boxed{
b_0=\bar y-b_1\bar x
}
$$

The residual is:

$$
\boxed{
e_i=y_i-\hat y_i
}
$$

The sum of squared errors is:

$$
boxed{
SSE=\sum(y_i-\hat y_i)^2
}
$$

The mean squared error is:

$$
\boxed{
MSE=rac{SSE}{n-2}
}
$$

The root mean squared error is:

$$
\boxed{
RMSE=\sqrt{MSE}
}
$$

The coefficient of determination is:

$$
\boxed{
R^2=1-rac{SSE}{SST}
}
$$

Regression is useful in semiconductor applications such as:

- I–V characterization
- Resistance estimation
- Sensor calibration
- Process monitoring
- Device parameter estimation
- Experimental prediction

The central idea is:

> **Regression uses many observations to build a mathematical model, quantify the relationship between variables, evaluate the quality of the fit, and make appropriate predictions.**

---

## 12.37 Key Formulae

### Regression Equation

$$
\boxed{
\hat y=b_0+b_1x
}
$$

### Regression Slope

$$
\boxed{
b_1=
rac{
\sum(x_i-\bar{x})(y_i-\bar{y})
}{
\sum(x_i-\bar{x})^2
}
}
$$

### Regression Intercept

$$
\boxed{
b_0=\bar y-b_1\bar x
}
$$

### Residual

$$
\boxed{
e_i=y_i-\hat y_i
}
$$

### Sum of Squared Errors

$$
\boxed{
SSE=\sum(y_i-\hat y_i)^2
}
$$

### Mean Squared Error

$$
\boxed{
MSE=rac{SSE}{n-2}
}
$$

### Root Mean Squared Error

$$
\boxed{
RMSE=\sqrt{MSE}
}
$$

### Total Sum of Squares

$$
\boxed{
SST=\sum(y_i-\bar y)^2
}
$$

### Coefficient of Determination

$$
\boxed{
R^2=1-rac{SSE}{SST}
}
$$

---

## 12.38 Review Questions

1. What is regression analysis?
2. Why is regression useful for experimental data?
3. What is the difference between an independent and dependent variable?
4. Write the simple linear regression equation.
5. What is the meaning of regression slope?
6. What is the meaning of regression intercept?
7. What is a fitted value?
8. What is a residual?
9. Why are residuals squared in the least-squares method?
10. What is SSE?
11. What is MSE?
12. What is RMSE?
13. What is $R^2$?
14. What is the difference between correlation and regression?
15. Why does a high $R^2$ not prove causation?
16. What is interpolation?
17. What is extrapolation?
18. Why should extrapolation be treated carefully?

### Semiconductor Application Questions

19. Why can regression be used to estimate resistance from I–V measurements?
20. What does the slope of a $V$ versus $I$ regression line represent?
21. How can regression be used for sensor calibration?
22. What could a systematic residual pattern indicate in an I–V experiment?
23. Why might a linear regression model fail for a diode over a wide voltage range?
24. Why should an outlier in semiconductor experimental data be investigated before removal?
25. Why are units important when interpreting regression coefficients?

---

## 12.39 Practice Problems

### Problem 1 — Regression Equation

A fitted regression model is:

$$
\hat y=2.5+1.8x
$$

Identify:

1. Regression intercept
2. Regression slope
3. Predicted value when $x=4$

### Problem 2 — Residual

A regression model predicts:

$$
\hat y=12.5
$$

but the observed value is:

$$
y=13.1
$$

Calculate the residual.

### Problem 3 — Semiconductor Resistance

A regression equation for an approximately ohmic device is:

$$
\hat V=0.02+480I
$$

where $V$ is in volts and $I$ is in amperes.

Determine:

1. Slope
2. Intercept
3. Estimated resistance
4. Predicted voltage at $I=0.005$ A

### Problem 4 — Sensor Calibration

A regression model for a semiconductor temperature sensor is:

$$
\hat V=0.60+0.020T
$$

where $T$ is in °C.

Calculate the predicted voltage at:

$$
T=35^\circ	ext{C}
$$

Interpret the slope.

### Problem 5 — SSE

Suppose the observed values are:

$$
y=(5,8,10)
$$

and the fitted values are:

$$
\hat y=(4,9,10)
$$

Calculate:

1. Residuals
2. Squared residuals
3. SSE

### Problem 6 — $R^2$

Suppose:

$$
SSE=20
$$

and:

$$
SST=100
$$

Calculate:

$$
R^2
$$

Interpret the result.

### Problem 7 — I–V Regression

Consider:

| $I$ (mA) | $V$ (V) |
|---:|---:|
| 1 | 0.49 |
| 2 | 1.02 |
| 3 | 1.48 |
| 4 | 2.03 |
| 5 | 2.51 |

Calculate:

1. $ar I$
2. $ar V$
3. Regression slope
4. Regression intercept
5. Regression equation
6. Estimated resistance
7. Fitted voltage for each observation
8. Residual for each observation

### Problem 8 — Model Interpretation

A semiconductor experiment gives:

$$
R^2=0.96
$$

Explain:

1. What this value tells us.
2. What it does not tell us.
3. Why residual analysis is still useful.

---

## 12.40 Final Perspective

Regression analysis brings together many ideas developed in the previous chapters:

$$
oxed{
	ext{Experimental Data}

ightarrow
	ext{Scatter Plot}

ightarrow
	ext{Relationship}

ightarrow
	ext{Model}
}
$$

Then:

$$
oxed{
	ext{Slope + Intercept}

ightarrow
	ext{Fitted Values}

ightarrow
	ext{Residuals}
}
$$

and finally:

$$
\boxed{
	ext{SSE}

rightarrow
	ext{RMSE}

rightarrow
R^2

rightarrow
	ext{Interpretation}

rightarrow
	ext{Prediction}
}
$$

The important lesson is:

> **Regression is not just a formula for calculating a line. It is a complete process for converting experimental data into a useful statistical and scientific model.**
