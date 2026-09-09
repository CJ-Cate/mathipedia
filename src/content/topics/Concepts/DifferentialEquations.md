---
title: Differential Equations
description: Equations that relate a function to its own derivative, the main families they are sorted into, and how separation of variables solves the simplest of them.
category: concept
tags:
  - calculus
  - differential-equations
  - integration
prerequisites:
  - concepts/integrals
seeAlso:
  - concepts/eulers_constant
  - concepts/logarithms
---

A differential equation is an equation which contains both a function and the derivative of that function. A simple example, and perhaps the most common at that, is compound interest. The amount of interest an account receives over a given time period is based on the amount of money in the account, and the amount of money in the account changes every time interest is granted. We can represent the balance as $B$, the net interest as $\frac{dB}{dt}$, and the percent rate as $r$. (Our independent variable will be $t$ for time.)
$$
\frac{dB}{dt}=rB
$$
The notation $\frac{dB}{dt}$ means "change in balance with respect to time".

# Types of Differential Equations
There are many types of differential equations, which can be classified based on what form the equation takes. This is important because very subtle changes to the form of a differential equation can result in dramatically different ways of solving that equation.

- **Ordinary Differential Equations (ODEs)** contain no partial derivatives.
- **Partial Differential Equations** contain partial derivatives.
- **First Order Linear Differential Equations (FOLDEs)** are equations of the form $\frac{dy}{dt}=a(t)*y+b(t)$. An FOLDE is said to be homogeneous if and only if $b(t)=0$, otherwise it would be nonhomogeneous.

*Disclaimer: This list is by no means exhaustive. A "differential equation" is a very broad term and there are counts ranging from hundreds to thousands of solved forms of differential equations.*

# Separation of Variables to Solve Homogeneous FOLDEs
One of the first types of equations that a student will encounter in a differential equations class is a homogeneous FOLDE. This form of differential equation can be used to powerfully model real-world situations while remaining relatively simple to solve. Let us solve the generic homogeneous FOLDE of $\frac{dy}{dx}=k*y$ where $k$ is a constant using the separation of variables technique.
$$
\begin{align}
    \frac{dy}{dx} & =k*y \\
	dy & =(k*y)dx && \text{Multiply by dx}  \\
	\frac{dy}{y} & =k\ dx && \text{Divide by }y\ (\text{assume }y\neq0)\\
	\int \frac{dy}{y}  & =\int k\ dx && \text{Integrate both sides} \\
	\ln|y|+c_{1} & =kx+c_{2} \\
\end{align}
$$
At this point, we are technically done. However, further steps can be taken to simplify this equation into something significantly more usable. Recall the identity $e^{\ln(x)}=x$ and that the arbitrary constants of integration ($c_{1},c_{2}$) can be combined with each other.
$$
\begin{align}
    \ln|y|+c_{1} & =kx+c_{2} && \text{Subtract }c_{1} \text{ and combine}\\
	\ln|y| & =kx+c_{3} && \text{Combine }c_{1}-c_{2} \\
	e^{\ln|y|} & =e^{kx+c_{3}} && \text{Identity} \\
	y & =e^{kx+c_{3}} && \text{Simplify} \\
	y & =e^{kx}e^{c_{3}} && \ \ \ \ \ \ \vdots \\
	y & =c_{4}e^{kx} && \ \ \ \ \ \ \vdots
\end{align}
$$
Finally, we are done. We re-write $e^{c_{3}}$ as $c$ because it is a constant.
$$
\frac{dy}{dx}=ky\to y=ce^{kx}
$$

# Sources
- MathIsGreatFun https://www.youtube.com/watch?v=QYAYH9gVe_E