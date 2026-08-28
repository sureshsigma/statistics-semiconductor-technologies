# Chapter 10 — Slope and Intercept

## Learning Objectives

After completing this chapter, students will be able to:

- Understand the meaning of slope and intercept.
- Calculate slope from two experimental observations.
- Calculate the intercept of a straight line.
- Interpret positive, negative and zero slopes.
- Understand the units of slope.
- Write the equation of a straight line.
- Interpret slope and intercept in semiconductor experiments.
- Understand how slope can represent a physical parameter.
- Understand why intercepts are important in experimental measurements.

---

## 10.1 Introduction

A linear relationship can be written as:

$$
\boxed{
y=a+bx
}
$$

This equation contains two important parameters:

$$
\boxed{a=\text{intercept}}
$$

and:

$$
\boxed{b=\text{slope}}
$$

These are not merely mathematical quantities.

In experimental science, slope and intercept can often provide useful information about the physical system being studied.

For example, in an electrical measurement:

$$
V=RI
$$

the slope of a voltage-current graph can represent resistance.

Similarly, in sensor calibration, the slope can represent sensor sensitivity.

Therefore, understanding slope and intercept is important before studying regression analysis.

---

## 10.2 What Is Slope?

Slope describes how rapidly one variable changes with respect to another variable.

It is defined as:

$$
\boxed{
b=\frac{\Delta y}{\Delta x}
}
$$

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

In simple words:

> **Slope tells us how much the output changes when the input changes.**

---

## 10.3 Simple Example

Consider two points:

$$
(2,5)
$$

and:

$$
(6,13)
$$

The slope is:

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

This means that for every one-unit increase in $x$, $y$ increases by 2 units.

---

## 10.4 Positive Slope

If:

$$
b>0
$$

the line rises as $x$ increases.

For example:

$$
y=2+3x
$$

has:

$$
b=3
$$

Therefore, $y$ increases as $x$ increases.

---

## 10.5 Negative Slope

If:

$$
b<0
$$

the line falls as $x$ increases.

For example:

$$
y=10-2x
$$

has:

$$
b=-2
$$

Therefore, $y$ decreases as $x$ increases.

---

## 10.6 Zero Slope

If:

$$
b=0
$$

then:

$$
y=a
$$

The value of $y$ does not change when $x$ changes.

For example:

$$
y=5
$$

has:

$$
b=0
$$

This represents a horizontal line.

---

## 10.7 What Is Intercept?

The intercept is the value of $y$ when:

$$
x=0
$$

Starting with:

$$
y=a+bx
$$

put:

$$
x=0
$$

Then:

$$
y=a+b(0)
$$

Therefore:

$$
\boxed{y=a}
$$

Thus:

$$
\boxed{
a=\text{y-intercept}
}
$$

The intercept is the point where the fitted line crosses the y-axis.

---

## 10.8 Example of Intercept

Consider:

$$
y=4+2x
$$

Here:

$$
a=4
$$

and:

$$
b=2
$$

When:

$$
x=0
$$

we obtain:

$$
y=4
$$

Therefore:

$$
\boxed{\text{Intercept}=4}
$$

---

## 10.9 Understanding the Complete Equation

Consider:

$$
y=5+2x
$$

We can interpret this equation as:

$$
\boxed{
\text{Output}
=
\text{initial value}
+
\text{rate of change}\times\text{input}
}
$$

Therefore:

- $5$ is the intercept.
- $2$ is the slope.

If $x$ increases by 1, $y$ increases by 2.

If:

$$
x=0
$$

then:

$$
y=5
$$

---

## 10.10 Units of Slope

Slope has units:

$$
\boxed{
\frac{\text{units of dependent variable}}
{\text{units of independent variable}}
}
$$

This is extremely important in experimental science.

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
\text{slope}
=
\frac{\text{V}}{\text{A}}
$$

Since:

$$
1\frac{\text{V}}{\text{A}}=1\Omega
$$

the slope has units:

$$
\boxed{\Omega}
$$

The units often help us identify the physical meaning of the slope.

---

## 10.11 Semiconductor Example — Resistance

Consider an approximately ohmic device.

Ohm's law is:

$$
V=IR
$$

Rearrange:

$$
V=RI
$$

Compare this with:

$$
y=a+bx
$$

We have:

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
b=R
$$

Therefore:

$$
\boxed{
\text{slope}=R
}
$$

when voltage is plotted against current.

This is one of the most important physical interpretations of slope in semiconductor measurements.

---

## 10.12 Experimental I–V Example

Suppose we obtain:

| Current $I$ (mA) | Voltage $V$ (V) |
|---:|---:|
| 1 | 0.50 |
| 2 | 1.01 |
| 3 | 1.49 |
| 4 | 2.02 |
| 5 | 2.51 |

