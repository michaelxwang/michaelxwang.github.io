---
layout: post
title: "Qualified mortgage interest and average principal amount"
categories:
- tax
---

<img src="/assets/images/20250426-mortgage-interest.png"/>

### Introduction

The mortgage interest deduction allows taxpayers to deduct mortgage interest
paid on qualified residence loans. Under the Tax Cuts and Jobs Act (TCJA), the
maximum loan amount eligible for deduction is $750,000 for loans incurred after
December 15, 2017.

In simple cases, if your mortgage balance is steady throughout the year, you
can prorate the interest directly based on the loan amount compared to the
$750,000 limit.

However, in more complex scenarios where the principal amount varies
dramatically during the year, a more precise method is required to calculate
the qualified mortgage interest.

### A complex example

Suppose the following situation occurs:

- First loan is active for the entire year 2024 but is converted to rental use starting September 1, 2024.
- A second loan is obtained on April 30, 2024, to purchase a new principal residence, and it remains active through the end of the year.

Thus, the total principal amounts fluctuate across the year, creating an irregular curve when plotted, as shown
in the diagram at the beginning of this article.

### How to calculate the deductible interest

The Total Interest (TI) is the sum of the interest per dollar per day ($$i$$) multiplied by the loan amount (L)
and by the time period ($$\Delta t$$) measured by number of days, or

$$
Q = i \times \int_0^{T} L \, dt \tag{1}
$$

Apart from the factor of $$i$$, it represents the total area under the curve (the light purple and dark purple areas combined).

The Qualified Interest (QI), on the other hand, is the dark purple area only, or

$$
Q = i \times \int_0^{T} min(750,000, L) \, dt \tag{2}
$$

Since we know the total interest paid (the total area), we use the ratio of the
purple area to the total area to prorate the qualified interest.

In practice, we can use a method similar to "cutting the circle" to carry out the calculation:

- Divide the year to a few periods where the principal changes approximately linearly within each period;
- Allocate interest paid for the period;
- Prorate the interest by:

$$
\text{Qualified Interest} = \text{Total Interest} \times \min\left(1, \frac{750,000}{\text{Average Principal}}\right) \tag{3}
$$

- Add them up.

As a spreadsheet is accidentally [Turing complete][turing]{:target="_blank"},
we developed a tool in Google sheets to automate the calculation:

<img src="/assets/images/20250426-google-sheets.png"/>

That is, you provide input as shown in purple, and
the final results appear automatically in highlighted blue.

### Average principal amount defined

The average principal amount in Equation (3) is easy to understand and compute for a period where the principal amount is nearly linear,
but how do we define the average principal amount for a year in which the principal amount fluctuates dramatically?

Well, we should define the average principal amount for year such as equation (3) will give the correct yearly
qualified interest using the yearly total interest.
In other words, we reverse the formula and define the Average Principal for the year as:

$$
\text{Average Principal} = 750,000 \times \frac{\text{Interest for the Year}}{\text{Qualified Interest for the Year}} \tag{4}
$$

Since we have the qualified interest for the year, why do we need the average principal amount? You may ask. We need to provide
total interest for the year for states. While federal tax law caps the deduction at $750,000, state tax law may have different
or no limits (some states allow the full personal residence mortgage interest deduction without the federal limitation).
Thus, by calculating the Average Principal, we can flexibly apply either the $750,000 federal limit or the relevant state-specific rules.

[turing]: https://en.wikipedia.org/wiki/Turing_completeness
