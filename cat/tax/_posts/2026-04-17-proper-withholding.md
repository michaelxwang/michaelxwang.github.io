---
layout: post
title: The Ultimate Guide to Proper Tax Withholding (W-4, RSUs, and Investments)
categories:
- tax
---

Most people's income consists of three components:

- Base salary
- Supplemental income (RSU, bonuses)
- Investment income (interest, dividends, capital gains from stock sales)

Let us discuss how to deal with each component properly.

### Base salary

- Single

If you are single and have one job, checking "Single" on your W-4 through your
company's self-help app usually results in perfect withholding.

- Married

Happily married people are often eager to check the "Married filing jointly"
box on their W-4. However, this often leads to a massive tax surprise.

If you check "Married" but don't account for your spouse's income, your
employer assumes you are the sole breadwinner. They apply the full married
standard deduction, and withhold using the lower tax rate based on your married
status. When your spouse also has income, the math breaks, leaving you owing a
large amount in April.

The standard approach is to use the extra withholding tables in the W-4
appendix, but that method caps out if the lower-earning spouse makes more than
$120,000.

There is a highly effective workaround: each spouse should check "Single or
Married filing separately" on their W-4. When two spouses have similar incomes,
married filing jointly will result in about the same tax as filing separately
(see this [post][separate]{:target="_blank"} for a detailed analysis). So, if
each spouse takes care of their own taxes via their W-4, when you actually file
jointly, you will have the proper tax paid.

By using this strategy, your withholdings will automatically scale correctly as
your salaries grow, so you do not need to rebalance your withholding annually.

- Multiple jobs

For both single and married taxpayers, you are at high risk of underpayment if
you change jobs or have multiple concurrent jobs. Neither employer knows about
the other, so they both apply your standard deduction and lower tax brackets,
resulting in significant under-withholding. Please refer to [this post][two jobs]{:target="_blank"}
for a math model. In this case, I would recommend using
the 100% / 110% [safe harbor rule][safe harbor]{:target="_blank"} to avoid an
underpayment penalty.

### Supplemental income (RSU, bonuses)

The default federal withholding rate for supplemental wages -- like annual
bonuses, stock vesting, and commissions -- is a flat 22%.

For high-income earners, this 22% rate is a trap. By the time your supplemental
income hits, your combined income might already place you in the 24%, 32%, 35%,
or even 37% tax bracket. This gap creates an instant underpayment penalty risk.

**The Fix:** If your employer allows it, request that supplemental income be
withheld at your top marginal tax bracket. Please refer to page 2 of your
prior-year tax return PDF file to check your tax bracket as a guide.

In the case of RSUs, that means increasing the "sell to cover" rate. By selling
more shares at your tax bracket rate, you ensure you do not owe taxes, which
protects you in the case the share price drops. If the share price rises, you
still have unsold shares to take advantage of market appreciation. This
approach prevents you from losing a lot of money if the stock market crashes,
and also ensures you are getting some profit if the stock goes well. 

For more information on RSU withholding, please refer to [this post][rsu]{:target="_blank"}.

### Investment income (interest, dividends, and capital gains from stocks)

Investment income usually has zero taxes withheld upfront, so if you have a
large sum of income from investments, you may owe a significant amount of taxes
at tax time.

The best approach is to have this part of your taxes paid via your payroll
withholding. The tax rate on ordinary income (interest, nonqualified dividends)
is your tax bracket plus the 3.8% Net Investment Income Tax (NIIT), and the tax
on long-term capital gains is capped at 23.8% (20% plus the 3.8% NIIT). 

If you have a large investment income at the end of the year, and the payroll
withholding isn't enough, you can make an estimated payment for the quarter in
which you have the income. However, this may require us to file an Annualized
Income schedule, which is rather complicated; it is like doing 4 additional
quarterly returns inside an annual return.

The mechanics to withhold more tax through payroll withholding are explained
[in this post][safe harbor]{:target="_blank"}.

After you take care of the withholdings for each category of your income, you
will have a balanced budget and the April pain is removed. Wish you many happy
returns!

[separate]: /cat/tax/2023/04/26/separate-or-joint-en.html
[safe harbor]: /cat/tax/math/2018/07/21/irs-estimated-payment-penalty.html
[two jobs]: /cat/tax/2018/06/24/change-jobs-n-tax-owed.html
[rsu]: /cat/tax/2023/04/27/rsu-tax-en.html