Take two points:

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

or:

$$
\boxed{
R\approx503\Omega
}
$$

The slope has given us a physical device parameter.

---

## 10.13 Why Does the Intercept Matter?

For an ideal resistor:

$$
V=RI
$$

When:

$$
I=0
$$

we expect:

$$
V=0
$$

Therefore, the ideal intercept is:

$$
\boxed{0}
$$

But real experimental data may produce:

$$
V=V_0+RI
$$

For example:

$$
V=0.03+500I
$$

Here:

$$
a=0.03\text{ V}
$$

and:

$$
b=500\Omega
$$

The non-zero intercept may indicate an experimental offset or another effect.

The important lesson is:

> **A non-zero intercept should be investigated rather than automatically ignored.**

---

## 10.14 Semiconductor Example — Contact and Measurement Effects

Suppose an experimentally measured relationship is:

$$
V=V_0+RI
$$

The slope represents the resistance associated with the measured system.

The intercept:

$$
V_0
$$

may arise from factors such as:

- Instrument offset
- Contact effects
- Measurement configuration
- Voltage offset
- Other systematic effects

The exact interpretation depends on the experimental setup.

Therefore:

> **Statistical parameters must always be interpreted using physical knowledge of the experiment.**

---

## 10.15 Sensor Calibration

Slope is also extremely important in sensor technology.

Suppose a semiconductor temperature sensor produces:

| Temperature (°C) | Output Voltage (V) |
|---:|---:|
| 20 | 1.02 |
| 30 | 1.21 |
| 40 | 1.39 |
| 50 | 1.61 |
| 60 | 1.80 |

Suppose the relationship is approximately:

$$
V=a+bT
$$

Here:

- $T$ = temperature
- $V$ = sensor output
- $a$ = intercept
- $b$ = sensitivity

If:

$$
b\approx0.020\text{ V}/^\circ\text{C}
$$

then:

$$
\boxed{
\text{Sensor sensitivity}
\approx0.020\text{ V}/^\circ\text{C}
}
$$

This means the output changes by approximately 20 mV for every $1^\circ$C change in temperature.

---

## 10.16 Slope Can Represent Different Physical Quantities

The same mathematical concept can have different physical interpretations.

| Experimental relationship | Slope may represent |
|---|---|
| $V$ vs $I$ | Resistance |
| Sensor output vs temperature | Sensitivity |
| Position vs time | Velocity |
| Temperature vs time | Rate of heating |
| Process parameter vs output | Process sensitivity |
| Calibration output vs reference | Calibration factor |

Therefore:

> **Never interpret the slope without considering the variables and their units.**

---

## 10.17 Calculating Intercept from Slope

Suppose we know:

$$
y=a+bx
$$

and have one point:

$$
(x,y)
$$

Rearranging:

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

and the line passes through:

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

The equation is:

$$
\boxed{
y=2+2x
}
$$

---

## 10.18 Finding the Equation from Two Points

Suppose two points are:

$$
(x_1,y_1)
$$

and:

$$
(x_2,y_2)
$$

### Step 1 — Calculate slope

$$
b=
\frac{y_2-y_1}{x_2-x_1}
$$

### Step 2 — Calculate intercept

Use:

$$
a=y-bx
$$

### Step 3 — Write the equation

$$
\boxed{
y=a+bx
}
$$

---

## 10.19 Semiconductor Example — Complete Calculation

Suppose two experimental points from an I–V measurement are:

$$
(I_1,V_1)=(2\text{ mA},1.00\text{ V})
$$

and:

$$
(I_2,V_2)=(5\text{ mA},2.50\text{ V})
$$

### Step 1 — Slope

$$
b=
\frac{2.50-1.00}{5-2}
$$

Therefore:

$$
b=\frac{1.50}{3}
$$

$$
\boxed{
b=0.50\text{ V/mA}
}
$$

Therefore:

$$
\boxed{
R=0.50\text{ k}\Omega
}
$$

### Step 2 — Intercept

Using:

$$
a=V-bI
$$

with the first point:

$$
a=1.00-(0.50)(2)
$$

Therefore:

$$
\boxed{
a=0
}
$$

So the relationship is:

$$
\boxed{
V=0.50I
}
$$

This is exactly the expected form for an ideal ohmic relationship.

---

## 10.20 Slope and Intercept in Experimental Data

In real experiments, we normally have many observations.

For example:

| $I$ (mA) | $V$ (V) |
|---:|---:|
| 1 | 0.49 |
| 2 | 1.02 |
| 3 | 1.48 |
| 4 | 2.03 |
| 5 | 2.51 |

