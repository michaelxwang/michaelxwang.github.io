---
layout: post
title: Maximum ISO spread without triggering AMT tax
categories:
- tax
---

When exercising Incentive Stock Options (ISO), taxpayers may become subject to
the Alternative Minimum Tax (AMT). The AMT is a parallel tax system designed to
ensure that taxpayers who benefit from certain deductions or exclusions still
pay a minimum amount of tax.

This tutorial will guide you through:

- How the AMT tax works when exercising ISOs.
- How to calculate the maximum ISO spread (the difference between the market price and exercise price) without triggering AMT.
  This becomes important when you have a choice of how much ISO's to exercise.

#### How AMT Tax is Computed

Based on IRS Form 6251, under "normal" conditions the AMT tax is calculated as:

AMT tax = ( Gross income + AMT income (ISO spread) - AMT exemption ) * 26%

Where:

- Gross Income: The taxpayer's regular taxable income.
- ISO Spread: The difference between the market value of the stock at exercise and the exercise price (considered as income for AMT purposes).
- AMT Exemption: A fixed amount that shields some income from AMT. This exemption phases out at higher income levels.
- 26% Tax Rate: This is the lower AMT rate applied to income below the AMT threshold.

The AMT only applies if the calculated AMT tax exceeds the regular tax.

#### Finding the Maximum ISO Spread Without Triggering AMT

To avoid AMT, the AMT tax must be less than or equal to the Regular Tax. The maximum ISO Spread is determined by setting AMT tax equal to Regular Tax, i.e.:

( Gross Income + ISO Spread − AMT Exemption) × 26% = Regular Tax

To solve the equation, we follow these steps:

- Estimate your Gross Income for the year.
- Estimate the Regular Tax by using [this spreadsheet][spreadsheet]{:target="_blank"}.
- Find the AMT Exemption from the [Form 6251][form6251]{:target="_blank"} for the year.
- Solve the equation.

Let us work out a concrete example:

- In 2021, you was single, and your gross income was $150,000.
- The Regular Tax on this income was calculated as $27,009 using [the spreadsheet][spreadsheet]{:target="_blank"}.
- The AMT Exemption for single status in 2021 was $73,600 based on [2021 Form 6251][form6251-2021]{:target="_blank"}.
- Solving the equation (150000 + ISO Spread - 73600)*26% = 27009, we have the max ISO Spread we can have without triggering AMT was $27,481.
- If your company offers you $0.07 for a share worth of $0.74, the corresponding number of shares you can exercise is: $ 27481/(0.74-0.07) = 41016 $.

PS: A Python program to automate the calculation for the year 2021 is copied below.

```
""" To calculate taxable income and max AMT income (ISO spead) without triggering AMT tax with the following limitations:
    - single and married filing jointly status only
    - standard deduction
    - income is less than 523,600 (single) and 1,047,200 (married)
    - 2021 tax table
"""

import argparse


class Tax:
    """ To calculate regular tax and max AMT income without AMT tax """

    def __init__(self):
        self.table = {}
        self.deduct = {}
        self.amt_exemption = {}

        self.table["single"] = [
            [0, 9950, 10.00, 0.00],
            [9951, 40525, 12.00, 199.00],
            [40526, 86375, 22.00, 4251.50],
            [86376, 164925, 24.00, 5979.00],
            [164926, 209425, 32.00, 19173.00],
            [209426, 523600, 35.00, 25455.75],
            [523601, 999999, 37.00, 35927.75],
        ]

        self.deduct["single"] = 12550
        self.amt_exemption["single"] = 73600

        self.table["mfj"] = [
            [0, 19900, 10.00, 0.00],
            [19901, 81050, 12.00, 398.00],
            [81051, 172750, 22.00, 8503.00],
            [172751, 329850, 24.00, 11958.00],
            [329851, 418850, 32.00, 38346.00],
            [418851, 628300, 35.00, 50911.50],
            [628301, 999999, 37.00, 63477.50],
        ]

        self.deduct["mfj"] = 25100
        self.amt_exemption["mfj"] = 114600
        self.tax = 0.0
        self.max_amt_income = 0.0

        parser = argparse.ArgumentParser()

        parser.add_argument("--income", type=float)
        parser.add_argument("--status", type=str, help="filing statuses: mfj, single")

        args = parser.parse_args()
        self.income = args.income
        self.status = args.status

    def compute_tax(self):
        """ To calculate regular tax """

        taxable_income = self.income - self.deduct[self.status]

        for bracket in self.table[self.status]:
            bracket_start = bracket[0]
            if taxable_income >= bracket_start:
                percent = bracket[2]
                adjustment = bracket[3]

        self.tax = round(taxable_income * percent / 100 - adjustment, 0)

    def compute_amt(self):
        """ To calculate max AMT income allowed  """
        self.max_amt_income = round(self.tax / 0.26 + self.amt_exemption[self.status] - self.income, 0)


if __name__ == "__main__":

    obj = Tax()
    obj.compute_tax()
    obj.compute_amt()
    print(f"regular tax is {obj.tax}.")
    print(f"max amt income without triggering amt tax is {obj.max_amt_income}.")
```

[spreadsheet]: https://docs.google.com/spreadsheets/d/1BnjUtb6ul_p62k2YEdBXcjHWvZunSVw0Y2E3BqTKao0
[form6251]: https://www.irs.gov/pub/irs-pdf/f6251.pdf
[form6251-2021]: https://www.irs.gov/pub/irs-prior/f6251--2021.pdf
