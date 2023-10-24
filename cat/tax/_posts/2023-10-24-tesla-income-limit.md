---
layout: post
title: Income limit on clean vehicle credit
categories:
  - tax
---

Many people are confused by the income limitation for the clean vehicle credit.
To clarify this, let's delve into the primary source.

According to the Internal Revenue Code (IRC) [30D(a)][irc]{:target="_blank"}:

> Allowance of credit. There shall be allowed as a credit against the tax imposed
> by this chapter for the taxable year an amount equal to the sum of the credit
> amounts determined under subsection (b) with respect to each new clean vehicle
> placed in service by the taxpayer during the taxable year.

At first glance, this suggests that a credit should be permitted. However, one
should be cautious, as specific rules come into play later. As per IRC
[30D(f)(10)(A)][irc]{:target="_blank"}:

> (A) In general. No credit shall be allowed under subsection (a) for any taxable year if --\
> (i) the lesser of --\
> (I) the modified adjusted gross income of the taxpayer for such taxable year, or\
> (II) the modified adjusted gross income of the taxpayer for the preceding taxable year, exceeds\
> (ii) the threshold amount.

These two sections of verbose code can be transcribed as:

```
credit_allowed = True

if min(income_current_year, income_prior_year) > threshhold:
    credit_allowed = False
```

or succinctly expressed as:

```python
credit_allowed = min(income_current_year, income_prior_year) <= threshhold
```

In simpler terms, if your income in the current year _or the prior year_ is
below a specified threshold, then you qualify for the clean vehicle credit.

The threshold values are detailed in IRC [30D(f)(10)(B)][irc]{:target="_blank"}:

> Threshold amount. For purposes of subparagraph (A)(ii), the threshold amount shall be --\
> (i) in the case of a joint return or a surviving spouse (as defined in section 2(a)), $300,000,\
> (ii) in the case of a head of household (as defined in section 2(b)), $225,000, and\
> (iii) in the case of a taxpayer not described in clause (i) or (ii), $150,000.

This can be concisely represented as:

```python
thresholds = {
    "joint": 300_000,
    "head of household": 225_000,
    "other status": 150_000
}
```

IRC [30D(f)(10)(C\)][irc]{:target="_blank"} elaborates on the definition of "income" in relation
to the clean vehicle credit:

> (C\) Modified adjusted gross income. For purposes of this paragraph, the term
> "modified adjusted gross income" means adjusted gross income increased by any
> amount excluded from gross income under section 911, 931, or 933.

Essentially, this refers to your adjusted gross income (AGI) unless specific
modifications are applied. For instance, if you have a foreign earned income
exclusion, this exclusion should be added back for the clean vehicle credit
evaluation.

It's also crucial to note that the credit is "nonrefundable". This means it can
only reduce your tax liability for the year. Whether you owe tax or receive a
refund on your tax return is immaterial. For a detailed explanation of
"refundable" and "nonrefundable", please refer to [this post][refundable]{:target="_blank"}.

By the way, the clean vehicle credit is applicable to citizens, resident
aliens, and nonresident aliens who file Form 1040-NR. The law doesn't specify
any limitations based on residency status, and [Form 8936][form8936]{:target="_blank"} clearly
includes Form 1040-NR.

Additionally, IRC [30D(a)][irc]{:target="_blank"} specifies _each new clean vehicle_. This means
if you purchase N clean vehicles, you are eligible for N credits.

[irc]: https://www.taxnotes.com/research/federal/usc26/30D
[refundable]: https://taxandlife.com/cat/tax/2023/02/08/refundable.html
[form8936]: https://www.irs.gov/pub/irs-pdf/f8936.pdf
