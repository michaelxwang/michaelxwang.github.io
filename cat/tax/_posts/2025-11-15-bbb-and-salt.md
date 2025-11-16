---
layout: post
title: One Big Beautiful Bill & State And Local Taxes
categories:
- tax
---

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

- $40,000 is the base SALT cap for 2025 (except married filing separately, which is $20,000), which increases by 1% annually through 2029. The SALT cap will revert to $10,000 starting with the 2030 tax year.
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

This summary is based on the [Pull Request, aka House Bill][pr]{:target="_blank"}:

>SEC. 70120. LIMITATION ON INDIVIDUAL DEDUCTIONS FOR CERTAIN STATE AND LOCAL TAXES, ETC.<br>
>(a) In General.—Section 164(b)(6) is amended—<br>
>(1) by striking “and before January 1, 2026”, and<br>
>(2) by striking “$10,000 ($5,000 in the case of a married individual filing a separate return)” and inserting “the applicable limitation amount (half the applicable limitation amount in the case of a married individual filing a separate return)”.<br>
>...<br>

which merges into [IRC §164][irc]{:target="_blank"}.

<!--
下面是中文翻译：

《减税与就业法案》（Tax Cut and Job Act, TCJA）自 2018 至 2025 纳税年度（含）设定了每年 $10,000 的州税及地方税 (SALT) 抵扣上限。而《大美丽法案》（One Big Beautiful Bill Act, OBBBA）自 2025 年起对该上限进行了调整。

2025 年的新 SALT 抵扣上限 ($y$) 可表示为修改后总收入 (MAGI, $x$) 的函数，具体公式如下：

$$
y = 
\begin{cases}
\$40,000 & :\ \$000{,}000 \leq x \lt \$500{,}000 \\
\$40,000 - 0.3(x - \$500{,}000) & :\ \$500{,}000 \leq x \lt \$600{,}000 \\
\$10,000 & :\ \$600{,}000 \leq x \lt \$\infty
\end{cases}
$$

其中：

- $40,000 为 2025 年 SALT 基本上限 (已婚单报为 $20,000) 2025 年起至 2029 年每年增加1%. SALT 抵扣上限将于 2030 纳税年度起恢复至 1 万美元。
- $500,000 为 2025 年 MAGI 门槛，同样每年递增 1%.

该公式可以通过下图直观展示：

<img src="/assets/images/20251115-obbba-salt.png" alt="SALT cap as a function of income" width=700 height=400/>

在 2025 年，您可以选择标准抵扣或逐项抵扣（如果更高的话）。2025 年不同申报状态的标准抵扣额为：

- 单身或已婚分别报税：$15,750
- 户主 (Head of Household) ：$23,625
- 已婚联合报税：$31,500

常见逐项抵扣项目包括：

- 州税及地方税（受新上限约束）
- 最高本金$750,000的猫给鸡利息
- 慈善捐赠

OBBBA 提升 SALT 扣除上限后，会让更多纳税人能够实质受益于逐项抵扣，特别是在高税州。

本简介基于国会[拉取请求（即众议院法案）][pr]{:target=”_blank”}：

>SEC. 70120. LIMITATION ON INDIVIDUAL DEDUCTIONS FOR CERTAIN STATE AND LOCAL TAXES, ETC.<br>
>(a) In General.—Section 164(b)(6) is amended—<br>
>(1) by striking “and before January 1, 2026”, and<br>
>(2) by striking “$10,000 ($5,000 in the case of a married individual filing a separate return)” and inserting “the applicable limitation amount (half the applicable limitation amount in the case of a married individual filing a separate return)”.<br>
>...<br>

以及最终并入的《美国国内税收法典》[第164条][irc]{:target=”_blank”}.
-->
[pr]: https://www.congress.gov/bill/119th-congress/house-bill/1/text
[irc]: https://www.taxnotes.com/research/federal/usc26/164
