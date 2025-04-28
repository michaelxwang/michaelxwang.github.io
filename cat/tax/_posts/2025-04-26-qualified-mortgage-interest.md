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

This post aims to provide a mathematically correct method to compute the
qualified mortgage interest directly, and re-define the average mortgage balance.
However, before we do that, let us survey the available methods provided by the
IRS.

### IRS provided methods

Under Treasury Regulation [§1.163-10T(h)][reg163]{:target="_blank"},
several acceptable methods are available for determining the average balance of debt secured by a qualified residence:

- Daily basis methid ([Reg. §1.163-10T(h)(3)][reg163]{:target="_blank"}): This method calculates the
  average mortgage balance by weighting the actual principal outstanding each
  day over the course of the year.

  This method can favor taxpayers
  by averaging down the balance when you do not have a loan during some months but
  while owning the home as a residence. For example, John Smith starts 2024 with a $1.5 million mortgage and pays it off on June 30.
  under this method, his average balance is about $750,000, allowing full deduction of the interest paid.

- Interest Rate Method ([Reg. §1.163-10T(h)(4)][reg163]{:target="_blank"}): This method calculates the
  average balance based on the ratio between the interest paid and the stated interest rate of the debt.

- Beginning and Ending Balance Method ([Reg. §1.163-10T(h)(5)][reg163]{:target="_blank"}): This approach
  allows the taxpayer to determine the average balance by taking the simple
  average of the beginning and ending loan balances for the year. However, this
  method may only be used when no new borrowing occurred during the tax year.

- Highest Balance Method ([Reg. §1.163-10T(h)(6)][reg163]{:target="_blank"}): Alternatively, the average
  balance can be approximated by taking the highest principal balance outstanding at any time during the year.

  This method is generally the most disadvantageous for taxpayers because it
  often lowers the deductible mortgage interest by locking in the highest debt
  level, even if the balance dropped later.

  For this reason, I specifically ask for the year-end mortgage balance in my
  checklist, so that I can apply a more favorable calculation method — which may
  lower the average balance and thus maximize the mortgage interest deduction

Furthermore, [Reg. §1.163-10T(h)(8)][reg163]{:target="_blank"} establishes an anti-abuse provision. Under
this rule, if the IRS determines that a taxpayer’s chosen method materially
overstates the interest deduction, the IRS has the authority to adjust the
calculation using a more appropriate method to correctly reflect the average
balance of the debt.

### "Exact" method - Concept

While IRS provided methods based on "average mortgage" balance work well
for simple cases, none of them work well for complex scenarios. An example was shown in the diagram at the beginning of this article where:

- First loan was active for the entire year 2024 but is converted to rental use starting September 1, 2024.
- A second loan is obtained on April 30, 2024, to purchase a new principal residence, and it remains active through the end of the year.

To handle any of the situations, we direct resort to the law and mathematics. 

[IRC 163(h)(3)(B)(ii)][irc163]{:target="_blank"} provides the basis to calculate the qualified mortgage interest:

>The aggregate amount treated as acquisition indebtedness _for any period_ shall not exceed $1,000,000 ($500,000 in the case of a married individual filing a separate return).

where the limit was modified by [IRC 163(h)(3)(F)(i)][irc163]{:target="_blank"}

> Limitation on acquisition indebtedness. Subparagraph (B)(ii) shall be applied by substituting "$750,000 ($375,000" for "$1,000,000 ($500,000".

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

### "Exact" method - Calculation

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

The steps involve using the average mortgage balance method in separate periods, and inside
each period, if there are more than two loans, we use the exact method similat to the simplified method and the exact method described in
[Reg. §1.163-10T(d)(3)][reg163]{:target="_blank"}
and
[Reg. §1.163-10T(e)(3)(iii)][reg163]{:target="_blank"}
except the loan amount is not limited by the cost basis but by the qualified limit.

As a spreadsheet is accidentally [Turing complete][turing]{:target="_blank"},
we developed a tool in Google sheets to automate the calculation. That is, you provide input as shown in purple, and
the final results appear automatically in highlighted blue.

The image below demontrates a calculation using the proportional inclusion method, i.e. we use $$750,000\times \frac{L_1}{L_1+L_2}$$ amount from
loan 1 and $$750,000\times \frac{L_2}{L_1+L_2}$$ amount from loan 2. I have an optiomal method to include the loan from the highest interest rate
as much as possible with slightly modification of logic.

<img src="/assets/images/20250426-google-sheets.png"/>

### Average loan balance defined

As we calcuale the qualified mortgage interest period by period, the
yearly average mortgage balance is not needed and not mathematically defined.

The IRS uses the yearly avergage mortgage balance and the yearly interest to calculate the yearly qualified interest using Equation (3).
However, since the yearly qualified interest is already calculated, we can reverse the logic
and define the yearly avergage mortgage balance such as equation (3) will give the correct result.
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
[reg163]: https://www.taxnotes.com/research/federal/cfr26/1.163-10T
[turing]: https://en.wikipedia.org/wiki/Turing_completeness
