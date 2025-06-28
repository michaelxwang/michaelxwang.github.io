---
layout: post
title: Tracking and Deducting Accrued Interest on Bonds
categories:
- tax
---

When you purchase a bond between its interest payment dates, you're often
required to pay the seller **accrued interest** for the period they held the
bond. However, this accrued interest is **not immediately deductible**.
Instead, you can deduct it **only when that interest is considered received**.
This article walks through a step-by-step algorithm to determine when and how
much of that paid interest you can deduct, and how to properly track it using
tax forms like **Form 1099-INT**, **Form 1099-B**, and **Schedule B**.

#### ✨ Quick Summary

- **Accrued interest paid** on a bond **is not deductible until it is received**.
- Interest may be received through:
  - An actual **interest payment** from the bond (reported on **Form 1099-INT**)
  - **Accrued interest received as part of a bond sale** (must be manually reported on **Schedule B**, not on 1099-INT)
- You must track whether interest has been recovered and deduct accordingly.

#### ✅ Step-by-Step Algorithm

- For each CUSIP where you paid accrued interest when purchasing the bond:
  - Find the total accrued interst
  - Check if the CUSIP appears on **Form 1099-INT**.
    - If **yes**:
      - It means the bond paid actual interest during the year.
      - You can deduct the **accrued interest paid** on any lots of that CUSIP.
      - This deduction goes on **Schedule B**, and reduces the interest reported on 1099-INT.
      - _Even if you have some shares of the CUSIP sold before the payment date, the interest will be reflected on the sale price that goes to Schedule B._
    - **else**:
      - _There are two possibilities:_
        - _(a) The bond **did not pay any interest** during the year._
        - _(b) The bond was **sold before the interest payment date**._
      - Check **Form 1099-B**:
        - If the CUSIP appears on 1099-B
             - Identify the number of units (face value) sold.
             - Prorate the **original accrued interest paid** by the fraction of the bond that was sold.
             - This prorated portion is considered **recovered** and is deductible.
             - You must manually report the accrued interest received **as interest income on Schedule B**, as it is not included in 1099-INT.
  - Any remaining unrecovered accrued interest for the CUSIP
  - Carry forward to the next year.
  - Reapply this algorithm recursively.

#### 📊 Accrued Interest Deduction Example

| CUSIP       | Accrued Paid | 1099-INT? | 1099-B? (Percent)  | Action                                |
|-------------|---------------|------------|------------------|----------------------------------------|
| AAA123ABC   | $120.00       | Yes        | Yes/No           | Deduct full $120                       |
| BBB456XYZ   | $90.00        | No         | Yes (50%)        | Deduct $45 now; carry forward $45     |
| CCC789DEF   | $80.00        | No         | No               | Carry forward full $80                |

#### 📃 Where to Report

| Event                          | Reflected on         | Line                 |
|--------------------------------|--------------|------------------------------|
| Accrued interest received via coupon | 1099-INT    | Schedule B              |
| Accrued interest received via sale   | 1099-B      | Schedule B, D, Form 8949 |
| Accrued interest paid (deducted)     | 1099-* supplemental info | Schedule B as a negative adjustment    |

#### 🔍 Important Notes

- **Do not rely solely on Form 1099-INT** to determine how much interest you received. If you sold a bond before the coupon date, your broker **will not** report the accrued interest received on the sale in 1099-INT.
- In that case, you must report it manually on **Schedule B**.
- Once you report accrued interest as **income**, you may deduct an equal amount that you previously paid.
- Always retain records of purchase confirmations and broker accrued interest summaries.

#### 🚀 Conclusion

Tracking accrued interest paid and deducted requires coordinating between
multiple forms and careful recordkeeping. Use this algorithm each year to
ensure you're deducting the correct amount **only when earned**, and avoid
either missing deductions or double-deducting interest.
