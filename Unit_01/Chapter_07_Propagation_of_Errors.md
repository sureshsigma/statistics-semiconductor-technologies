# Chapter 7 — Propagation of Errors

## Learning Objectives

After completing this chapter, students will be able to:

- Explain the basic idea of propagation of errors.
- Understand why a calculated quantity also has uncertainty when its input measurements have uncertainty.
- Distinguish between absolute and relative uncertainty in calculations.
- Apply simple propagation rules to addition and subtraction.
- Apply simple propagation rules to multiplication and division.
- Calculate uncertainty in resistance from voltage and current measurements.
- Calculate uncertainty in power from voltage and current measurements.
- Interpret propagated uncertainty in semiconductor applications.
- Report calculated quantities with appropriate uncertainty.

---

## 7.1 Why Do We Need Propagation of Errors?

In experimental science, we often do not measure the quantity we actually want directly.

Instead, we measure some quantities and use them to calculate another quantity.

For example, resistance can be calculated from voltage and current:

$$
R=\frac{V}{I}
$$

Suppose we measure:

$$
V=5.00\text{ V}
$$

and:

$$
I=2.00\text{ mA}
$$

Then:

$$
R=\frac{5.00}{2.00}
=
2.50\text{ k}\Omega
$$

But real measurements are not perfectly exact.

Suppose:

$$
V=5.00\pm0.05\text{ V}
$$

and:

$$
I=2.00\pm0.02\text{ mA}
$$

The calculated resistance cannot be treated as perfectly exact.

The uncertainties in $V$ and $I$ affect the calculated value of $R$.

This transfer of uncertainty from measured quantities to a calculated quantity is called **propagation of errors**.

> **When measured quantities are used to calculate another quantity, the uncertainty in the input measurements affects the uncertainty of the calculated result.**

---

## 7.2 The Basic Idea

Consider a simple calculation:

$$
C=A+B
$$

If $A$ has uncertainty and $B$ has uncertainty, then $C$ also has uncertainty.

The idea can be represented as:

$$
\boxed{
\text{Input measurements}
\rightarrow
\text{Mathematical calculation}
\rightarrow
\text{Uncertainty in output}
}
$$

For example:

$$
V,\;I
\rightarrow
R=\frac{V}{I}
\rightarrow
\text{uncertainty in }R
$$

Similarly:

$$
V,\;I
\rightarrow
P=VI
\rightarrow
\text{uncertainty in }P
$$

The uncertainty does not disappear simply because we perform a calculation.

---

## 7.3 A Simple Example

Suppose:

$$
A=10\pm1
$$

and:

$$
B=20\pm2
$$

We calculate:

$$
C=A+B
$$

Therefore:

$$
C=10+20=30
$$

But $A$ and $B$ have uncertainty.

Therefore, $C$ must also have uncertainty.

Using the simple maximum-error approach:

$$
\Delta C=\Delta A+\Delta B
$$

Hence:

$$
\Delta C=1+2=3
$$

Therefore:

$$
\boxed{
C=30\pm3
}
$$

This is the basic idea of error propagation.

---

## 7.4 Propagation for Addition

Suppose:

$$
C=A+B
$$

where:

$$
A=A_0\pm\Delta A
$$

and:

$$
B=B_0\pm\Delta B
$$

For the simple maximum-error method, the absolute uncertainties are added:

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

### Example

Suppose:

$$
A=10.0\pm0.2
$$

and:

$$
B=5.0\pm0.1
$$

Then:

$$
C=10.0+5.0=15.0
$$

The uncertainty is:

$$
\Delta C=0.2+0.1=0.3
$$

Therefore:

$$
\boxed{
C=15.0\pm0.3
}
$$

---

## 7.5 Propagation for Subtraction

Suppose:

$$
C=A-B
$$

For the simple maximum-error method, the absolute uncertainties are again added:

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

This may initially seem surprising.

Although the measured values are subtracted, the possible uncertainties can combine in the same direction.

### Example

Suppose:

$$
A=20.0\pm0.2
$$

and:

$$
B=10.0\pm0.1
$$

Then:

$$
C=20.0-10.0=10.0
$$

The uncertainty is:

$$
\Delta C=0.2+0.1=0.3
$$

Therefore:

$$
\boxed{
C=10.0\pm0.3
}
$$