The observations do not lie perfectly on a line.

We therefore need a method to determine the **best values of slope and intercept**.

That method is called **regression analysis**.

We will study it later.

For now, the important thing is to understand what slope and intercept mean.

---

## 10.21 Common Mistakes

### Mistake 1 — Reversing the slope formula

Correct:

$$
b=
\frac{y_2-y_1}{x_2-x_1}
$$

### Mistake 2 — Forgetting units

Slope must have units.

### Mistake 3 — Confusing slope with intercept

For:

$$
y=a+bx
$$

$a$ is the intercept and $b$ is the slope.

### Mistake 4 — Assuming intercept is always zero

It is zero only when the relationship passes through the origin.

### Mistake 5 — Giving a physical interpretation without checking units

The units are an important clue to the physical meaning.

---

## 10.22 Summary

A straight-line relationship is:

$$
\boxed{
y=a+bx
}
$$

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

The slope tells us:

> **How rapidly the dependent variable changes with the independent variable.**

The intercept tells us:

> **The predicted value of the dependent variable when the independent variable is zero.**

In semiconductor applications:

$$
V=RI
$$

gives:

$$
\boxed{
\text{slope}=R
}
$$

and in sensor calibration:

$$
V=a+bT
$$

gives:

$$
\boxed{
\text{slope}=\text{sensor sensitivity}
}
$$

Therefore:

> **Slope and intercept are mathematical parameters that can have important physical meaning.**

---

## 10.23 Key Formulae

### Straight Line

$$
\boxed{
y=a+bx
}
$$

### Slope

$$
\boxed{
b=
\frac{y_2-y_1}{x_2-x_1}
}
$$

### Intercept

$$
\boxed{
a=y-bx
}
$$

### Resistance from V–I Slope

$$
\boxed{
R=\frac{\Delta V}{\Delta I}
}
$$

---

## 10.24 Review Questions

1. What is slope?
2. What is intercept?
3. Write the equation of a straight line.
4. What does a positive slope indicate?
5. What does a negative slope indicate?
6. What does zero slope indicate?
7. What are the units of slope?
8. How is the intercept calculated?
9. Why is the intercept important in experimental measurements?
10. Why should the units of slope always be considered?

### Semiconductor Applications

11. Why does the slope of a $V$–$I$ graph represent resistance?
12. What does a non-zero intercept in an experimental I–V relationship indicate?
13. How can slope be used to determine sensor sensitivity?
14. Why might the experimentally observed intercept differ from the ideal theoretical value?
15. Why is physical knowledge required to interpret slope and intercept?

---

## 10.25 Practice Problems

### Problem 1

Calculate the slope of the line passing through:

$$
(2,5)
$$

and:

$$
(6,13)
$$

### Problem 2

For:

$$
y=5+3x
$$

identify:

1. Slope
2. Intercept
3. Value of $y$ when $x=0$

### Problem 3 — Semiconductor Resistance

An approximately ohmic device gives:

$$
(I_1,V_1)=(1\text{ mA},0.50\text{ V})
$$

and:

$$
(I_2,V_2)=(5\text{ mA},2.50\text{ V})
$$

Calculate the resistance.

### Problem 4 — Sensor Sensitivity

A temperature sensor gives:

$$
V_1=1.00\text{ V}
$$

at:

$$
T_1=20^\circ\text{C}
$$

and:

$$
V_2=1.50\text{ V}
$$

at:

$$
T_2=45^\circ\text{C}
$$

Calculate the sensitivity in V/°C.

### Problem 5 — Intercept

A fitted relationship is:

$$
V=0.02+500I
$$

where $V$ is in volts and $I$ is in amperes.

Identify:

1. Slope
2. Intercept
3. Physical meaning of the slope
4. Possible interpretation of the intercept

### Problem 6 — Complete Line

Two semiconductor measurements are:

$$
(I_1,V_1)=(2\text{ mA},1.1\text{ V})
$$

and:

$$
(I_2,V_2)=(5\text{ mA},2.6\text{ V})
$$

Find:

1. Slope
2. Intercept
3. Equation of the line
4. Physical interpretation of the slope

---

## 10.26 Looking Ahead

We now understand the two important parameters of a straight-line relationship:

$$
\boxed{
\text{slope}
\quad\text{and}\quad
\text{intercept}
}
$$

But in real semiconductor experiments, we normally have many observations rather than just two points.

The next question is:

> **How do we measure the strength of the relationship between two variables?**

This leads to the next chapter:

$$
\boxed{
\text{Correlation Coefficient}
}
$$

After that, we will move to **regression analysis**, where we will learn how to determine the best-fitting slope and intercept from many observations.
