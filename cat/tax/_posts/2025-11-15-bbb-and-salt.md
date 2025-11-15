---
layout: post
title: One Big Beautiful Bill and State And Local Taxes
categories:
- tax
---
<!-- 大而美法案对州税及地方税扣除额上限的调整 -->

The Tax Cuts and Jobs Act (TCJA) established an annual $10,000
deduction cap for state and local taxes (SALT) from tax years 2018
through 2025 (inclusive). The One Big Beautiful
Bill Act (OBBBA), however, modifies the cap beginning with the 2025
tax year.

For the year 2025, the new SALT cap ($$y$$), as a function of Modified Adjusted Gross Income or MAGI ($$x$$),
can be expressed by:

$$
y = 
\begin{cases}
\$40,000 & :\ \$000{,}000 \leq x \lt \$500{,}000 \\
\$40,000 - 0.3(x - \$500{,}000) & :\ \$500{,}000 \leq x \lt \$600{,}000 \\
\$10,000 & :\ \$600{,}000 \leq x \lt \$\infty
\end{cases}
$$

where:

- $40,000 is the base SALT cap for 2025 (except married filing separately, which is $20,000), which increases by 1% annually through 2029.
- $500,000 is the MAGI Threshold for 2025, also subject to the annual 1% increase.

This formula can be visualized as follows:

<img src="/assets/images/20251115-obbba-salt.png" alt="SALT cap as a function of income" width=700 height=400/>

For 2025, you may claim either the standard deduction or (if larger) your itemized deductions. The standard deduction amounts by filing status are:

- $15,750 for Single or Married Filing Separately
- $23,625 for Head of Household
- $31,500 for Married Filing Jointly or Qualifying Surviving Spouse

Typical itemized deduction items include:

- SALT (subject to the new limitation)
- Mortgage interest on loans up to \$750,000 principal
- Charitable donations

Raising the SALT cap under OBBBA will increase the number of filers
who benefit from itemizing their deductions, especially for those
in high-tax states.

This summary is based on the [Pull Request, aka House Bill](https://www.congress.gov/bill/119th-congress/house-bill/1/text){:target="_blank"}:

>SEC. 70120. LIMITATION ON INDIVIDUAL DEDUCTIONS FOR CERTAIN STATE AND LOCAL TAXES, ETC.<br>
>(a) In General.—Section 164(b)(6) is amended—<br>
>(1) by striking “and before January 1, 2026”, and<br>
>(2) by striking “$10,000 ($5,000 in the case of a married individual filing a separate return)” and inserting “the applicable limitation amount (half the applicable limitation amount in the case of a married individual filing a separate return)”.<br>
>...<br>

which merges into [IRC §164](https://www.taxnotes.com/research/federal/usc26/164){:target="_blank"}.
