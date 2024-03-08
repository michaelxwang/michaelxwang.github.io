---
layout: post
title: "Tax notes: ISO, ESPP, and RSU"
categories:
- tax
---

If you participate in an Incentive Stock Option (ISO), Employee Stock Purchase
Plan (ESPP), or have Restricted Stock Units (RSUs), there's a significant
chance you may have overpaid on your taxes. From my experience reviewing tax
returns, many that involve ISOs, ESPPs, or RSUs were not correctly filed.

This is crucial information if you hold ISOs, ESPPs, or RSUs, especially since
the IRS made significant changes to how the cost basis is reported on your Form
1099-B. This change took effect on January 1, 2014. It's essential to make the
necessary adjustments to avoid double taxation.

To clarify these issues, let's define some terms commonly used in this discussion.

Statutory and non-statutory plans represent two principal categories of equity awards granted to employees.

Statutory Plans: These comply with IRS criteria to qualify for special tax treatment.
Non-Statutory Plans: Also known as "non-qualified stock options" (NSOs or NQSOs), these do not meet the IRS criteria for special tax treatment and are subject to different tax regulations.

ISOs are an example of statutory plans. RSUs, however, are non-statutory plans.
ESPPs can be offered under either plan.

When you sell stocks under statutory plans, the sale can be classified
as either a qualifying disposition or a disqualifying disposition, based on the
holding period:

- Qualifying Disposition:
  - If sale_date - exercise_date > 1 year AND
  - sale_date - grant_date > 2 years
- Disqualifying Disposition:
  - If the above conditions are not met.

The terms "long term" and "short term" capital gains retain their standard definitions.

- Long Term Capital Gain:
  - If the holding period > 1 year, taxed at a reduced rate.
- Short Term Capital Gain:
  - If the holding period ≤ 1 year, taxed as ordinary income at the marginal rate.

It's possible to have a disqualifying disposition yet still qualify for long term capital gains.

- Ordinary Income: Income that is subject to income tax but not to FICA taxes (Social Security and Medicare taxes). Examples include bank interest and capital gains.
- Compensation: Income that is subject to both income tax and FICA taxes. An example of this would be your wages.
- Grant or offer: The employer's promise to grant you stock options.
- Vest or Exercise: The point at which the stock options or RSUs become yours.

Let us discuss some common forms of equity awards.

#### ISO

Only pay tax when sold.

- Qualifying disposition: Taxes are levied only on the long-term capital gain (or
loss), which is the difference between the sale price and the option purchase
price, and not as compensation.

- Disqualifying disposition: You pay ordinary income tax on the "bargain
element", the spread betwen market price and purchase price, but only up to the actual gain realized if the stock is
sold for more than the option purchase price.

> Example 1:
> 
> - Market price at grant: $100
> - Sale price: $90
> - Option purchase price: $70

The ordinary income (Box 1 of W-2) is $20 ($90 - $70, up to the gain), and
the capital gain is $0 (not to pay tax twice).

> Example 2:
> 
> - Sale price: $120
> - Market price at grant: $100
> - Option purchase price: $70

The ordinary income (Box 1 of W-2) is $30 ($100 - $70), and
the capital gain (long or short depending on holding period) on $20 ($120 - $100).

For both situations, the broker will report the option purchase price ($70) as cost basis,
you need to increase the cost basis to reflect the ordinary income realized, or you end
up paying tax twice.

#### ESPP

Same as ISO, you pay tax only when the stocks are sold for ESPP offered under a statutory plan.

- Qualifying Disposition: This occurs when the stock is sold at least two years
  after the grant date and more than one year after the stock was purchased.
  The tax treatment for a qualifying disposition involves taxing part of the gain
  as ordinary income and potentially part as capital gain.

> Example:
> 
> - FMV (Fair Market Value) at grant = 100
> - Sale price: 90
> - Purchase price (with discount, as if purchased at grant time): 85
 
Ordinary income is $90 - $85 = $5 (up to the gain), and the
capital gain is $0.

The broker will report that you have a $5 gain ($90 - $85), you
should increase your basis by $5 to derive $0 gain because the $5
has been reported as regular income on your W-2.

- Disqualifying disposition must realize ordinary income of bargain element
(FMV at exercise minus purchase price) at year of sale even there is a loss.
The cost basis is the purchase price plus the bargain element, ie, the
FMV value.

> Example:
> 
> - FMV at exercise = 100
> - Sale price: 90
> - Purchase price: 85
 
The ordinary income: 100 - 85 = 15, and the capital gain: 90 - 100 = -10.
 
The broker will report that you have a $5 gain ($90 - $85), you
should adjust your basis to reflect a $10 loss because the $15
has been reported as regular income on your W-2.

Some companies have a look-back provision to determine the purchase
price, so the purchase price could be much lower than the market
price, as a result of this the ordinary income could be much larger, and so
the adjustment on the basis. If you do not make adjustment, then
you are paying tax twice on this part of income, once as ordinary
income, and once as capital gain.

The following psudo code can help to visualize the logic:

```
IF qualified
  IF Sale price > Purchase price
    Ordinary income = Sale price - Purchase price
  ELSE
    Ordinary income = 0
ELSE
  Ordinary income = FMV at exercise - Purchase price

Capital gain = Sale price - (Purchase price + Ordinary income)
```

Since tax is higher or equal on ordinary income than capital gain, qualified disposition pays less or equal taxes
than disqualified disposition. When Sale price >= FMV at exercise, they converge.

Most people forget the Ordinary income in above formula in computing capital gain, they pay tax on Ordinary income twice, once as ordinary income
and once as capital gain.

#### RSU

RSU is non-statuary stock option. You do not pay tax when the stock
was granted, but you pay taxes when the stock was transferred to you
before you sell it. You pay tax on the benefit you get (market price
minus the purchase price) as _compensation_.

You can either transfer external money to pay for the taxes, but by default
they will sell some stocks to cover the tax.
If you do not sell enough stock to cover the taxes, and later the
stock becomes worthless, you may not have enough money to cover
the taxes.

> Example:
> 
> - Number of shares: 10
> - Purchase price: $0
> - Share price: $1,000

$10,000 ($1,000 * 100) will be taxed as ordinary income. Suppose 40%
of tax needs to be paid, then you need either to come up with
$4,000 to pay taxes from your pocket, you sell 4 shares
to cover the taxes ($1,000 * 4).

If you sell 4 shares to cover the taxes, then on your brokerage
form, it will show that you have a $4,000 capital again because
the purchase price is $0. However because the benefit of having the
stock for free has been added to your W-2 and taxed as
compensation, then you should increase your basis to $4,000 to
derive a $0 gain. Because of cost of sale, you should have a 
small loss. If you do not do this, then you will pay taxes
twice, once as compensation, and once as capital gain.

Suppose after many years, you want to sell the rest of 6 shares
and you forgot that you have paid taxes already up to $1,000 per share
and the company does not provide you with the proper paperwork, you will
end up paying taxes again.

Documents needed for the cost basis adjustment:

- Form 3921 from employer if you have ISO or RSU.
- Form 3922 from employer if you have sold stocks from ESPP.

Those are official forms, but I have seen supplemental document from
brokers to help you make adjustment for the cost basis.
