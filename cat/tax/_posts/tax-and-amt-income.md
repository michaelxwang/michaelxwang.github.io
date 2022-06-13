---
layout: post
title: Maximum AMT income (ISO spread) without triggering AMT tax
categories:
- tax
---

This program estimates regular tax based gross income and filing status under standard deduction, and
the maximum AMT income (ISO spread) without triggering AMT tax.

Based on Form 6251, under "normal" conditions the AMT tax is computed as:

( gross income + AMT income (ISO spread) - AMT exemption ) * 26%

So the max AMT income is obtained by solving the equation:

( gross income + AMT income (ISO spread) - AMT exemption ) * 26% = regular income

Since there is no analytical solution, the AMT income (ISO spread) can be computed by the following Python program. 

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
