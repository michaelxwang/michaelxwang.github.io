---
layout: post
title: IRS underpayment penalty and how to avoid it
categories:
- tax
- math
---

In general, you are required to pay estimated taxes every quarter.
If you do not pay enough, you may have to pay an "estimated tax
penalty," which is calculated on line 38 of [Form
1040][f1040]{:target="_blank"}.

Although it is referred to as a "penalty," it is essentially an
interest charge on late payments. The interest rate for underpayment
(and overpayment) for each quarter is determined according to [IRS
rules][rule]{:target="_blank"}.

First, find the [federal short-term rate][short]{:target="_blank"}
in the first month of the previous quarter, rounded to the nearest
whole number, and add 3%. For example, if the federal short-term
rate in October 2017 was 1.27%, the interest rate for the first
quarter of 2018 would be ROUND(1.27%) + 3% = 4%. Similarly, we can
derive that the interest rates for the remaining three quarters of
2018 are 5%.

The IRS also publishes the updated interest rates directly, and the
updated table can be found [here][rate]{:target="_blank"}. The first
column is for personal and the second column is for large corporations.

Let's use the year 2018 as an example. Since the due dates for each
quarter's estimated payments were 4/15/2018, 6/15/2018, 9/15/2018,
and 1/15/2019, respectively, and the due date for the tax return
was 4/15/2019, the length of time the tax owed for each quarter was
late for 12, 10, 7, and 3 months, respectively.

Let's assume that the income and estimated tax payment (or withholding)
are the same for each quarter, meaning that you owe the same amount
each quarter. The weighted average of the annual interest rate for
2018 is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;R_{2018} = \frac{1}{4}(\frac{12}{12}\times 4% + \frac{10}{12}\times 5% + \frac{7}{12}\times 5% + \frac{3}{12}\times 5%)=3.08%">

This means that you would pay about 3% for 2018 on the shortage to
the required tax payment, which is the lesser of 90% of the current
year's tax or (100%|110%) of last year's tax. (See below for how
100% or 110% are determined.)


While the penalty for underpayment of estimated taxes may not be a significant
amount, it is still better to avoid it. The penalty will not apply if you
satisfy one of the following conditions (see [Form 2210][f2210]{:target="_blank"}
and [Form 2210 instructions][i2210]{:target="_blank"}):

- The current year's withholding is more than 90% of the current year's tax liability.
- The current year's withholding is more than the current year's tax liability minus $1,000.
- The current year's withholding is more than the previous year's tax liability multiplied by X, where X is 110% if your adjusted gross income on your previous year's return is over $150,000 or over $75,000 if you are married filing separately. Otherwise, X is 100%.

The first two conditions are difficult to follow, as they require knowledge of
the current year's tax liability, which you don't know until you complete your
tax return. On the other hand, all the necessary numbers are known for the
third condition. The previous year's tax liability is on last year's [Form 1040][f1040]{:target="_blank"}
(usually line 24), and the withholding is on your pay stub and can be
extrapolated to the end of the year. If you expect you won't satisfy the third
condition and are worried about the penalty, you can use line 4(c\) of Form
[W-4][w4]{:target="_blank"} to make extra payments.

The third condition is sufficient but not necessary to avoid the penalty. That
is, if this condition is satisfied, then there will be no penalty. For example,
with a million dollars in capital gain without tax paid, you just need to pay
the tax owed by the due date without penalty. However, if it is not satisfied,
it does not mean the penalty will apply. There will be no penalty if either of
the first two conditions are satisfied, but you won't know until you prepare
the return for the current year.

The third condition does not work well if you had a large income in the
previous year but not in the current year. It still works, but not as well.

For W-2 employees, the income and withholding are considered earned and paid
equally each quarter by default. For example, if you paid $400 in the fourth
quarter, it can be treated as if you paid $100 in each quarter, so you can make
up the tax shortage at the end of the year.

For estimated payments made on [Form 1040-ES][es]{:target="_blank"} or
via [IRS Direct Pay][direct-pay]{:target="_blank"}, unfortunately, we have to test each
quarter. If you owe taxes in previous quarters, you cannot make it up, no
matter how much you pay in the current quarter. As a result, you may end up
with a situation where you have a refund but still owe an underpayment penalty.

States have similar conditions to avoid penalties. For example, in Virginia,
you do not pay a penalty if you satisfy one of the following conditions:

- You have paid 90% of the tax you owe or the tax owed is less than $150 for the current year.
- You have paid 100% (always 100% regardless of your income) of the tax you owed for the previous tax year.

[f1040]: https://www.irs.gov/pub/irs-pdf/f1040.pdf
[rule]: https://www.irs.gov/newsroom/interest-rates-remain-the-same-for-the-first-quarter-of-2021
[short]: https://apps.irs.gov/app/picklist/list/federalRates.html
[rate]: https://www.dol.gov/agencies/ebsa/employers-and-advisers/plan-administration-and-compliance/correction-programs/vfcp/table-of-underpayment-rates
[f2210]: https://www.irs.gov/pub/irs-pdf/f2210.pdf
[i2210]: https://www.irs.gov/pub/irs-pdf/i2210.pdf
[w4]: https://www.irs.gov/pub/irs-pdf/fw4.pdf
[es]: https://www.irs.gov/pub/irs-pdf/f1040es.pdf
[direct-pay]: https://www.irs.gov/payments/direct-pay
[va]: https://tax.virginia.gov/sites/default/files/vatax-pdf/2017-form-760c-instructions.pdf
