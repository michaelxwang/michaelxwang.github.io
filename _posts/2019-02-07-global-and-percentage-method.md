---
layout: post
title: "Global and percentage method"
categories:
- tax
- math
---

For part year and nonresidents, some states tax only the income
earned in the state, some states, notably California and New York,
compute their state tax as the tax on global income multiplied
by the percentage of income earned in the state. 

In this article, let me show you how California compute its tax for part year resident and
nonresident, and why this is advantageous to the state.

If you are a part year resident or nonresident of California, you
may be surprised to find out how California computes its tax: First
it figure the tax based on total income from all states, and then
apply the ratio of California income over the total income.

For example suppose you made $10,000 in California, and then moved
to Washington and make another $10,000 there. California will add
both the income, compute tax based on $20,000 and then divide the
tax amount by 2, and this is the tax you need to pay California.

Why should California compute its tax this complicated way instead
just using its own income? The answer is that the tax is higher
this way due to the graduated tax rates. Let us use a simple
mathematical model to illustrate the differences. Suppose the tax
rate is 10% for the first $10,000 and 15% for the second $10,000.
To use only CA income to compute tax, the result is $1,000. To use
the California method, the result is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\begin{align*}
\text{tax} &= \text{tax\_of} (10,000 + 10,000) * 10,000/(10,000 + 10,000) \\
           &= (10,000 * 10% + 10,000 * 15%) * 50% \\
           &= 2,500 * 50% \\
           &= 1,250
\end{align*}
">

Please note California tax increases if you made more money outside
of the state. Not only California uses income from other states,
but also adds back certain deductions permitted by Federal tax code,
for example, the pre tax contributions to Health Savings Account,
and the $5,000 exemption allowed by US-China tax treaty, and they
become global income *per California law*, and California income
as well if the deduction takes place in California.

In general, suppose A is California income, and B is income out
side of California, the formula used by California to compute tax
is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\text{tax} = \text{tax\_of} (A+B) \times \frac{A}{A+B}
">

Since the more your earn, the more tax you pay, so we have:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\frac{\text{tax\_of}(A+B)}{A+B} > \frac{\text{tax\_of}(A)}{A}
">

or

<img src="https://latex.codecogs.com/svg.latex?\small&space;
\text{tax\_of}(A+B) \times \frac{A}{A+B} > \text{tax\_of}(A)
">

So we can see by lumping other states' income in the formula, California is able to collect more tax. 

You may ask: what can I do about this? Well if you are single, you cannot do anything. However if you are married, and one spouse is a nonresident, you can choose to file federal jointly, and California separately because the [California law](https://www.ftb.ca.gov/individuals/filing-status-information.shtml) states:

>Use the same filing status for California that you used for your federal income tax return ...
 
>Exception: If you file a joint tax return for federal purposes, you may file separately for California if either spouse was:

>An active member of the United States armed forces or any auxiliary military branch during 2017.

>A nonresident for the entire year and had no income from California sources during 2017.

Suppose the spouse A is MD resident and the spouse B is CA resident,
and you do not want to A's income to inflate CA tax, you need to
file a joint return for federal, and perhaps a joint return for MD,
but a separate return for CA.

Most likely you cannot do this with a single return, you need to
create separate return for spouse B but only file for state only,
in which federal return is an "as if" return used for state only
but will not actually be filed.

If your software does not allow you to create two returns with the
same primary social security number, you need to switch the positions
of the spouses in the joint return to make it work.
