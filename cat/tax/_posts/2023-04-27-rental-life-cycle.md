---
layout: post
title: A sample analysis of rental property investment life cycle
categories:
- tax
---

## 0. Introduction

Investing in rental property can be a viable long-term investment strategy. By
purchasing a property and renting it out, investors can earn passive income
from rental payments and potentially profit from the property's appreciation
over time.

In this analysis, we'll examine a hypothetical rental property investment over
a 10-year period, which includes:

- The property's purchase,
- The rental operations, and
- The eventual sale of the property.

We assume that the investor cannot take the rental loss annually due to high income and can only offset it upon sale against ordinary income at their 32% tax bracket.

Before delving into the complex calculations, let's clarify some key concepts:

- Depreciation: The process of recovering the cost of the rental property over
  27.5 years. Only the building, not the land, can be depreciated.
- Capital gain: The profit earned when real estate is sold for a higher price
  than its original purchase cost. Long term (more than one year) capital gain
  is taxed at 0%, 15%, and maximum 20% depending on your tax bracket, and 
  the short term capital gain is taxed as your ordinary income.
- Section 1250 gain: When a property is sold for more than its original cost
  minus depreciation, the depreciation that was allowed or allowable will be
  added back as taxable income regardless whether took the depreciation or not.
  This depreciation recapture is called "section 1250 gain", taxed at a higher
  rate (up to 25%) compared to regular long-term capital gains.

A picture is worth a thousand words. The best way to understand those concepts is to look at the pictures in [my other post][sale]{:target="_blank"}.

## 1. Purchase

- Purchase price: $250,000
- Down payment (20%): $50,000
- Mortgage amount: $200,000 (30-year fixed at 4%)
- Building value = $190,000
- Land value = $60,000

## 2. Rental Operations

During the 10-year rental period, the investor experiences the following:

- Gross annual rental income: $18,000 x 10 = $180,000
- Total annual operating expenses (excluding depreciation): $8,900 x 10 = $89,000
- Total interest paid on the mortgage over the first 10 years: Approximately $72,148 (from the mortgage amortization schedule at the end of this post)
- Annual depreciation: $190,000 / 27.5 x 10 = $69,091
- Total deductible expenses (operating expenses + depreciation + mortgage interest): $89,000 + $72,148 + $69,091 = $230,239
- Accumulated rental losses over the 10-year period (deductible expenses - rental income): $230,239 - $180,000 = $50,239

## 3. Sale

After 10 years, the investor sells the property:

- Sale price: $350,000
- Long term capital gain = $350,000 - $250,000 (purchase price) = $100,000
- Depreciation recapture ("Section 1250 gain"): $69,091
- Capital gains tax (15%): $100,000 x 0.15 = $15,000
- Section 1250 gain tax (25%): $69,091 x 0.25 = $17,273
- Accumulated rental losses = ($50,239)
- Tax on accumulated rental losses = ($50,239) * 0.32 = ($16,076)
- Total cash collected: $350,000 (sale price) + $180,000 (rental income) = $530,000
- Total cash paid: $250,000 (purchase price) + $89,000 (operating expenses) + $72,148 (interest paid) + $15,000 + $17,273 + ($16,076) (taxes paid) = $427,345
- Net profit = $530,000 - $427,421 = $102,655

## 4. Summary

The tax theory surrounding rental properties is complex, and calculating the
associated taxes can be complicated. However, don't get overwhelmed by the
numbers. Let's simplify the situation to better understand the core concept.

Let's assume the following:

- The rent collected and cash expenses (operating expenses + interest payments) offset each other, so the rental loss results solely from depreciation; and
- The rental property's value remains unchanged after 10 years.

In this scenario, you don't have any capital gains. All you have is
depreciation recapture, taxed at a rate of 25% or your tax bracket, whichever
is lower. At the same time, you have an equal amount of rental loss, which is
also taxed at your tax bracket. As a result, you either break even or come out
slightly ahead, depending on your tax bracket. Any improvement in cash flow
during the rental operations or capital appreciation will further enhance your
financial position.

## PS: Mortgage calculator

When calculating principal and interest paid for a loan, you'll need to use the
amortization formula. The amortization formula calculates the monthly payment
`(M)` for a fixed-rate loan, given the loan amount `(P)`, the interest rate per
period `(r)`, and the number of payment periods `(n)`. Here's the formula:

M = P * (r * (1 + r)^n) / ((1 + r)^n - 1)

Where:
- M is the monthly payment
- P is the loan principal (the initial amount borrowed)
- r is the periodic interest rate (annual interest rate divided by the number of payment periods per year, e.g., 12 for monthly payments)
- n is the total number of payment periods (loan term in years multiplied by the number of payment periods per year)

After calculating the monthly payment (M), you can determine the interest and principal paid for each payment period. For each payment, the interest paid `(I)` is calculated as follows:

I = P_remaining * r

Where:

- I is the interest paid for that payment period
- P_remaining is the remaining principal balance before that payment

The principal paid `(P_paid)` for that payment period can be calculated as follows:

P_paid = M - I

Where:

- P_paid is the principal paid for that payment period
- M is the monthly payment
- I is the interest paid for that payment period

By repeating this process for each payment period, you can determine the principal and interest paid over the life of the loan.

Applying above algorith to a loan of $200,000 over 30 years at 4% annual rate, we have:

- Loan amount (P): $200,000
- Annual interest rate: 4% = 0.04
- Periodic interest rate (r): 0.04 / 12
- Number of payment periods (n): 30 years * 12 = 360
- Monthly payment (M) = $200,000 * ((0.04 / 12) * (1 + (0.04 / 12))^360) / ((1 + (0.04 / 12))^360 - 1) ≈ $954.83
- Total interest paid = ($954.83 * 360) - $200,000 ≈ $143,738.80
- Total cost of loan = $954.83 * 360 ≈ $343,738.80

The first 10 years of accumulated principal, interest, and remaining balance are tabulated below using above formula.
If you are not interested to calculate yourself, you can also find calculators online.

| Year | Principal Paid | Accumulated Interest Paid | Remaining Balance |
|:----:|---------------:|--------------------------:|------------------:|
|  1   |     $3,522.07  |            $7,935.89      |    $196,477.93    |
|  2   |     $7,187.64  |            $15,728.29     |    $192,812.36    |
|  3   |     $11,002.55 |            $23,371.35     |    $188,997.45    |
|  4   |     $14,972.88 |            $30,858.99     |    $185,027.12    |
|  5   |     $19,104.97 |            $38,184.86     |    $180,895.03    |
|  6   |     $23,405.41 |            $45,342.39     |    $176,594.59    |
|  7   |     $27,881.06 |            $52,324.71     |    $172,118.94    |
|  8   |     $32,539.05 |            $59,124.69     |    $167,460.95    |
|  9   |     $37,386.81 |            $65,734.89     |    $162,613.19    |
| 10   |     $42,432.08 |            $72,147.59     |    $157,567.92    |

[sale]: https://taxandlife.com/cat/tax/2018/11/25/sale-of-rental-home.html
