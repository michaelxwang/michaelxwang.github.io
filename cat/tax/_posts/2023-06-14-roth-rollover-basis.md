---
layout: post
title: Basis in rollover from Roth 401(k) to Roth IRA
categories:
  - tax
---

The question starts very simple: when there is a loss, i.e. the contribution amount exceeds the distribution amount, what is the basis in rollover?

The authority to this question is buried in the Treasury Decision T.D. 9324
initially published in Federal Registry (a daily journal of the United States Government)
on 04/30/2007 as document ID [72 FR 21103][fr]{:target="_blank"},
and codified in Code of Federal Regulations [Part I][cfr]{:target="_blank"},
mostly in [1.408A-10][408A10]{:target="_blank"}
(Coordination between designated Roth accounts and Roth IRAs), and [1.402A-1][402A1]{:target="_blank"}
(Designated Roth Accounts).

Let us read the regulations. In response to the question Q-3:

> For purposes of the ordering rules on distributions from Roth IRAs, what
> portion of a distribution from a rollover contribution from a designated Roth
> account is treated as contributions?

[1.408A-10][408A10]{:target="_blank"} (Coordination between designated Roth accounts and Roth IRAs) has this to say in A-3(a):

> (a) Under [section 408A(d)(4)][408A]{:target="_blank"},
> distributions from Roth IRAs are deemed to consist
> first of regular contributions, then of conversion contributions, and finally,
> of earnings. For purposes of [section 408A(d)(4)][408A]{:target="_blank"},
> the amount of a rollover contribution that is treated as a regular contribution is the portion of the
> distribution that is treated as investment in the contract under A–6 of [§1.402A–1][402A1]{:target="_blank"},
> and the remainder of the rollover contribution is treated as
> earnings. Thus, the entire amount of any qualified distribution from a
> designated Roth account that is rolled over into a Roth IRA is treated as a
> regular contribution to the Roth IRA. Accordingly, a subsequent distribution
> from the Roth IRA in the amount of that rollover contribution is not includible
> in gross income under the rules of A–8 of [§1.408A–6][408A6]{:target="_blank"}.

It is a mouthful of words, but the key part is "the portion of the distribution that is treated as investment".
It implies that the cost basis cannot exceed the distribution as a portion cannot be greater than the whole.
The issue pops up when there is an investment loss when the contribution is greater than the account value from which to be distributed.

The sentence after "Thus" appears to be abrupt, and the sentence before that does not bear
a logical relationship to the conclusion after that. This is because section refers to the A-6 of Section [1.402A-1][402A1]{:target="_blank"}
(Designated Roth Accounts) in how to determine the "investment in the contract" even though the circumstances are different but similar, in which it says:

> (a) If a distribution from a designated Roth account is rolled over to another
> designated Roth account in a direct rollover, the amount of the rollover
> contribution allocated to investment in the contract in the recipient
> designated Roth account is the amount that would not have been includible in
> gross income (determined without regard to [section 402(e)(4)][402]{:target="_blank"})
> if the distribution had not been rolled over. Thus, if an amount that is a qualified
> distribution is rolled over, the entire amount of the rollover contribution is
> allocated to investment in the contract.

In simpler language it says what is not included in gross income should be treated as investment.
In light of this reference, the conclusions after "Thus" in both sections can be easily understood
as in a qualified distribution, the entire amount of the rollover is not included in gross income, and
therefore the entire amount is treated as a regular contribution.

The next question is how to determine the what should be included and what should not be included
in gross income if it had not been a rollover? This question is answered in A-3 of [1.402A-1][402A]{:target="_blank"},
which in turn refers to [section 72(e)(8)][72]{:target="_blank"}
which says:

> (B) Allocation of amount received
> 
> For purposes of paragraph (2)(B), the amount allocated to the investment in the
> contract shall be the portion of the amount described in subparagraph (A) which
> bears the same ratio to such amount as the investment in the contract bears to
> the account balance. The determination under the preceding sentence shall be
> made as of the time of the distribution or at such other time as the Secretary
> may prescribe.

As the allocation is to determine the tax free portion of the distribution, the ratio
cannot be greater than 1, which is precisely coded in the worksheet of the IRS [pub 590-B][590b]{:target="_blank"}
(Distributions from Individual Retirement Arrangements) which follows the same [section 72][72]{:target="_blank"}
rule:

> Worksheet 1-1. Figuring the Taxable Part of Your IRA Distribution
>
> 7. Divide line 3 by line 6. Enter the result as a decimal (rounded to at least three places). If the result is 1.000 or more, enter 1.000

Prior to [Tax Cuts and Jobs Act][tcja], the loss from the IRA could deductible,
"but only when all the amounts in all your traditional IRA accounts have been
distributed to you" ([2017 version][590b2017]{:target="_blank"}
of the Pub 590-B).

Similarly, the cost basis exceeding the distribution is recognized when the entire account balance is distributed
as documented in [1.408A-10][408A10]{:target="_blank"}
(Coordination between designated Roth accounts and Roth IRAs) in A-3(b) which says:

