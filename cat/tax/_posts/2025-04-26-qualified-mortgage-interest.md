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

- First loan was active for the entire year 2024 but is converted to rental use starting September 1, 2024.
- A second loan is obtained on April 30, 2024, to purchase a new principal residence, and it remains active through the end of the year.

Thus, the total principal amounts fluctuate across the year, creating an irregular curve when plotted, as shown
in the diagram at the beginning of this article.

### Definition of Qualified Interest

While [IRS Publication 936][pub936]{:target="_blank"}
provides an "average mortgage balance" method that
works well for simple cases, it does not clearly define the calculation for
complex cases involving multiple changes in principal, leading to potential
confusion.

This is because there is no precise mathematical definition of "average mortgage balance" beyond
those simple cases, and you cannot calculate something that is not defined.

Instead, we should stick to the basic text in [IRC 163(h)(3)(B)(ii)][irc163]{:target="_blank"}:

>The aggregate amount treated as acquisition indebtedness _for any period_ shall not exceed $1,000,000 ($500,000 in the case of a married individual filing a separate return).

where the limit was modified by [IRC 163(h)(3)(F)(i)][irc163]{:target="_blank"}

> Limitation on acquisition indebtedness. Subparagraph (B)(ii) shall be applied by substituting "$750,000 ($375,000" for "$1,000,000 ($500,000".

Please note the phrase _for any period_. 

Not related to the law at all, but in pure mathematics, the defintion of the interest amount for loan i is the integral of the interest per dollar per day ($$\alpha_i$$) multiplied by the loan amount (L_i)
over time period. The total interest is then the sum over all loans. Expressed as a mathematical formula:

$$
\text{Total Interest} = \sum_{i=1}^{n} \int_0^{T} \alpha_i \times L_i \, dt \tag{1}
$$

Apart from the factor of $$\alpha_i$$, the total interest is represented by the total area under the curve (the light purple and dark purple areas combined) in the digram.

The law simply adds a restriction for qualified interest: 

$$
\sum_{i=1}^{n} L_i <= 750,000 \tag{2}
$$

The Qualified Interest is represented by the dark purple area only.

Please note that the law only restricts the total loan amount eligible for the
deduction; it is up to us to choose which loan amounts to include, and how much
to include in the qualified interest calculation. We can either allocate
proportionally or allocate optimally by prioritizing the loan with the higher
interest rate $$\alpha$$.

### Calculation of Qualified Interest

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

When we have more than one loan at the same time, we need to coordinate the
the loans so that the total loan amount to include in the qualified interest calculation
does not exceed the qualified loan limit.

As a spreadsheet is accidentally [Turing complete][turing]{:target="_blank"},
we developed a tool in Google sheets to automate the calculation. That is, you provide input as shown in purple, and
the final results appear automatically in highlighted blue.

The image below demontrates a calculation using the proportional inclusion method, i.e. we use $$750,000\times \frac{L_1}{L_1+L_2}$$ amount from
loan 1 and $$750,000\times \frac{L_2}{L_1+L_2}$$ amount from loan 2. I have an optiomal method to include the loan from the highest interest rate
as much as possible with slightly modification of logic.

<img src="/assets/images/20250426-google-sheets.png"/>

### Average loan balance defined

As we previously mentioned, the average mortgage balance is not mathematically defined leading to confusion in the accouting community.

The IRS uses the avergage mortgage balance and the total interest for the year to calculate the yearly qualified interest using Equation (3).
However, since the yearly qualified interest is mathematically defined, and can be calculated independently, we can reverse the logic
and define the avergage mortgage balance such as equation (3) will give the correct yearly qualified interest using the yearly total interest.
In other words, we reverse the formula and define the Average Principal for the year as:

$$
\text{Average Principal} = 750,000 \times \frac{\text{Interest for the Year}}{\text{Qualified Interest for the Year}} \tag{4}
$$

Since we have the qualified interest for the year, why do we need the average loan balance, You may ask? Well we do it for two purposes:

- First of all, that is what the IRS asks in its table 1 in [Publication 936][pub936] to calculate qualified mortgage interest using
total interest paid and average balance;
- Secondly, We need to provide total interest for the year for states. While federal tax law caps the deduction at $750,000, state tax law may have different
or no limits (some states allow the full personal residence mortgage interest deduction without the federal limitation).
Thus, by calculating the Average Principal, we can flexibly apply either the $750,000 federal limit or the relevant state-specific rules.

[irc163]: https://www.taxnotes.com/research/federal/usc26/163
[pub936]: https://www.irs.gov/pub/irs-pdf/p936.pdf
[turing]: https://en.wikipedia.org/wiki/Turing_completeness
