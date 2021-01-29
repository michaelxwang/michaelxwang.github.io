---
layout: post
title: '"Complicated" math in tax law: SE tax and retirement plan'
categories:
- tax
- math
---

If you are self employed (SE), or burn the midnight oil to make extra
money, then you are familiar with form 1099-MISC. When you file tax,
besides income tax, you need to pay SE tax on IRS [schedule SE][1],
a simplified version is shown here:

```
   1a Net farm profit or (loss) from Schedule F
    b ... enter the amount of Conservation Reserve Program payments ...
   2 (*) Net profit or (loss) from Schedule C
   3 Combine lines 1a, 1b, and 2 
   4 (*) Multiply line 3 by 92.35% (0.9235)
   5 (*) Multiply line 4 by 15.3% (0.153). 
   6 (*) Deduction for one-half of self-employment tax. Multiply line 5 by 50% (0.50).
```

where 1a and 1b are rare form of income most of us do not have, so
basically to figure out the SE tax, you multiple the net profit by 92.35%,
and then 15.3%.

The percentage 15.3% is the SE tax, also called FICA tax to fund the social security
and medicare. For employees, these two taxes appear in Box 4 and 6 of
your W-2. If you are not highly paid individual who are affected by
additional medicare tax as added by the Affordable Care Act (ACA, aka
Obama Care), then you can verify that the social security tax _withheld_,
and medicare tax _withheld_ are 6.20% and 1.45% respectively, or 7.65%
together. Not shown on W-2, but the employer also contribute the same
amount. As a SE person, you are employer and employee at the same time,
so you pays the double amount: 7.65% \* 2 = 15.3%. This explains the FICA
tax rate, but where does 92.35% (0.9235) comes from?

Apparently, the percentate comes from:

   1 - 7.65% = 92.35%

i.e. the percentage left after one-half of the SE tax (employer portion)
deducted.

However this is incorrect because you deduct the employer's portion
based on the net income, but actually pay the same percentage based on
the amount after deduction. Let the net income to be N, the employer's
portion you _deduct_ is:

   N \* 7.65%

The employer's portion that you _pay_ is:

   N\*(1-7.65%)\*7.65%

These two amounts should be equal but are not equal.

The correct percentage X that you deduct should be the tax you actually paid, or:

   N\*(1-X)\*7.65% = N\*X

OR X = 7.65%/(1+7.65%) = 7.11%.

Using the formula for [Taylor series expansion][2], and ignore the second
order and higher, we have:

   X = 1 - 7.65% = 92.35%

So we can say the percentage that IRS used is first order approximation of
the Taylor series, although there is no such a need as this is a constant
that only need to be compute once. Fortunately this "approximation"
favors the taxpayer.

By the way, the 92.35% of the net earnings from the Sch. C business is what
listed as "Your Taxed Social Security Earnings" and "Your Taxed Medicare Earnings"
in "Your Social Security Statement", and this ought to be what is used to compute
the ["quarter of coverage"](https://www.ssa.gov/OACT/COLA/QC.html).

In computing the retirement contribution of SE person, however, the IRS
choose to face the mathematical reality.

When setting up a SE retirement plan, you need to set a plan contribution
percentage up to 25% based on the plan compensation. While this is easy
to compute for your employees as the plan compensation is the net income
without adjustment. For the SE person to make his own contribution it
is ["more complicated"][3] because the net income should exclude the
contribution amount to arrive plan compensation. For example, if your
plan contribution rate is 10%, and your net income is 100. If you use
the plan rate then your contribution is 100\*10% = 10, and the plan
compensation is 100 - 10 = 90, so the contribution percentage becomes
10/90 = 11.11% which violates the preset plan contribution percentage. In
[the words of IRS][3]:

> your plan compensation and the amount of your own plan
> contribution/deduction depend on each other - to compute one, you need
> the other (this is a circular calculation).

To solve this problem,
IRS proposes to use a reduced rate which, of course is listed in a table
found in [Publication 560][4] together with worksheets, something that IRS
does best. The table is copied below for all percentages from 1% to 25%:

|  Plan rate (R) | Your rate (r\) |
|  -:        | -:        |
|   1 | .009901 |
|   2 | .019608 |
|   3 | .029126 |
|   4 | .038462 |
|   5 | .047619 |
|   6 | .056604 |
|   7 | .065421 |
|   8 | .074074 |
|   9 | .082569 |
|  10 | .090909 |
|  11 | .099099 |
|  12 | .107143 |
|  13 | .115044 |
|  14 | .122807 |
|  15 | .130435 |
|  16 | .137931 |
|  17 | .145299 |
|  18 | .152542 |
|  19 | .159664 |
|  20 | .166667 |
|  21 | .173554 |
|  22 | .180328 |
|  23 | .186992 |
|  24 | .193548 |
|  25\*|.200000\* |

Let us see how to use the table. Use the same sample as above, if
the plan rate is 10%, your rate should be reduced to 9.0909%. So your
contribution is 100\*9.0909% = 9.0909. The plan compensation is then 100 -
9.0909 = 90.9091, and then plan contribution rate "magically" equals to
9.0909/90.9091 = 10% within the margin of errors, which agrees with the
plan policy.

How does this "magic" occur? The "circular calculation" is actually
called an equation in mathematical terms. Let N be net income, C be
your contribution, R be the plan contribution rate, and P the plan
compensation. True that Plan compensation depends on contribution:

   P = N - C

True also the contribution depends on the plan compensation:

   C = P \* R

We can resolve this circular relationship mathematically, and get

   r = C/N = R/(1+R)

where r is your rate defined as the ratio of
contribution over the net income. We can easily verify, as an example,
that when plan rate is 10%, the personal rate is 10%/(1+10%) = 9.0909%,
which agrees with IRS table.

We can take first derivative, or rewrite the C/N = 1/(1+1/R), or use
the IRS table to show that the personal rate is monotonically increasing
function of R, and the maximum personal rate is 20%.

Here we assume the net income has been adjusted for SE tax with one-half
of SE tax deducted. As we recall from discussion above, the SE tax is
unadjusted net income times (1-7.65%) and times 15.3%, so the net income
adjusted for SE tax is unadjusted net income times (1-(1-7.65%)\*7.65%),
so the maximum personal contribution rate over unadjusted net income is:

   20% \* (1-(1-7.65%)\*7.65%) = 18.587045%

which is documented in [Wikipedia][5], which says:

> the contribution limit for
> self-employed persons is more complicated; barring limits, it is
> 18.587045% (approximately 18.6%) of net profit

Now resolved the "complication". 

[1]: https://www.irs.gov/pub/irs-pdf/f1040sse.pdf
[2]: https://en.wikipedia.org/wiki/Taylor_series
[3]: https://www.irs.gov/retirement-plans/self-employed-individuals-calculating-your-own-retirement-plan-contribution-and-deduction
[4]: https://www.irs.gov/publications/p560/ch05.html
[5]: https://en.wikipedia.org/wiki/SEP-IRA
