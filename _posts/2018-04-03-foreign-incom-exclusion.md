---
layout: post
title: Foreign Earned Income Exclusion
categories:
- tax
- math
---

If you have income earned from working outside United States, and you satisfy either:

* bona fide residence test or
* physical presence test

then take foreign earned income exclusion.

Alternatively you can take credit for foreign tax paid, or combination of both when your foreign income could not fully excluded.

This article is not about the tax rules which you can read elsewhere, but on the mathematics involved on computing the foreign earned income exclusion. Some people may think, "Oh, it is great that I don't need to pay taxes on my foreign income", and the employers will say the same when they need to send their employees to work overseas for over a year, but this is only true if you do not have other income from U.S. sources.

Suppose your foreign income is F, and your U.S. income is U, the formula for the IRS compute your tax liability T is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;T = f(U+F) - f(F) ">

and this is greater, often much greater, than <img src="https://latex.codecogs.com/svg.latex?\small&space;f(U)">.

Let us a simple model to illustrate the problem. Suppose the tax rate is 10% for first 10,000 and 15% for next 10,000. If you have 10,000 U.S. income, then you pay 1,000 tax and that is it. Now you have 10,000 U.S. income _and_ 10,000 foreign income, the total income is 20,000, the tax on total income is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;10,000 * 10% + 10,000 * 15% = 2,500">

But you say "wait a minute", the 10,000 is the foreign income and should be excluded. Fair enough, so let us exlcude it. The tax corresponds to the 10,000 foreign income is 1,000, so the tax liability you should pay after the exclusion is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;2,500 - 1,000 = 1,500">

which is more than the 1,000 tax on U.S. income alone.

Generally,

<img src="https://latex.codecogs.com/svg.latex?\small&space;f(a+b) - f(a) \ne f(b)">

the two sides are equal only when `f()` is a linear function. The left side could be lower, for example:

<img src="https://latex.codecogs.com/svg.latex?\small&space;\sqrt{a+b} - \sqrt{a} < \sqrt{b}">

or higher, for example:

<img src="https://latex.codecogs.com/svg.latex?\small&space;(a+b)^2 - a^2 > b^2">

but when <img src="https://latex.codecogs.com/svg.latex?\small&space;f(x)"> is a upperward convex function like the tax rate, the left side is always greater. I often hear pepople say that U.S. does not put much attention on mathematics, after reading the tax code of the federal government and some of the states, I have a different conclusion.

How do we combat the problem? If the U.S. income belongs to your spouse, you can try to file separately. However, MFS has its own limitations, such as you cannot take education credit, both of spouse have to either take standard deduction or itemized deduction, etc. The only way to find out if MFS works and how well it works is to compute your tax both ways and compare.