### Important Point

For both addition and subtraction:

> **Add the absolute uncertainties.**

---

## 7.6 Why Absolute Uncertainty Is Used for Addition and Subtraction

Consider two measurements:

$$
A=10.0\pm0.2
$$

and:

$$
B=5.0\pm0.1
$$

The quantities are added:

$$
C=A+B
$$

The uncertainty has the same unit as the measured quantities.

Therefore, adding the absolute uncertainties is natural:

$$
0.2+0.1=0.3
$$

So:

$$
C=15.0\pm0.3
$$

The uncertainty remains in the original unit.

---

## 7.7 Propagation for Multiplication

Now consider:

$$
C=AB
$$

For multiplication, it is more useful to work with **relative uncertainty**.

The simple maximum-error rule is:

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

Therefore, for multiplication:

> **Add the relative uncertainties.**

### Example

Suppose:

$$
A=10\pm1
$$

and:

$$
B=20\pm2
$$

First calculate:

$$
C=10\times20=200
$$

Relative uncertainty in $A$:

$$
\frac{\Delta A}{A}
=
\frac{1}{10}
=
0.10
$$

Relative uncertainty in $B$:

$$
\frac{\Delta B}{B}
=
\frac{2}{20}
=
0.10
$$

Therefore:

$$
\frac{\Delta C}{C}
=
0.10+0.10
=
0.20
$$

So the relative uncertainty is:

$$
20\%
$$

The absolute uncertainty is:

$$
\Delta C=0.20\times200=40
$$

Therefore:

$$
\boxed{
C=200\pm40
}
$$

---

## 7.8 Propagation for Division

Consider:

$$
C=\frac{A}{B}
$$

For the simple maximum-error method:

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

Therefore, for division also:

> **Add the relative uncertainties.**

### Example

Suppose:

$$
A=10\pm1
$$

and:

$$
B=2.0\pm0.1
$$

Then:

$$
C=\frac{10}{2}=5
$$

Relative uncertainty in $A$:

$$
\frac{1}{10}=0.10
$$

Relative uncertainty in $B$:

$$
\frac{0.1}{2.0}=0.05
$$

Therefore:

$$
\frac{\Delta C}{C}
=
0.10+0.05
=
0.15
$$

So:

$$
\Delta C=0.15\times5=0.75
$$

Therefore:

$$
\boxed{
C=5.00\pm0.75
}
$$

---

## 7.9 The Four Basic Rules

For the simple maximum-error approach:

### Addition

$$
C=A+B
$$

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

### Subtraction

$$
C=A-B
$$

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

### Multiplication

$$
C=AB
$$

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

### Division

$$
C=\frac{A}{B}
$$

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

A useful memory rule is:

> **Addition and subtraction → absolute uncertainties.**

> **Multiplication and division → relative uncertainties.**

---

## 7.10 Semiconductor Example — Calculating Resistance

Resistance is calculated from:

$$
R=\frac{V}{I}
$$

Suppose:

$$
V=5.00\pm0.05\text{ V}
$$

and:

$$
I=2.00\pm0.02\text{ mA}
$$

### Step 1 — Calculate Resistance

$$
R=\frac{5.00}{2.00}
=
2.50\text{ k}\Omega
$$

### Step 2 — Calculate Relative Uncertainty in Voltage

$$
\frac{\Delta V}{V}
=
\frac{0.05}{5.00}
=
0.01
$$

Therefore:

$$
1\%
$$

### Step 3 — Calculate Relative Uncertainty in Current

$$
\frac{\Delta I}{I}
=
\frac{0.02}{2.00}
=
0.01
$$

Therefore:

$$
1\%
$$

### Step 4 — Propagate Relative Uncertainty

Since resistance is calculated by division:

$$
\frac{\Delta R}{R}
=
\frac{\Delta V}{V}
+
\frac{\Delta I}{I}
$$

Therefore:

$$
\frac{\Delta R}{R}
=
0.01+0.01
=
0.02
$$

Thus:

$$
\boxed{
\text{Relative uncertainty}=2\%
}
$$

### Step 5 — Calculate Absolute Uncertainty

$$
\Delta R
=
0.02\times2.50
$$

Therefore:

$$
\boxed{
\Delta R=0.05\text{ k}\Omega
}
$$

Hence the result is:

