---
layout: post
title: "Tax notes: Penalty and interest"
categories:
- tax
---

The IRS, in addition to taxes, levies various penalties and interest charges. The sequence in which these penalties and interest are typically applied is as follows:

- Estimated tax penalty.
- Failure-to-file penalty.
- Failure-to-pay penalty.
- Interest charges.

### Estimated tax penalty

The IRS mandates that taxpayers pay estimated taxes on the income earned in
each quarter promptly. As the saying goes, "Pay As You Go, So You Won't Owe."

For the self-employed, upon the conclusion of each quarter, they should remit
an estimated payment using form 1040-ES or submit it online based on the
quarter's income. Interestingly, one might receive a year-end refund yet still
be liable for an estimated tax penalty if a particular quarter's obligations
were not fulfilled.

For employees, employers typically handle this through payroll withholdings. By
default, these withholdings, regardless of when made, are equally allocated
across each quarter. Thus, if you're settled for the year, you're also settled
for each quarter, and vice versa.

An alternative method for calculating the estimated tax penalty is available,
which considers the timing of your yearly income and deductions. Known as the
"Annualized Income Installment Method," it's especially advantageous for those
whose income doesn't come in steadily throughout the year. By offering a truer
representation of quarterly income, this approach can sometimes decrease or
even negate the penalty. To employ this method, one should fill out Schedule AI
of Form 2210 (Underpayment of Estimated Tax by Individuals, Estates, and
Trusts).

While referred to as a "penalty," its computation is interest-based. This
penalty, determined via Form 2210, is then noted on line 79 of Form 1040.

The default methodology for calculating the estimated tax penalty (P\) hinges
on:

* The shortfall to satisfy the required annual payment, denoted as T, and T/4
  for each quarter.

* The interest rate for each quarter (I<sub>1</sub>, I<sub>2</sub>,
  I<sub>3</sub>, I<sub>4</sub>). This rate is the [federal short-term rate][short-term]{:target="_blank"}
  as of the first month of the preceding quarter, rounded to the nearest whole number, plus an
  additional 3%. The resulting interest rate can also be found directly at the [Department of Labor website][final-rate]{:target="_blank"}.

* The duration for which the tax remains unpaid. Given that the due dates for
  quarterly estimated taxes are 4/15, 6/15, 9/15, and 1/15 (the following year),
  the delay for each quarter amounts to 12, 10, 7, and 3 months, respectively, assuming taxes are
  settled on 4/15 of the subsequent year.

Using the aforementioned parameters, the penalty is formulated as:

<img src="https://latex.codecogs.com/svg.latex?\small&space;P = \frac{T}{4} (\frac{12}{12}I_1 + \frac{10}{12}I_2 + \frac{7}{12}I_3 + \frac{3}{12}I_4)">

For the fiscal year 2016, given that I<sub>1</sub> = I<sub>2</sub> = I<sub>3</sub> = I<sub>4</sub>= 4%, the formula simplifies to:

<img src="https://latex.codecogs.com/svg.latex?\small&space;P = T \times 2.667%">

The value in line 15 of the [form 2210 for 2016][f2210-2016]{:target="_blank"}
is 2.656% (as indicated by "Multiply line 14 by 0.02656"). This gives insight
into how the number was derived. The slight discrepancy is attributed to the
method of using months instead of days, but the variance is less than 0.4%.

It's crucial to note that this percentage corresponds to the shortfall relative
to the required payment, which is the lesser value between:

- 90% of the current year's tax and
- either 100% of the previous year's tax if the prior year's AGI was below $150,000, or 110% if it exceeded $150,000

Thus, the penalty percentage in relation to the actual tax owed might be
somewhat lower than the nominal tax value.

### Fail to file penalty

- Imposed if you don't file by the return's due date (including any extensions).
- 5% or 4.5% (if Fail to pay penalty also apply) of the unpaid tax for each month or part of a month the return is late for maximum 5 months.
- If the return is more than 60 days late, there's a minimum penalty, either $435 (for tax returns that were required to be filed after December 31, 2019) or 100% of the unpaid tax, whichever is less.

