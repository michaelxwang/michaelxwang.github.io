---
layout: post
title: "RSU Wash-sale timing: vesting or release?"
date: 2026-10-19
categories: tax
tags:

- Wash-sale
- RSU
- Acquisition
- Vesting
- Release

---

**FACTS**

DocuSign restricted stock units (RSUs) vest before a recurring quarterly release date, documented in a DocuSign [RSU agreement](https://www.sec.gov/Archives/edgar/data/1261333/000119312518099555/d506878dex104.htm){:target="_blank"} filed with the SEC, and in employee’s grant documents as illustrated below:

* *Vest Date: 11/10/2025*
* *Release Date: 12/15/2025*

The E\*Trade’s 1099-B lists the release date as “date acquired”.

**ISSUE**

Which date, the vest date or release date, is used for wash-sale computation?

**SHORT ANSWER**

Under the facts, the wash-sale computation should use the release date (12/15/2025), not the vest date (11/10/2025). This holds if December 15 is when the shares were actually delivered to you, which is what the E\*Trade 1099-B suggests. For a 12/15/2025 acquisition, the 61-day window runs from 11/15/2025 through 1/14/2026, inclusive.

**ANALYSIS**

**Step 1: Identify the statutory event**

[IRC §1091(a)](https://www.taxnotes.com/research/federal/usc26/1091){:target="_blank"} and [Treas. Reg. §1.1091-1(a)](https://www.taxnotes.com/research/federal/cfr26/1.1091-1){:target="_blank"} provide that a loss is disallowed if, within a 61-day period (beginning 30 days before the date of sale and ending 30 days after), the taxpayer has acquired or entered into a contract or option to acquire substantially identical stock or securities.

The test turns on when you acquire the stock. It does not mention "vesting" or "release," so we need another authority to say when an RSU holder acquires stock.

**Step 2: Acquiring stock means getting beneficial ownership**

[Treas. Reg. §1.83-3(a)(1)](https://www.taxnotes.com/research/federal/cfr26/1.83-3){:target="_blank"} establishes that a transfer of property occurs when a person acquires a beneficial ownership interest in such property.

This is a §83 rule, not a wash-sale rule, but it is the closest federal definition of when employer-provided stock is transferred, and I found no wash-sale authority that defines "acquired" differently.

**Step 3: Vesting and transfer are separate tests**

[Treas. Reg. §1.83-3](https://www.taxnotes.com/research/federal/cfr26/1.83-3){:target="_blank"} distinguishes between property being "substantially vested" and "transferred." Property is substantially vested when it is either transferable or not subject to a substantial risk of forfeiture.

An RSU vesting on 11/10 means your forfeiture risk has ended. It does not mean you already hold shares. [Treas. Reg. §1.83-3(e)](https://www.taxnotes.com/research/federal/cfr26/1.83-3){:target="_blank"} also excludes an "unfunded and unsecured promise to pay money or property in the future" from "property." An RSU before delivery is that kind of promise.

The [SEC filing](https://www.sec.gov/Archives/edgar/data/1261333/000119312518099555/d506878dex104.htm){:target="_blank"} section 16 says the award "is unfunded" and a holder of a vested award is "an unsecured creditor of the Company." It adds that you "will not have voting or any other rights as a stockholder" until the shares are issued, and that on issuance you "obtain full voting and other rights."

Section 6 says you receive no benefit "with respect to any cash dividend, stock dividend or other distribution" on the RSUs, apart from plan adjustments.

**Step 4: Apply it to our case**

| Date | What happened | Acquisition of shares? |
| :---- | :---- | :---- |
| 11/10/2025 | The entitlement vests. | No. You still hold only a promise of future shares (Steps 2–3). |
| 12/15/2025 | The shares are released to you, and E\*Trade lists this as "date acquired." | Yes, if the shares are first delivered on that date. This is when beneficial ownership arises. |

If the employee's grant contains the same terms as the SEC form (see section 16 above), the grant puts a gap between vesting and release. During that gap, the company still owes you the shares. Under Step 2, you acquire them on the release date.

**E\*TRADE EVIDENCE**

The 1099-B "date acquired" of 12/15 fits Steps 2–4 in ANALYSIS. The broker reports the release date as the acquisition date, which is consistent with delivery of the shares on that date.

Limitation: The 1099-B is evidence, not law. [Section 1091](https://www.taxnotes.com/research/federal/usc26/1091){:target="_blank"} and the regulations decide the result, so the broker's label alone cannot settle it. With that said, the position is stronger because the legal test and the broker's data agree.

**CAUTIONS**

* The "contract or option" clause. [IRC §1091(a)](%20https://www.taxnotes.com/research/federal/usc26/1091){:target="_blank"} also covers entering into "a contract or option so to acquire" the stock. An RSU is a contract right, so a cautious reader could ask whether the grant, or the vesting, is itself a contract event. No ruling or case was identified that settles this for delayed-settlement RSUs, so it is not risk-free to assume that only the release date matters.

* No RSU-specific wash-sale authority. The reasoning applies §83 regulations to a §1091 question. It is a well-grounded inference, not an express rule.

If you want to avoid the question: plan loss sales outside both windows (10/11/2025 through 12/10/2025, and 11/15/2025 through 1/14/2026), which combine to 10/11/2025 through 1/14/2026. That is a precaution, not what the law requires on these facts.

Furthermore, a wash sale only temporarily disallows the loss. Under [IRC §1091(d)](https://www.taxnotes.com/research/federal/usc26/1091){:target="_blank"} and [Treas. Reg. §1.1091-2](https://www.taxnotes.com/research/federal/cfr26/1.1091-2){:target="_blank"}, the disallowed loss is added to the basis of the newly acquired shares, so it is recognized when those shares are sold. Likewise, under [IRC §1223(3)](https://www.taxnotes.com/research/federal/usc26/1223){:target="_blank"}, the holding period of the replacement shares includes the period for which the shares sold at a loss were held, so a wash sale does not restart the holding-period clock.
