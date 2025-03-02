---
layout: post
title: Backdoor Roth IRA
categories:
- tax
---

<img src="/assets/images/20210105-basic-backdoor-Roth-IRA.jpg">

We hold these truths to be self-evident: everyone can contribute to a
traditional IRA, even Bill Gates, if he likes. It is merely a matter of how
much one can deduct from their income - zero, partial, or the full amount.

On the other hand, contributions to the Roth IRA are limited by income with phaseouts:

- $218,000 (Y2023) for Married Filing Jointly, Qualifying Widow(er) with Dependent Child
- $138,000 (Y2023) for Single, Head of Household
- $000,000 (Y2023) for Married Filing Separately (living with spouse)

However, everyone can convert to a Roth IRA from a traditional IRA, even Bill
Gates, if he likes. It is just a matter of whether it is done through the
"front door" (direct contribution) or the "back door" (conversion). You can
also go through the back door while the front door is open to you.

How do you contribute to ROTH IRA via "back door"? Here is the run book:

0. Make sure you do not have tradition IRA without basis [or a rollover IRA from 401(k)] or get rid of it (see footnote).
1. You contribute to traditional IRA in the amount X.
2. You convert the full amount to ROTH IRA at earliest possible time when the fund is available _without paying withholding tax_.
3. Provide (a) the contribution and (b) distribution information to your accountant or your tax software.

Here is what you will see on your tax form when it is done right:

- You report the deductible amount Y (0 <= Y <= X) in the year where the contribution is allocated.
- You report the income amount Y in the year where the conversion is made.

The deduction and income cancels each other, and the end result is that you have contributed X to ROTH IRA.

Example:

- On 2019-04-01 you contributed $5,500 to traditional IRA allocated to 2018,
- On 2019-04-01 you contributed $6,000 to traditional IRA allocated to 2019,
- On 2019-04-03 you converted the full amount $11,500 to ROTH IRA.

Here is how you report:

- On your 2018 form 1040, you report deduction Y1 between $0 and $5,500.
- On your 2019 form 1040, you report deduction Y2 between $0 and $6,000 and income Y1 + Y2 between $0 and $11,500.

If your income level does not allows you to deduct or or you choose not to deduct, then Y1 = Y2 = 0.

Footnote:

- The contribution is reported on [Form
5498](https://www.irs.gov/pub/irs-pdf/f5498.pdf), but this form is
typically received after the tax filing deadline. This delay occurs
because the deadline for contributions coincides with the filing
deadline, preventing the form from being finalized until after this
date. Consequently, it is crucial to **provide your own record**
of the contribution amount, date, and the allocated year to your accountant.

- The distribution is in [Form
1099-R](https://www.irs.gov/pub/irs-pdf/f1099r.pdf) and it will
come before the deadline. The distribution code should be 02 (early
distribution but exception applies).

- If you do not know if you should enter through the "front
door" or "back door", then you can wait until you file your tax.
The dead line for contributing to prior year is 4/15 next year.
This is why Form 5498 comes after the filing dead line.

- If you do have traditional
IRA or rollover IRA from 401(k) for which you have not paid taxes
yet ("old money"), then you would need to convert it to ROTH IRA
and pay tax first, which is the original intent of the "back door".
If you do not have "old money" or have got rid of it, there is
nothing wrong nor illegal for the "new money" to take a free ride
via the "back door". I would not recommend to mix the "old money"
without basis with "new money" with basis for the sake of sanity,
or you will need to keep track of the basis via [Form
8606](https://www.irs.gov/pub/irs-pdf/f8606.pdf), rollover the "old
money" and "new money" proportionally, and pay tax on the "old
money".  

PS:

When executing a Backdoor Roth IRA conversion, the pro-rata rule applies if you
have pre-tax funds in a Traditional IRA at any time within the same tax year.
Even if you complete the Backdoor Roth conversion before rolling over pre-tax
funds from a 401(k) to a Traditional IRA later in the year, the IRS will still
apply the pro-rata rule based on your total IRA balances as of December 31 of
that tax year.

The pro-rata rule requires that when converting funds from a Traditional IRA to
a Roth IRA, the taxable and non-taxable portions are determined based on the
ratio of pre-tax to after-tax funds across all your Traditional IRAs as of
December 31 of that year.

Example Scenario:

  - In January 2024, you contribute $7,000 to a Traditional IRA and immediately convert it to a Roth IRA (Backdoor Roth).
  - In December 2024, you roll over $693,000 from a 401(k) to a Traditional IRA.

Since the pro-rata rule applies to your entire Traditional IRA balance as of
December 31, your conversion in January is now subject to taxation.

The Tax Cuts and Jobs Act (Pub. L. No. 115-97) eliminated the ability to recharacterize a Roth IRA conversion starting January 1, 2018.
This means Roth conversions are irrevocable, and you must pay tax on the pre-tax portion of the conversion.

The non-taxable portion of the $7,000 conversion is determined using the formula:

$$
\frac{7,000}{7,000+693,000} \times 7,000 = 70.00
$$

Breakdown of Funds:

| Fund Type        | Amount Before Conversion | Amount Converted | Remaining Balance |
|----------------------|----------------------------|----------------------|------------------------|
| After-Tax Fund   | $7,000                      | $70              | $6,930             |
| Pre-Tax Fund     | $693,000                    | $6,930           | $686,070           |

You have three options afterwards:

Option 1: Transfer the Pre-Tax Portion Out. Best if you want to continue Backdoor Roth conversions tax-efficiently.

  - Roll over the pre-tax portion of the IRA into a 401(k) (if your plan allows it).
  - Alternatively, roll it into an HSA (if you have an eligible plan and haven't used the once-in-a-lifetime IRA-to-HSA transfer).
  - Next year, convert only the after-tax portion to a Roth IRA, avoiding pro-rata taxation.

Option 2: Convert Everything and Pay the Tax. Best if you want tax-free growth moving forward.

  - Convert all Traditional IRAs (including rollover IRAs) to a Roth IRA.
  - "Bite the bullet" and pay tax now to allow tax-free withdrawals later.

Option 3: Stop Backdoor Roth Conversions. Best if you don’t want to deal with complex tracking.

  - Keep everything in the Traditional IRA and let it grow tax-deferred.
  - If you plan to convert later, track pre-tax and after-tax amounts carefully.