> (b) If the entire account balance of a designated Roth account is distributed
> to an employee and only a portion of the distribution is rolled over to a Roth
> IRA within the 60-day period described in section 402(c)(3), and at the time of
> the distribution, the investment in the contract exceeds the balance in the
> designated Roth account, the portion of investment in the contract that exceeds
> the amount used to determine the taxable amount of the distribution is treated
> as a regular contribution for purposes of section [408A(d)(4)][408A]{:target="_blank"}.

The situation is more complex here because the rollover is indirect and the only a portion of the distribution is rolled to Roth IRA, but we can
treat the direct and complete rollover as a special case of the clause. Simply put, if the _entire_ account balance is distributed,
the contribution exceeding the distribution is treated as the cost basis. 

Since the section for rollover to Roth IRA is mirrored from the rollover to designated Roth account, we can
understand the treatment better by looking at the similar treatment in [1.402A-1][402A1]{:target="_blank"}
(Designated Roth Accounts) A-6 where the situation is simpler as indirect rollover is not allowed:

> (b) If the entire account balance of a designated Roth account is rolled over
> to another designated Roth account in a direct rollover, and, at the time of
> the distribution, the investment in the contract exceeds the balance in the
> designated Roth account, the investment in the contract in the distributing
> plan is included in the investment in the contract of the recipient plan.

After reading the law itself, we can understand where what the IRS is saying in its [instructions][i1099r]{:target="_blank"}
for forms 1099-R and 5498. It says on page 9:

> If you are making a distribution from a designated Roth account, enter the
> gross distribution in box 1, the taxable portion of the
> distribution in box 2a, the basis included in the distributed
> amount in box 5 ...

Please note "the basis included in the distributed amount", that is, the basis cannot exceed the distribution.

On page 13, it says:

> Box 5. Employee Contributions/Designated Roth Contributions or Insurance Premiums
>
> Enter the employee's contributions, designated Roth
> contributions, or insurance premiums that the employee may
> recover tax free this year (even if they exceed the box 1 amount).

This is clear except the concessive clause in parentheses which is supposed to add clarification.
Confusing it is, but the information is not wrong. It says two things: (a) the box 5 is the contribution
to recover tax free, and (b) the amount could exceed the distribution. When will (b) happen? The answer
is on the same page:

> If a total distribution is made, the total employee contributions or insurance
> premiums available to be recovered tax free must be shown only in box 5. If any
> previous distributions were made, any amount recovered tax free in prior years
> must not appear in box 5.

The checkbox for "Total distribution" on [Form 1099-R][1099r]
indicates the situation. Perhaps the only other situation is the 
rollover the stocks in kind, the cost basis is carried with the stock.
The [instructions][i1099r]{:target="_blank"}
says on page 10:

> If a distribution is a loss, do not enter a negative amount in this box. For
> example, if an employee's 401(k) account balance, consisting solely of stock,
> is distributed but the value is less than the employee's remaining after-tax
> contributions or designated Roth contributions, enter the value of the stock in
> box 1, leave box 2a blank, and enter the employee's contributions or designated
> Roth contributions in box 5.

I doubt if anyone has read all the above, but if you did, you would agree that the
tax code is like the old code in a company, it is too complicated to refactor. The only
feasible solution is to set up a new tax system in Mars, and then migrate the taxpayers
to that new system.

[irb]: https://www.irs.gov/irb/2007-22_IRB
[egtrra]: https://www.congress.gov/107/plaws/publ16/PLAW-107publ16.htm
[fr]: https://www.federalregister.gov/documents/2007/04/30/E7-8125/designated-roth-accounts-under-section-402a
[402A]: https://www.law.cornell.edu/uscode/text/26/402A
[cfr]: https://www.ecfr.gov/current/title-26/chapter-I/subchapter-A/part-1?toc=1
[408A6]: https://www.ecfr.gov/current/title-26/chapter-I/subchapter-A/part-1/section-1.408A-6
[408A10]: https://www.ecfr.gov/current/title-26/chapter-I/subchapter-A/part-1/section-1.408A-10
[402A1]: https://www.ecfr.gov/current/title-26/chapter-I/subchapter-A/part-1/section-1.402A-1
[i1099r]: https://www.irs.gov/pub/irs-pdf/i1099r.pdf
[408A]: https://www.law.cornell.edu/uscode/text/26/408A
[402]: https://www.law.cornell.edu/uscode/text/26/402
[72]: https://www.law.cornell.edu/uscode/text/26/72
[590b]: https://www.irs.gov/pub/irs-pdf/p590b.pdf
[tcja]: https://en.wikipedia.org/wiki/Tax_Cuts_and_Jobs_Act
[590b2017]: https://www.irs.gov/pub/irs-prior/p590b--2017.pdf
[1099r]: https://www.irs.gov/pub/irs-pdf/f1099r.pdf