$$
\boxed{
R=2.50\pm0.05\text{ k}\Omega
}
$$

---

## 7.11 Interpreting the Resistance Example

We started with:

$$
V=5.00\pm0.05\text{ V}
$$

and:

$$
I=2.00\pm0.02\text{ mA}
$$

and calculated:

$$
R=2.50\pm0.05\text{ k}\Omega
$$

The important idea is not just the formula.

The important idea is:

> **The uncertainty in the voltage and current measurements has propagated into the calculated resistance.**

Therefore, reporting only:

$$
R=2.50\text{ k}\Omega
$$

would hide useful information.

Reporting:

$$
\boxed{
R=2.50\pm0.05\text{ k}\Omega
}
$$

communicates both the calculated value and its uncertainty.

---

## 7.12 Semiconductor Example — Calculating Power

Electrical power is:

$$
P=VI
$$

Suppose:

$$
V=10.0\pm0.1\text{ V}
$$

and:

$$
I=2.0\pm0.1\text{ A}
$$

### Step 1 — Calculate Power

$$
P=10.0\times2.0
$$

Therefore:

$$
P=20.0\text{ W}
$$

### Step 2 — Relative Uncertainty in Voltage

$$
\frac{\Delta V}{V}
=
\frac{0.1}{10.0}
=
0.01
$$

### Step 3 — Relative Uncertainty in Current

$$
\frac{\Delta I}{I}
=
\frac{0.1}{2.0}
=
0.05
$$

### Step 4 — Add Relative Uncertainties

$$
\frac{\Delta P}{P}
=
0.01+0.05
=
0.06
$$

Therefore:

$$
\boxed{
\text{Relative uncertainty}=6\%
}
$$

### Step 5 — Convert to Absolute Uncertainty

$$
\Delta P
=
0.06\times20.0
$$

Therefore:

$$
\Delta P=1.2\text{ W}
$$

Hence:

$$
\boxed{
P=20.0\pm1.2\text{ W}
}
$$

---

## 7.13 A Sensor Example

Suppose a semiconductor sensor produces an output voltage:

$$
V=2.00\pm0.04\text{ V}
$$

The sensor is connected to a circuit with resistance:

$$
R=1000\pm20\Omega
$$

The current is calculated using:

$$
I=\frac{V}{R}
$$

### Step 1 — Calculate Current

$$
I=\frac{2.00}{1000}
$$

Therefore:

$$
I=0.002\text{ A}
$$

or:

$$
I=2.00\text{ mA}
$$

### Step 2 — Relative Uncertainty in Voltage

$$
\frac{\Delta V}{V}
=
\frac{0.04}{2.00}
=
0.02
$$

### Step 3 — Relative Uncertainty in Resistance

$$
\frac{\Delta R}{R}
=
\frac{20}{1000}
=
0.02
$$

### Step 4 — Propagate

Since:

$$
I=\frac{V}{R}
$$

we add relative uncertainties:

$$
\frac{\Delta I}{I}
=
0.02+0.02
=
0.04
$$

Therefore:

$$
\boxed{
\text{Relative uncertainty}=4\%
}
$$

### Step 5 — Absolute Uncertainty

$$
\Delta I
=
0.04\times2.00
=
0.08\text{ mA}
$$

Hence:

$$
\boxed{
I=2.00\pm0.08\text{ mA}
}
$$

---

## 7.14 Percentage Uncertainty

Relative uncertainty can be expressed as a percentage.

For multiplication or division:

$$
\boxed{
\text{Percentage uncertainty in result}
=
\text{sum of percentage uncertainties of inputs}
}
$$

For example, if:

$$
V
$$

has $1\%$ uncertainty and:

$$
I
$$

has $2\%$ uncertainty, then for:

$$
R=\frac{V}{I}
$$

the simple maximum-error estimate is:

$$
1\%+2\%=3\%
$$

Therefore:

$$
\boxed{
R\text{ has approximately }3\%\text{ uncertainty}
}
$$

---

## 7.15 Why Does the Rule Change?

Students often ask:

> Why do we add absolute uncertainties for addition but relative uncertainties for multiplication?

The reason is related to how a small change affects the calculated quantity.

For addition:

$$
C=A+B
$$

a change of $1$ unit in $A$ has the same unit effect on $C$ as a change of $1$ unit in $B$.

