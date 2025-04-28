---
layout: post
title: "Qualified mortgage interest and average principal amount"
categories:
- tax
---

<img src="/assets/images/20250426-mortgage-interest.png"/>

### Introduction

The mortgage interest deduction allows taxpayers to deduct interest paid on qualified residence loans.
Under the Tax Cuts and Jobs Act (TCJA), the maximum loan amount eligible for deduction is $750,000 for mortgages incurred after December 15, 2017.

This post provides a mathematically accurate method for computing qualified mortgage interest directly, as well as a refined approach to defining the average mortgage balance.
Before introducing the new method, however, we will first review the methods currently provided by the IRS.

### IRS provided methods

Under Treasury Regulation [§1.163-10T(h)][reg163]{:target="_blank"},
several acceptable methods are available for determining the average balance of debt secured by a qualified residence:

- Daily basis method ([Reg. §1.163-10T(h)(3)][reg163]{:target="_blank"}): This method calculates the
  average mortgage balance by weighting the actual principal outstanding each
  day over the course of the year.

  This method can favor taxpayers
  by averaging down the balance when you do not have a loan during some months but
  while owning the home as a residence. For example, John Smith starts 2024 with a $1.5 million mortgage and pays it off on June 30.
  Under this method, his average balance is about $750,000, allowing full deduction of the interest paid.

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
  checklist, so that I can apply a more favorable calculation method - which may
  lower the average balance and thus maximize the mortgage interest deduction.

Furthermore, [Reg. §1.163-10T(h)(8)][reg163]{:target="_blank"} establishes an anti-abuse provision. Under
this rule, if the IRS determines that a taxpayer’s chosen method materially
overstates the interest deduction, the IRS has the authority to adjust the
calculation using a more appropriate method to correctly reflect the average
balance of the debt.

### Direct Method - Concept

Although the IRS provides several methods based on average mortgage balance for
simple cases, they do not address more complex real-world situations.

To handle such cases, we rely on both the law and mathematics. Instead of
calculating a single average mortgage balance for the entire year, we compute
qualified mortgage interest period-by-period throughout the year.

Within each period, if multiple loans exist, the method applies either a "Simplified
Method" or an "Exact Method" similar to the principles outlined in Treasury
Regulation [§1.163-10T(d)][reg163]{:target="_blank"} and [§1.163-10T(e)][reg163]{:target="_blank"}.

Although not explicitly listed among the IRS's provided methods, this
calculation approach is fully defensible because it is based on statutory law
and sound mathematical principles.

[IRC 163(h)(3)(B)(ii)][irc163]{:target="_blank"} establishes the basis for calculating qualified mortgage interest:

>The aggregate amount treated as acquisition indebtedness _for any period_ shall not exceed $1,000,000 ($500,000 in the case of a married individual filing a separate return).

This limit was subsequently modified by [IRC 163(h)(3)(F)(i)][irc163]{:target="_blank"}:

> Limitation on acquisition indebtedness. Subparagraph (B)(ii) shall be applied by substituting "$750,000 ($375,000" for "$1,000,000 ($500,000".

From a purely mathematical perspective, independent of tax law, the definition of interest amount for loan $$i$$
is the integral of the interest per dollar per day ($$\alpha_i$$)
multiplied by the loan amount (L_i)
over time. The total interest paid across all loans can be expressed as:

$$
\text{Total Interest} = \sum_{i=1}^{n} \int_0^{T} \alpha_i \times L_i \, dt \tag{1}
$$

Apart from the factor of $$\alpha_i$$, the total interest corresponds to the total area under the curve (the light purple and dark purple areas combined) shown in the digram.

The law simply imposes a restriction on the loan amounts eligible for deduction:

$$
\sum_{i=1}^{n} L_i \leq 750,000 \tag{2}
$$

Thus, the Qualified Interest corresponds only to the dark purple area.

Please note that the law restricts only the total loan amount eligible for the deduction; it does not dictate exactly which loans must be included.
Therefore, we have flexibility:
we can allocate proportionally across loans or allocate optimally by prioritizing loans with the higher interest rate $$\alpha$$.

### Direct Method - Example

First loan:

- 01/01/2024: Balance of $500,000
- 09/01/2024: Converted to rental property.
- 12/31/2024: Year-end balance of $400,000, interest paid: $20,000

Second loan:

- 04/30/2024: Borrowed $90,000 to buy a new home.
- 12/31/2024: Year-end balance of $80,000, interest paid: $25,000

We divided the year into three periods:

- 01/01/2024 - 04/30/2024: Only the first loan is present
- 04/30/2024 - 09/01/2024: Both loans are active.
- 09/01/2024 - 12/31/2024: Only the second loan is active (the first loan has been converted to rental use).

During each period, we can calculate:

- Beginning and ending balances for each loan by extrapolation, and then determine the average balance.
- Interest prorated to each period based on the number of days in the period.

For periods 1 and 3, we can calculate the qualified interest based on the average loan balance using the following equation:

$$
\text{Qualified Interest} = \text{Total Interest} \times \min\left(1, \frac{750,000}{\text{Average Balance}}\right) \tag{3}
$$

For period 2, we have two options:

- Average method: Combine the balances and interests of both loans and apply the same formula to the combined amounts.
- Optimal method: Prioritize including the loan with the higher interest rate first, up to the $750,000 limit.

After calculating the qualified interest for each period, we sum them to obtain the yearly total.

Since spreadsheets are accidentally [Turing complete][turing]{:target="_blank"},
we developed a Google Sheets tool to automate the calculation. You simply enter the input data (highlighted in purple), and the results appear automatically (highlighted in blue).

The image below demonstrates a calculation using the optimal method:

<img src="/assets/images/20250426-google-sheets.png"/>

### Average Loan Balance Defined

Since we have already calculated the yearly qualified mortgage interest
directly, we no longer need to compute the yearly average mortgage balance to
derive it.

The IRS typically uses the yearly average mortgage balance along with the
yearly interest paid to calculate qualified interest under Equation (3).

However, because we have already determined the yearly qualified interest
precisely, we can reverse-engineer the logic and define the average mortgage
balance in such a way that Equation (3) still produces the correct result.

In other words, we define the Average Principal for the year as:

$$
\text{Average Principal} = 750,000 \times \frac{\text{Interest for the Year}}{\text{Qualified Interest for the Year}} \tag{4}
$$

You might wonder why we still need to calculate the average mortgage balance if
the qualified interest is already known.

There are two important reasons:

- First, the IRS requires the reporting of average mortgage balances in Table 1 of [Publication 936][pub936] to calculate qualified mortgage interest using the total interest paid and the average balance.
- Second, we must provide the total interest information for state tax returns.
While federal tax law caps the deductible amount at $750,000, some states apply different limits - or no limits at all - allowing full mortgage interest deductions without federal restrictions.

Thus, by calculating the Average Principal, we retain flexibility to apply either the $750,000 federal limit or more generous state-specific rules as needed.

[irc163]: https://www.taxnotes.com/research/federal/usc26/163
[pub936]: https://www.irs.gov/pub/irs-pdf/p936.pdf
[reg163]: https://www.taxnotes.com/research/federal/cfr26/1.163-10T
[turing]: https://en.wikipedia.org/wiki/Turing_completeness
