---
layout: post
title: "Tax notes: ISO, ESPP, and RSU"
categories:
- tax
---

If you have Incentive Stock Options (ISO), Employee Stock Purchase Plan (ESPP),
and Restricted Stock Unit (RSU), then most likely than not, you have overpaid
your taxes. Among the tax returns that I have reviewed, many returns involving
ISO, ESPP, or RSU were not done correctly.

If you have ISO, ESPP, or RSU, you should read this because effective
January 1st 2014, the IRS changed how cost basis is reported on your 1099-B
tax form sent to you by your broker. You should make adjustment in order not
to pay your tax twice.

In order to explain the problems, we need to define some terms used in the discussion.

The following are the common example of stock options and the categories they belong:

- Statutory stock option
  - Incentive Stock Options (ISO)
  - Employee Stock Purchase Plan (ESPP)
- Non-statutory stock option
  - Restricted Stock Unit (RSU)

When you sell the stock options, it can be either qualifying disposition or
disqualifying disposition depending on the holding period:

```
IF sale_date - exercise_date > 1 year AND
   sale_date - offer_date    > 2 years
THEN
   It is "qualifying disposition"
ELSE
   It is "disqualifying disposition"
```

Long term and short term capital gain have their normal definition:

```
IF holding period > 1 year
THEN
   It is long term capital gain and
   you pay tax at reduced rate
ELSE
   It is short term capital gain and
   you pay tax as "ordinary income" at the marginal rate
```

So you could have a disqualifying disposition but long term capital gain.

Ordinary income: Income subject to income tax only, but not
FICA tax (social security tax and medicare tax). Example:
bank interest, capital gain.

Compensation: income not only subject to income tax, but also
FICA tax. Example, your wage.

Offer: the employer promised to give you stocks.

Grant, exercise: the stocks became yours.

#### ISO

Only pay tax when sold.

Qualifying disposition: only pays tax as long term capital gain (or loss) based on
sale price and the option purchase price, not as compensation.

Disqualifying disposition: pay tax as ordinary income up to your gain.

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

Same as ISO, you pay tax only when the stocks are sold.

-- Qualifying disposition realizes ordinary income up to the gain.

> Example:
> 
> - FMV at exercise = 100
> - Sale price: 90
> - Purchase price: 85
 
Ordinary income is $90 - $85 = $5 (up to the gain), and the
capital gain is $0.

The broker will report that you have a $5 gain ($90 - $85), you
should increase your basis by $5 to derive $0 gain because the $5
has been reported as regular income on your W-2.

-- Disqualifying disposition must realize ordinary income of bargain element
(FMV at grant minus purchase price) at year of sale even there is a loss.
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
  IF Sale price >= Purchase price
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
