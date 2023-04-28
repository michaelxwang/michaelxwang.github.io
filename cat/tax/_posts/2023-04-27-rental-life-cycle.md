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

- Depreciation: The process of recovering the cost of the rental property over 27.5 years. Only the building, not the land, can be depreciated.
- Capital gain: The profit earned when real estate is sold for a higher price than its original purchase cost.
- Section 1250 gain: The recapture of the depreciation taken, taxed at a higher rate (up to 25%) compared to regular long-term capital gains.

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
- Total interest paid on the mortgage over the first 10 years: Approximately $72,260 (from the mortgage amortization schedule at the end of this post)
- Annual depreciation: $19,000 / 27.5 x 10 = $69,091
- Total deductible expenses (operating expenses + depreciation + mortgage interest): $89,000 + $72,260 + $69,091 = $230,350
- Accumulated rental losses over the 10-year period (deductible expenses - rental income): $230,350 - $180,000 = $50,350

## 3. Sale

After 10 years, the investor sells the property:

- Sale price: $350,000
- Long term capital gain = $350,000 - $250,000 (purchase price) = $100,000
- Depreciation recapture ("Section 1250 gain"): $69,091
- Capital gains tax (15%): $100,000 x 0.15 = $15,000
- Section 1250 gain tax (25%): $69,091 x 0.25 = $17,273
- Accumulated rental losses = ($50,350)
- Tax on accumulated rental losses = ($50,350) * 0.32 = ($16,112)
- Total cash collected: $350,000 (sale price) + $180,000 (rental income) = $530,000
- Total cash paid: $250,000 (purchase price) + $89,000 (operating expenses) + $72,260 (interest paid) + $15,000 + $17,273 + ($16,112) (taxes paid) = $427,421
- Net profit = $530,000 - $427,421 = $102,579

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

PS: The first 10 years of principal and interest paid for a loan of 200,000 at 4% annual rate.

| Year | Principal Paid | Interest Paid | Remaining Balance | Principal Running Total | Interest Running Total |
|-----:|---------------:|--------------:|------------------:|------------------------:|-----------------------:|
| 1    | $3,404.84      | $7,951.16      | $196,595.16       | $3,404.84               | $7,951.16              |
| 2    | $3,547.33      | $7,808.67      | $193,047.83       | $6,952.17               | $15,759.83             |
| 3    | $3,696.29      | $7,659.71      | $189,351.54       | $10,648.46              | $23,419.54             |
| 4    | $3,852.02      | $7,503.98      | $185,499.52       | $14,500.48              | $30,923.52             |
| 5    | $4,014.80      | $7,341.20      | $181,484.72       | $18,515.28              | $38,264.72             |
| 6    | $4,184.95      | $7,171.05      | $177,299.77       | $22,700.23              | $45,435.77             |
| 7    | $4,362.78      | $6,993.22      | $172,937.00       | $27,063.01              | $52,429.00             |
| 8    | $4,548.63      | $6,807.37      | $168,388.36       | $31,611.64              | $59,236.36             |
| 9    | $4,742.82      | $6,613.18      | $163,645.54       | $36,354.46              | $65,849.54             |
| 10   | $4,945.72      | $6,410.28      | $158,699.82       | $41,300.18              | $72,259.82             |

[sale]: https://taxandlife.com/cat/tax/2018/11/25/sale-of-rental-home.html
