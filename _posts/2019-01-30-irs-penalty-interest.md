---
layout: post
title: "Tax notes: Penalty and interest"
categories:
- tax
---

Besides taxes, IRS charge various penalties and interest.

First, IRS requires that the tax due on every quarter to be paid on time,
if not, there will be _estimated tax penalty_ which is calculated on Form
2210. It is possible that at the end of year, you will get a refund but
still owe estimated tax penalty because the obligation of a particular
quarter was not met. Although it is called _penalty_, it is calculated
based on interest. The penalty is reported on line 79 of Form 1040.

The estimated tax penalty (P\) is calculated based on:

* The shortage to meet the required payment, T for the year, and T/4 each quarter. 

* interest rate on each quarter (I<sub>1</sub>, I<sub>2</sub>, I<sub>3</sub>, I<sub>4</sub>) which is the [federal short-term rate](https://apps.irs.gov/app/picklist/list/federalRates.html) 
in the first month of the previous quarter, rounded to the nearest integer, plus 3%.

* The length of the time owed. Since the quarterly
estimated tax due dates for each quarter are: 4/15, 6/15, 9/15, and 1/15,
you are late each quarter for 12, 10, 7, and 3 months respectively
assuming you pay tax on 4/15 next year.

Therefore we have:

<img src="https://latex.codecogs.com/svg.latex?\small&space;P = \frac{T}{4} (\frac{12}{12}I_1 + \frac{10}{12}I_2 + \frac{7}{13}I_1 + \frac{3}{12}I_4)">

For the year 2016, we have I<sub>1</sub> = I<sub>2</sub> = I<sub>3</sub> = I<sub>4</sub>= 4%, so

<img src="https://latex.codecogs.com/svg.latex?\small&space;P = T \times 2.667%">

The percentage is on line 15 of [form 2210](https://www.irs.gov/pub/irs-pdf/f2210.pdf) is 2.656%, the error 
due to the use of months instead of days is less than 0.4%.

Please note that the percentage is based on the shortage to the required payment for the lesser of 
90% of this year's tax or 100% (when AGI is less $150,000) or 110% (when AGI
is more than $150,000) of prior year's tax, so the percentage based on the
actual tax owed is less than the of the actual tax.

If you do not file and pay tax on time, there will be additional *fail to file penalty*, *fail to pay penalty*,
and additional *interest* until it is paid.

The fail to file penalty is 5% per month or partial month up to 25%
of the tax owed [IRC Section 6651(a)(1)](https://www.law.cornell.edu/uscode/text/26/6651).

The fail to pay penalty is 0.5% per month or partial month up to 25%
of the tax owed [IRC Section 6651(a)(2)](https://www.law.cornell.edu/uscode/text/26/6651).

If you owe both fail to file penalty and fail to pay penalty, the fail
to file penalty is reduced by the amount of fail to pay penalty [IRC Section 6651(c\)(1)](https://www.law.cornell.edu/uscode/text/26/6651).

The interest used in calculation is the same
as in estimated tax penalty determined quarterly, but
compounded daily. As the calculation involves the "advanced" math,
[Rev. Proc. 95-17](https://www.section6166.com/pdf_files/Rulings_Etc/Rev_Proc_95-17v2.pdf)
provided the _Factor Tables_ to calculated the interest of a quarter
for different interest rate, number of days of the quarter the tax
was due, and whether the year is leap year or not.

Let me use an example to demonstrate how these amounts are
calculated. Suppose you did not file nor pay 2014 tax due on 2015-04-15,
until 2017-10-26, and you owe $10,000 in tax.

The _fail to file penalty_ is 5% per month or per partial month up to
the maximum of 5 months, reduced by _fail to pay penalty_ of 0.5% per month or per partial month for the period. Therefore
we have:

<img src="https://latex.codecogs.com/svg.latex?\small&space;\text{Fail to file penalty} = \$10,000 * 5% * 5 - \$10,000 * 0.5% * 5 = \$2,250">

The fail to pay penalty is 0.5% per month or per partial month for 31
full or partial months (From 2015-04-15 to 2017-10-26):

<img src="https://latex.codecogs.com/svg.latex?\small&space;\text{Fail to pay penalty} = \$10,000 * 0.5% * 31 = \$1,550">

The interest was 3% for first 351 days (from 2015-04-15 to 2016-03-31),
and 4% for the rest of 574 days (from 2016-04-01 to 2017-10-26),
accumulated daily, so the total interest is:

<img src="https://latex.codecogs.com/svg.latex?\small&space;\text{Interest} = \$12,250[(1+\frac{3%}{365})^{351} + (1+\frac{3%}{366})^{574} - 1] = \$1,174.79">

Please note the base amount is the tax owed plus the fail to file
penaty [IRM 20.2.5.3(2)](https://www.irs.gov/irm/part20/irm_20-002-005r#idm140320882416896), and 2016 is a leap year (366 days).

If we use the IRS table method to calculate interest quarter by quarter,
the result is $1,175.72. The difference due to rounding is less than
a dollar.
