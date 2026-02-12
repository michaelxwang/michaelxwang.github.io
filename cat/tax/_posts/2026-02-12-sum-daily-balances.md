---
layout: post
title: "Optimizing the Mortgage Interest Deduction"
categories:
- tax
---

<img src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRWyqc0xf5-AVN9-fshHvrFDXB-PYEMj8w9Z7FbCIYPUzELpW5VUXDBcFazSGOT-SAlBQBoaZxk8LnQ/pubchart?oid=1827100040&format=image"/>

The mortgage interest deduction allows taxpayers to deduct interest paid on qualified residence loans.
Under the Tax Cuts and Jobs Act (TCJA), the deduction is limited to interest paid on the first $750,000 of home acquisition debt
for mortgages incurred after December 15, 2017.

The IRS provides a formula to prorate the deductible interest when your loan exceeds this limit:

$$
\text{Qualified Interest} = \text{Total Interest} \times \min\left(1, \frac{750,000}{\text{Average Balance}}\right) \tag{3}
$$

Under Treasury Regulation [§1.163-10T(h)][reg163]{:target="_blank"},
taxpayers may use one of several methods to determine the average balance
of debt secured by a qualified residence:

- Daily Basis Method ([Reg. §1.163-10T(h)(3)][reg163]{:target="_blank"})
- Interest Rate Method ([Reg. §1.163-10T(h)(4)][reg163]{:target="_blank"})
- Beginning and Ending Balance Method ([Reg. §1.163-10T(h)(5)][reg163]{:target="_blank"})
- Highest Balance Method ([Reg. §1.163-10T(h)(6)][reg163]{:target="_blank"})

Among these, the Interest Rate and Highest Balance methods are generally
disadvantageous. They fail to lower the average during periods where your loan
balance is low. The Beginning and Ending Balance Method is better, but it is
restricted to loans with "level payments at fixed equal intervals."

The Daily Basis Method calculates the average balance by weighting the actual principal outstanding on each day of the year.
This often favors taxpayers by reducing the average balance if the loan did not exist for the entire year,
provided the home was still a qualified residence.
Consider this example: John Smith starts 2024 with a $1.5 million mortgage but pays it off on June 30.
Under this method, his average balance for the year is roughly $750,000. Since this average does not exceed the limit, he can deduct the full interest paid.

However, this method can be tedious, seemingly requiring 365 data points.
This post introduces a simple tool to automate this calculation.

Let's examine the use case illustrated in the chart above:

- Day 1: Taxpayer has a $1.0 million loan.
- Day 2: Taxpayer takes a new $1.7 million loan to buy a new home.
- Day 3: Taxpayer sold her old home.
- Day 4: Taxpayer paid down the new loan with the proceeds from the old home.

This scenario is summarized with the table below:

| Days | Loan 1 | Loan 2<br> before paydown | Loan 2<br> after paydown | Daily balance<br> over all loans|
|------|--------|------------------------|------------------------|----------------|
| 1    | $1.0   |                        |                        | $1.0           |
| 2    | $0.9   | $1.7                   |                        | $2.6           |
| 3    | $0.8   | $1.5                   |                        | $2.3           |
| 4    | $0.0   | $1.3                   |                        | $1.3           |
| 5    |        |                        | $0.5                   | $0.5           |
| 6    |        |                        | $0.3                   | $0.3           |
| 7    |        |                        | $0.1                   | $0.1           |
| Sum over days for<br> each loan (segment) | $2.7 | $4.5            | $0.9                   | $8.1           |

Under the standard Daily Basis Method, you would:

1. Sum all loan balances for a specific day to get a daily total.
2. Sum those daily totals for the entire year.
3. Divide by the number of days the taxpayer owned a home (even if they did not have a loan for all of those days).

This is illustrated by the "Daily Balance" column. The sum of these daily
balances is $8.1 million. Dividing by 7 days gives an average daily balance of
$1,157,143.

By the commutative property of addition, we can calculate the sum of daily balances alternatively by
adding the daily balances first for each loan or debt segment.

Mathematically, the calculation doesn't care if a balance belongs to an old
loan, a new loan, or a single loan interrupted by a massive paydown. It simply
treats any period with a linearly decreasing balance as a "segment". For our use case, you would:

1. Calculate the sum for the Loan 1 segment.
2. Calculate the sum for the Loan 2 segment (before paydown).
3. Calculate the sum for the Loan 2 segment (after paydown).

This is shown in the bottom row: "Sum over days for each loan."

More often than not, loans are paid monthly, meaning the balance decreases linearly.
This allows us to calculate the "sum of balances" for any linear segment using a simple average for
that period multiplied by the number of days, rather than logging 365
individual entries.

Whenever a major disruption occurs, like the large paydown on Loan 2, we simply
split the timeline and treat the period after the paydown as a brand new
segment.

This [Google Sheets doc][google-sheets]{:target="_blank"} automates the calculation. If you are in this situation, please
include the spreadsheet in your tax documents.

[reg163]: https://www.taxnotes.com/research/federal/cfr26/1.163-10T
[google-sheets]: https://docs.google.com/spreadsheets/d/1906CSp8IiGdfGlHGJUj4ddRvvYFU66puhNXlILLfPm8