### Fail to pay penalty 

- Begins accruing the day after taxes are due (typically April 16) without regard to extension. 
- 0.5% of the unpaid tax amount for each month or part of a month the tax isn't paid 
- Capped at 25% of the unpaid tax.

### Interest charges

- The IRS charges interest on unpaid taxes plus fail to file penalty (per [IRM 20.2.5.3(4)][irm]) from the original due date of the return regard to extension until the date of payment.
- The interest rate is determined quarterly and is the [federal short-term rate][short-term]{:target="_blank"}
  plus 3%, or the resulting rate at the [Department of Labor website][final-rate]{:target="_blank"}.
- Interest is compounded daily.
- Unlike penalties, the interest charge is mandatory and can't be abated for reasonable cause.
- The interest used in the calculation is the same as that used for the
  estimated tax penalty, determined quarterly but compounded daily. Since the
  computation involves more "advanced" math, [Rev. Proc. 95-17][revproc]{:target="_blank"}
  provides _Factor Tables_ to calculate the
  quarter's interest. These tables account for varying interest rates, the number
  of days in the quarter that the tax was due, and whether it's a leap year.

To illustrate how these calculations work, let's use an example. Assume that
you neither filed nor paid your 2014 taxes, which were due on 2015-04-15, until
2017-10-26, and that the owed amount is $10,000.

1. **Fail to File Penalty**: This is assessed at 5% per month or part of a
   month, for up to a maximum of 5 months. It's reduced by the fail to pay
   penalty which is 0.5% per month or part of a month. The calculation is:
  
   ![\text{Fail to file penalty} = \$10,000 \times 5% \times 5 - \$10,000 \times 0.5% \times 5 = \$2,250](https://latex.codecogs.com/svg.latex?\small&space;\text{Fail to file penalty} = \$10,000 \times 5% \times 5 - \$10,000 \times 0.5% \times 5 = \$2,250)

2. **Fail to Pay Penalty**: This is assessed at 0.5% per month or part of a month. Given that the period extends across 31 full or partial months (from 2015-04-15 to 2017-10-26), the penalty becomes:
  
   ![\text{Fail to pay penalty} = \$10,000 \times 0.5% \times 31 = \$1,550](https://latex.codecogs.com/svg.latex?\small&space;\text{Fail to pay penalty} = \$10,000 \times 0.5% \times 31 = \$1,550)

3. **Interest**: The interest rate was 3% for the first 351 days (from 2015-04-15 to 2016-03-31) and 4% for the subsequent 574 days (from 2016-04-01 to 2017-10-26). This interest is compounded daily, so the total accumulated interest is:

   ![\text{Interest} = \$12,250[(1+\frac{3%}{365})^{351} + (1+\frac{3%}{366})^{574} - 1] = \$1,174.79](https://latex.codecogs.com/svg.latex?\small&space;\text{Interest} = \$12,250[(1+\frac{3%}{365})^{351} + (1+\frac{3%}{366})^{574} - 1] = \$1,174.79)

   *Note: The base amount for calculating interest includes both the tax owed and the fail to file penalty. Also, remember that 2016 was a leap year, having 366 days.*

   If we employ the IRS's table method, calculating the interest quarter by
   quarter, the resultant amount is $1,175.72. The negligible discrepancy, less
   than a dollar, corroborates the accuracy of our method.

[short-term]: https://apps.irs.gov/app/picklist/list/federalRates.html
[final-rate]: https://www.dol.gov/agencies/ebsa/employers-and-advisers/plan-administration-and-compliance/correction-programs/vfcp/table-of-underpayment-rates
[f2210-2016]: https://www.irs.gov/pub/irs-prior/f2210--2016.pdf
[irc6651]: https://www.taxnotes.com/research/federal/usc26/6651
[irm]: https://www.irs.gov/irm/part20/irm_20-002-005r#idm140320882416896
[revproc]: https://www.section6166.com/pdf_files/Rulings_Etc/Rev_Proc_95-17v2.pdf

Reference:

- [IRC Section 6651][irc6651]{:target="_blank"}
