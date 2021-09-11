---
layout: post
title: "Primary residence or rental home: which one to pay down first?"
categories:
- tax
---

## Primary residence or rental home: which one to pay down first?

A client recently asked me: I have some cash at hand, should I pay down the mortgage on my primary home first or on rental home. The answer depends on a few factors, let us convert the tax question to a general math question.

Suppose you borrow \$10,000 from bank, and the interest rate is 4%, then you pay \$400 interest. Suppose the mortgage interest is duductible, and your highest tax rate is 22%, you can "save" \$400 * 22%, or \$88. So you effectively paid \$400 - \$88, or \$312 interest, that is, your effective interest rate is 3.12%. From now on, when we talk about interest, it means effective interest with tax effect included unless it is specified.

The interest you paid on the rental property to the mortgage company is always deductible, so you always pay the reduced effective interest rate. The interest you paid on the primary resident can be divided into two parts: the part above the standard deduction is tax deductible, and you pay the reduced effective interest rate; the part below is not deductible, you pay the interest at the face value. 

<img src="/assets/images/20210911-mortgage.pdf">

So the problem is coverted to a math problem: We have to three pools of debt as shown in the digram with a dependency that we have to pay the debt on primary residence above standard deduction before the debt below the standard deduction, which one should we pay first, the primary residence or the rental home. Let us calculate each and compare.

Let us assume we pay interest and equal amount Y towards the principal each year, and that we pay at the end of the year, the total amount of money paid P if we pay primary residence first is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\begin{align*}
P &= {a+1\over2}aYS \\
         &+ {c+1\over2}cYL + acYL\\
         &+ {b+1\over2}bYM + (a+c)bYM\\
\end{align*}
">

Similarly, if we pay the rental home first, the the total amount of money paid R is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\begin{align*}
R &= {b+1\over2}bYM \\
         &+ {a+1\over2}aYS + baYS\\
         &+ {c+1\over2}cYL + (b+a)cYL\\
\end{align*}
">

Subtract these two quantities, we have:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
P-R = bY[a(M-S) - c(L-M)]
">

Without numeric calculation, we can reach the following conclusions:

- If M<=S, then P-R<0, i.e. we should pay primary residence first. This is obvious, if the interest rate on rental is small, of course we should pay primary home first.
- If M>=L, then P-R>0, i.e. we should pay rental home first. This is equally obvious.

Let us concentrate on the interesting situation when S<M<L. We can conclude that:

- when a=0, P-R<0, i.e. we should pay primary residence first. This is obvious since we only have two pools of debt, we need to pay the one with higher interest rate. 
- when a is infinity, P-R>0, i.e. we should pay rental home first. This is easy to understand: even though it is better to reach the debt below the standard deduction, but it takes hopelessly long, let us just pay rental first. 

From the equation we can also see that "b" does not change the direction of P-R, but it just amplifies the quantity. This is a bit hard to explain in word, but is a correct mathematical result.

For general situations, we have to do a numeric calculation. Let us take a real example:

> We currently have 2 loans
> 1) VA Condo - Rental property with about 100k in loan with 4% APR
> 2) NJ house - 620k in loan with 3.25% APR

The taxpayers were married and their tax brackets are 24% for federal and 6.4% for state, so there effective interest rate are:

- S = 3.25% * (1-30.4%) = 2.26%
- L = 3.25%
- M = 4.00% * (1-30.4%) = 2.78%

The standard deduction for married filing joint is 24K, the maximum tax deduction is 10K, so there are 14K interest or 14K/3.25% or 431K below the standard deduction, and 189K above the standard deduction. Suppose they pay down 50K principal plus interest, then:

- a=189K/50K = 3.78
- c=431K/50K = 8.62
- b=100K/50K = 2.00

Substitute these number in the equation:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\begin{align*}
P - R &= 2 * 50000 * [3.78*(2.78%- 2.26%) - 8.62*(3.25%-2.78%)] \\
         &= -2086 \\
\end{align*}
">

That is, if you follow this strategy you will save about \$2000 over 14 years, or about \$140 per year. It is not much, but it does not take much effort either: you just calculate once and follow it through.
