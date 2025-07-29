---
layout: post
title: Excess HSA contribution
categories:
  - tax
---

Overcontributing to a Health Savings Account (HSA) can happen, typically when
you change jobs. This can happen if your new employer is not informed of the
contributions you've already made via your previous employer, provided their
payroll software has the capacity to accommodate this information. It's worth
noting that excess contributions to an HSA are unlikely with a single employer,
as the payroll software should automatically halt contributions once the
maximum limit is reached.

#### What to do if you overcontribute to an HSA

If you do overcontribute to an HSA, there are a few things you can do to
rectify the situation. Here are three options:

#### Option 1: Timely correction: treat spending as withdrawal

If you had spending from the HSA before the filing deadline (including extensions),
you can treat distributions as a withdrawal of the excess.

For timely correction, the IRS requires that you withdraw the excess contribution
plus earnings ("such distribution is accompanied by the amount of net income attributable
to such excess contribution." per [IRC Sec 223(f)(2)][irc223]{:target="_blank"}).

"If the excess contribution isn’t included in box 1 of Form W-2, you must
report the excess as “Other income” on your tax return." ([IRS Publication 969][p969]{:target="_blank"}).

You need also to pay tax on the earnings ("Any net income described
in clause (ii) shall be included in the gross income of the individual for the taxable
year in which it is received.", [IRC Sec 223(f)(2)][irc223]{:target="_blank"}).

However, you do not pay 6% excise tax as the excess contribution has been timely corrected.

Step by step instructions:

- Calculate the distribution plus earnings:
  - c = amount of the contribution.
  - b1 = balance after contribution.
  - b2 = balance before distribution.
  - e = excess contribution.
  - d = distribution = $$ e(1 + \frac{b2-b1}{c}) $$.
- Report the excess contribution and earnings withdrawn on Form 8889, line 14b (for tracking qualified medical expenses).
- Report the excess contribution (if not already included in W-2) and earnings (always) as "other income" on your tax return.
- Report the excess contribution withdrawn on Form 5329 to avoid the 6% excise tax.
<!--
"Instruction for Form 8889" page 6 under "Excess Employer Contributions":
"""If the excess was not included in income on Form W-2, you must report it as “Other income” on your tax return."""
-->

If you do not have enough spending to withdraw the excess contribution plus earnings, 
the excess is not considered as withdrawn, and you will need to follow option 2, 3, or 4.
The excess contribution is either corrected or not corrected, there is no partial correction.

#### Option 2: Timely correction: actual withdrawal

The process is the same as Option 1 except that you need to contact your HSA custodian
to have the excess plus earnings withdrawn. This is the most straightforward option,
but it may also be the most time-consuming, and sometimes costly as some HSA custodians
charge a fee for the service.

#### Option 3: Untimely correction - Rollover to next year

If you have missed the chance, or simply do not want to go through the trouble of contacting the HSA custodian,
another option is to simply let the excess stay in your account for the current
year, pay a 6% penalty, and treat it as part of your contribution for the next
year. Be sure to adjust your next year's contribution amount so that the total
does not exceed the limit<sup>[1](#fn1)</sup>.

Note: You will also need to add the excess contribution (excluding earnings) to your
current year's income. You can then deduct the excess in the following year, up
to the amount that fits the maximum limit.

For example, let's say you contribute $3,950 to your HSA in 2023, but the
maximum contribution limit is $3,850. You would have $100 of excess
contributions. If you choose to rollover this amount to the next year, you would pay a 6%
excise tax on the excess, which is $6. You would then add the $100 to your 2023 income. In 2024, you could deduct $100 from your
taxable income.

Step by step instructions:

- Let the excess contributions stay in your HSA account.
- Pay a 6% penalty on the excess contributions.
- Add the excess contributions (excluding earnings) to your current year's income.
- Adjust your next year's contribution amount so that the total does not exceed the limit.
- Deduct the excess contributions in the following year, up to the amount that fits the maximum limit.

#### Option 4: Untimely correction - Actual withdrawal

If you have discovered the errors late, and cannot withdraw the excess contribution by spending it out,
you can always contact your HSA custodian to withdraw the excess.

You will pay 6% excise tax on the excess contribution that remained on the account
"as of the close of the taxable year" ([IRC Section 4973(a)][irc4973]{:target="_blank"}), that is
December 31st, not the tax filing deadline for untimely correction.

You will also need to pay regular tax on the excess contribution if not included in W-2 (excluding earnings)
for the year of the contribution.

#### Which option is right for you?

The answer is neither. The best option is not to have an excess contribution, but things happen, so I hope
this post provides information to allow you to make a decision that can minimize your cost in
both of time and dollars.

PS: 

When the contributions were initially _allowed_ when made (you were eligible), 
but later become ineligible under the testing period rule,
these are not "excess contributions" - they were proper 
contributions at the time, but now must be included in income due to loss of 
eligibility. Unlike excess contributions, these amounts do not need to be removed 
from the HSA - they only need to be added to income.

#### Footnotes:

<a name="fn1">1</a> [IRS Publication 969][p969] states: 
>You may be able to deduct excess contributions for previous years that are still in 
your HSA. The excess contribution you can deduct for the current year is the lesser of:
- (1) Your maximum HSA contribution limit for the year minus any amounts 
contributed to your HSA for the year, or
- (2) The total excess contributions in your HSA at the beginning of the year.

References:

1. [Instructions][i8889]{:target="_blank"} for Form 8889.
2. [Instructions][i5329]{:target="_blank"} for Form 5329.
3. [Publication 969][p969]{:target="_blank"} - Health Savings Accounts and Other Tax-Favored Health Plans.
4. [IRC Section 223][irc223]{:target="_blank"}.
5. [IRC Section 4973][irc4973]{:target="_blank"}.

[f5329]: https://www.irs.gov/pub/irs-pdf/f5329.pdf
[f8889]: https://www.irs.gov/pub/irs-pdf/f8889.pdf
[i5329]: https://www.irs.gov/pub/irs-pdf/i5329.pdf
[i8889]: https://www.irs.gov/pub/irs-pdf/i8889.pdf
[p969]: https://www.irs.gov/pub/irs-pdf/p969.pdf
[irc223]: https://www.taxnotes.com/research/federal/usc26/223
[irc4973]: https://www.law.cornell.edu/uscode/text/26/4973