Therefore, absolute changes are naturally combined.

For multiplication:

$$
C=AB
$$

the effect depends on the size of $A$ and $B$.

A change of $1$ unit in a quantity of size $10$ is much more important than a change of $1$ unit in a quantity of size $1000$.

Therefore, relative change is more useful.

This is why multiplication and division use relative uncertainty.

---

## 7.16 A Useful Calculation Strategy

When solving propagation-of-error problems, use the following sequence.

### Step 1 — Write the equation

For example:

$$
R=\frac{V}{I}
$$

### Step 2 — Calculate the quantity

$$
R=\frac{5.00}{2.00}=2.50\text{ k}\Omega
$$

### Step 3 — Identify the type of operation

Here we have division.

Therefore, use relative uncertainties.

### Step 4 — Calculate input relative uncertainties

$$
\frac{\Delta V}{V}
$$

and:

$$
\frac{\Delta I}{I}
$$

### Step 5 — Combine the uncertainties

$$
\frac{\Delta R}{R}
=
\frac{\Delta V}{V}
+
\frac{\Delta I}{I}
$$

### Step 6 — Convert relative uncertainty into absolute uncertainty

$$
\Delta R
=
R
\left(
\frac{\Delta R}{R}
\right)
$$

### Step 7 — Report the result

$$
R=R_{\text{calculated}}\pm\Delta R
$$

This step-by-step procedure prevents many calculation errors.

---

## 7.17 Important Limitation: Simple Maximum-Error Method

The rules introduced in this chapter use a **simple maximum-error approach**.

For example:

$$
\Delta C=\Delta A+\Delta B
$$

for addition, and:

$$
\frac{\Delta C}{C}
=
\frac{\Delta A}{A}
+
\frac{\Delta B}{B}
$$

for multiplication and division.

These rules provide a conservative estimate of the maximum possible propagated error under the stated assumptions.

In more advanced experimental science, uncertainties are often combined using **root-sum-of-squares** methods based on statistical independence.

For example, independent uncertainties in addition may be combined as:

$$
u_C=
\sqrt{u_A^2+u_B^2}
$$

A full treatment of statistical uncertainty propagation requires additional mathematical concepts.

For this course, the focus is on understanding the basic idea and applying the simple propagation rules correctly.

---

## 7.18 Common Mistakes

### Mistake 1: Calculating the output but ignoring uncertainty

If the inputs have uncertainty, the calculated output generally has uncertainty too.

### Mistake 2: Adding relative errors for addition

For:

$$
C=A+B
$$

the introductory maximum-error rule uses absolute uncertainties:

$$
\Delta C=\Delta A+\Delta B
$$

### Mistake 3: Adding absolute errors for multiplication

For:

$$
C=AB
$$

use relative uncertainties:

$$
\frac{\Delta C}{C}
=
\frac{\Delta A}{A}
+
\frac{\Delta B}{B}
$$

### Mistake 4: Forgetting to convert relative uncertainty back to absolute uncertainty

If:

$$
C=100
$$

and relative uncertainty is $5\%$, then:

$$
\Delta C=0.05\times100=5
$$

Therefore:

$$
C=100\pm5
$$

### Mistake 5: Mixing units

Always use consistent units before calculating.

For example, if:

$$
I=2\text{ mA}
$$

and:

$$
V=5\text{ V}
$$

then resistance can conveniently be expressed as:

$$
R=2.5\text{ k}\Omega
$$

### Mistake 6: Reporting too many digits

The final uncertainty should guide the reporting precision.

---

## 7.19 Summary

Propagation of errors describes how uncertainty in measured quantities affects a calculated quantity.

For addition:

$$
\boxed{
C=A+B
\quad\Rightarrow\quad
\Delta C=\Delta A+\Delta B
}
$$

For subtraction:

$$
\boxed{
C=A-B
\quad\Rightarrow\quad
\Delta C=\Delta A+\Delta B
}
$$

For multiplication:

$$
\boxed{
C=AB
\quad\Rightarrow\quad
\frac{\Delta C}{C}
=
\frac{\Delta A}{A}
+
\frac{\Delta B}{B}
}
$$

For division:

$$
\boxed{
C=\frac{A}{B}
\quad\Rightarrow\quad
\frac{\Delta C}{C}
=
\frac{\Delta A}{A}
+
\frac{\Delta B}{B}
}
$$

