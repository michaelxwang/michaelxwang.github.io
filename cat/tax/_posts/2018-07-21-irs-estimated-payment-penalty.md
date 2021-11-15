---
layout: post
title: IRS underpayment penalty and how to avoid it
categories:
- tax
- math
---

Generally speaking, you need to pay estimated tax every quarter.
If you did not pay enough, then you will pay "estimated tax penalty",
this is what line 79 of [form 1040
](https://www.irs.gov/pub/irs-pdf/f1040.pdf) is for.

Although it is called "penalty", it is essentially an interest on
the late payment. The interest rate for underpayment (and overpayment as well) on each quarter is determined
as [this](https://www.irs.gov/newsroom/interest-rates-remain-the-same-for-the-first-quarter-of-2021):
First find the [federal short-term
rate](https://apps.irs.gov/app/picklist/list/federalRates.html) in
the first month of the previous quarter, rounded to the nearest
integer, plus 3%. For example, the federal short term rate in
October 2017 is 1.27%, so the interest for the first quarter 2018
is `ROUND(1.27%) + 3% = 4%`. In the same way, we can derive the
interest rates for the rest of three quarters of 2018 are 5%.
The IRS also publish the updated interest rate directly, the
table up to the first quarter 2021 is [here](https://www.irs.gov/pub/irs-drop/rr-20-28.pdf).

Since the due dates for each quarter's estimated payments are 4/15/2018, 6/15/2018, 9/15/2018, 1/15/2019 respectively, and due date for the tax
return is 4/15/2019, so the tax payments for each quarter are late for 12, 10, 7, and 3 months respectively.
Let us assume the income, estimated tax payment (or withholding) are the same for each quarter, i.e. you owe the same amount each quarter,
the weighted average of annual interest rate for 2018 is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;R_{2018} = \frac{1}{4}(\frac{12}{12}\times 4% + \frac{10}{12}\times 5% + \frac{7}{12}\times 5% + \frac{3}{12}\times 5%)=3.08%">

which means you pay about 3% for 2018 on the shortage to required
tax payment, which is the lesser of 90% of the current year's tax
or (100%|110%) of last year's tax (with details below for 100% vs 110%).

Even the penalty is not a huge amount, it is better to avoid it.
The penalty will not apply if you satisfy one of the following
conditions (see [form 2210](https://www.irs.gov/pub/irs-pdf/f2210.pdf)
and [form 2210 instruction](https://www.irs.gov/pub/irs-pdf/f1040.pdf)):

- The _current_ year withholding is more than _current_ year tax liability * 90%.
- The _current_ year withholding is more than _current_ year tax liability - $1,000.
- The _current_ year withholding is more than _last year_'s tax liability * X`, where `X = 110% if the
adjusted gross income on your previous year's return is over $150,000,
or over $75,000 if you are married filing separately, otherwise X = 100%.
A special case is that you had no tax liability for prior year and
you were a U.S. citizen or resident alien for the entire year.

The first two condition is hard to follow as it request to know the
current year's tax which you don't until you complete the return.
On the other hand, all the numbers are known for the third condition:
the previous tax year is on the last year's form 1040, in general
we can use line 61 but for special situations, please see [form
2210 instruction](https://www.irs.gov/pub/irs-pdf/f1040.pdf) for
details; the withholding is on your pay check stub and can be easily
extrapolated to the end of year. If you expect you won't satisfy
the third condition, and are worried about the penalty, you can use
form [w4](https://www.irs.gov/pub/irs-pdf/fw4.pdf) to make a one
time additional payment.

The third condition is a sufficient condition, not a necessary
condition. That is, if this condition is satisfied, then there
will no penalty. For example, a million dollars capital gain without
tax paid, you just need to pay the tax owed by the due date without
penalty. However, if it is not satisfied, it does not mean the
penalty will apply. There will be no penalty still if either of
the first two conditions are satisfied which we do not know until
we prepare the return for the current year.

The third condition does not work well if you had a million dollars
additional income in previous year, but not in current year. It
still works, but just not well.

For W-2 employees, _by default_ the income and withholding are considered
as earned and paid equally on each quarter, for example, if you paid \$400
on 4th quarter, it can be treated as paid \$100 each quarter, so you can
make up the tax shortage at the end of year.

For estimated payment made on
[1040-ES](https://www.irs.gov/pub/irs-pdf/f1040es.pdf), unfortunately we 
have to test each quarter. If you owe taxes in previous quarters, you cannot
make it up no matter how much you pay in current quarter, so you may end up
with a situation where you have a refund, but still owe underpayment penalty.

The states have similar conditions to avoid penalties, for example,
you do not pay penalty for
[VA](https://tax.virginia.gov/sites/default/files/vatax-pdf/2017-form-760c-instructions.pdf)
if you satisfy one of the following conditions:

- You have paid 90% of the tax you owe, or the tax owed is less than $150, for the current year.
- You have paid 100% (always 100% regardless of your income) of the tax you owed for the previous tax year.