The key idea is:

> **Uncertainty in input measurements propagates through mathematical calculations and produces uncertainty in the calculated result.**

In semiconductor applications, propagation of errors is useful when calculating:

- Resistance from voltage and current
- Power from voltage and current
- Sensor quantities
- Device parameters
- Derived experimental quantities

---

## 7.20 Key Formulae

### Addition

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

### Subtraction

$$
\boxed{
\Delta C=\Delta A+\Delta B
}
$$

### Multiplication

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

### Division

$$
\boxed{
\frac{\Delta C}{|C|}
=
\frac{\Delta A}{|A|}
+
\frac{\Delta B}{|B|}
}
$$

### Convert Relative Uncertainty to Absolute Uncertainty

$$
\boxed{
\Delta C
=
|C|
\left(
\frac{\Delta C}{|C|}
\right)
}
$$

---

## 7.21 Review Questions

### Conceptual Questions

1. What is meant by propagation of errors?
2. Why does a calculated quantity have uncertainty when its input measurements have uncertainty?
3. What is the difference between absolute and relative uncertainty?
4. What type of uncertainty is used for addition and subtraction in the simple maximum-error method?
5. What type of uncertainty is used for multiplication and division?
6. Why are relative uncertainties used for multiplication and division?
7. Why is it important to use consistent units?
8. Why should the final result not contain unjustified digits?
9. What is the difference between the simple maximum-error method and statistical uncertainty propagation?
10. Why is propagation of errors important in semiconductor experiments?

### Semiconductor Application Questions

11. Why does calculated resistance have uncertainty when voltage and current are measured with uncertainty?
12. How does uncertainty in current affect calculated power?
13. How can propagation of errors be applied to sensor measurements?
14. Why is uncertainty important when reporting a calculated semiconductor parameter?
15. Give two examples of quantities in semiconductor science that are calculated from measured quantities.

---

## 7.22 Practice Problems

### Problem 1 — Addition

Calculate:

$$
C=A+B
$$

where:

$$
A=10.0\pm0.2
$$

and:

$$
B=5.0\pm0.1
$$

Report $C$ with its uncertainty.

### Problem 2 — Subtraction

Calculate:

$$
C=A-B
$$

where:

$$
A=20.0\pm0.2
$$

and:

$$
B=10.0\pm0.1
$$

Report $C$ with its uncertainty.

### Problem 3 — Multiplication

Calculate:

$$
C=AB
$$

where:

$$
A=10\pm1
$$

and:

$$
B=20\pm2
$$

Use the simple maximum-error method.

### Problem 4 — Division

Calculate:

$$
C=\frac{A}{B}
$$

where:

$$
A=10\pm1
$$

and:

$$
B=2.0\pm0.1
$$

Report the calculated value and its uncertainty.

### Problem 5 — Semiconductor Resistance

A semiconductor device is tested at:

$$
V=5.00\pm0.05\text{ V}
$$

and:

$$
I=2.00\pm0.02\text{ mA}
$$

Calculate:

1. Resistance
2. Relative uncertainty
3. Percentage uncertainty
4. Absolute uncertainty
5. Final result

### Problem 6 — Semiconductor Power

A device operates at:

$$
V=10.0\pm0.1\text{ V}
$$

and:

$$
I=2.0\pm0.1\text{ A}
$$

Calculate:

1. Power
2. Relative uncertainty
3. Absolute uncertainty
4. Final result

### Problem 7 — Sensor Circuit

A sensor produces:

$$
V=2.00\pm0.04\text{ V}
$$

across a resistance:

$$
R=1000\pm20\Omega
$$

Calculate the current:

$$
I=\frac{V}{R}
$$

and determine its propagated uncertainty using the simple maximum-error method.

---

## 7.23 Looking Ahead

We now understand how uncertainty moves from measured quantities into calculated quantities.

The next part of the course returns to statistical relationships between variables.

In semiconductor experiments, we often want to investigate questions such as:

- Does current increase when voltage increases?
- Does sensor output increase with temperature?
- Does resistance change with temperature?
- How strongly are two measured quantities related?

These questions lead to:

$$
\boxed{
\text{Correlation and Relationships Between Variables}
}
$$
