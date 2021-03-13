---
layout: post
title: Income earned outside of US by residents and nonresidents
categories:
- tax
---

Residents and nonresidents report foreign earned income differently: residents report worldwide income, while nonresidents report only income 
from sources in the United States or effectively connected income. You could be a resident and nonresident during the same year ("dual status"), in which case you follow
the resident rule while you are a resident, and nonresident rule while a nonresident.

#### Resident, nonresident, and dual status

If you are a US citizen or a permanent resident, then you are a resident. Period.

If you are not a US citizen or a permanent resident, then you compute the number of days using the [Substantial Presence Test][substantial]. Please do not
count the days when you are an "Exempt Individual" such as an F-1 student within first 5 calendar years in the United States.

If you passed the test, generally you are a resident for tax purposes, but you could be a dual status alien.

If you fail the test, generally you are a nonresident, but you can make the [First-Year Choice][first-year] to be taxed as dual-status if doing so has a clear advantage, such as deducting mortgage interest payment
during the residence period, or claiming the recovery rebate credit for the COVID-19 assistance (click [this link][dual-rrc] for more information). The biggest advantage is that
when you are married, you can make a [section 6013][6013] election to file jointly as full year US residents.

#### Residents

Residents report worldwide income, but if you satisfy either the [Physical Presence Test][physical] or the [Bona Fide Residence Test][bona fide], you can exclude the foreign earned income up to the maximum
exclusion amount (107,600 in 2020), and unexcluded amount can be further offset by the foreign tax credit.

To pass the Physical Presence Test, you must be physically present outside of the United States for a full 330 days during a 12-month test period that includes the days of the current year. The test period could
be from January 1, YYYY to December 31, YYYY, but it does not necessarily to be the entire calendar year. It could be, for example, from March 1, YYYY to February 28, YYYY + 1 if you left the US. In this example, the
maximum exclusion amount will be reduced to 10/12, but it does not reduce the exclusion amount directly. It could also be March 1, YYYY -1 to February 28, YYYY if you come to the United States.

The Bona Fide Residence Test has no hard foreign presence requirement,
but your trip to the United States must be "brief or temporary", you
must be a foreign resident for the entire calendar year, and generally,
you must pay taxes to the foreign country.

"What is the use of including the income and then excluding it?" you may ask. First of all, you may not be able to exclude all of the income. Secondly, if you have US income, it pushes 
the US income to a higher bracket due to the [Pauli exclusion principle][pauli]. [This post][exclusion-math] of mine discusses the mathematics of the exclusion. 

#### Nonresidents

Nonresidents do not report income that is not from a US source. For example, [Xi Jinping][xi] does not file a nonresident return to the US reporting his wages. The ten thousand dollar question is: is the
wage paid by a US company while working in a foreign country income from a US source? To answer this question, let us go to the authorities.

- U.S. Code

The U.S. Code Title 26, The Internal Revenue Code (IRC), § [862][862] says:

> (a) Gross income from sources without United States  
>     The following items of gross income shall be treated as income from sources without the United States:  
>   ...  
>   (3) compensation for labor or personal services performed without the United States;

In the context here, without = not within, i.e. outside. This establishes that the income is foreign income.

- Code of Federal Regulations (CFR)

Often time the law lacks the implementation details, and the IRS must come up with an operation procedure. In this case, since the text of law is so clear, [the CFR][cfr] simply mirrors what the law said.

- IRS publication 519

The IRS [publication 519][pub519] talks more or less in human language. It says:

> Income from sources outside the United States that is not effectively
> connected with a trade or business in the United States is not
> taxable if you receive it while you are a nonresident alien.

So we have established that the compensation for services performed outside of the US is foreign income, and now we need to see if the foreign income is effectively connected with
a U.S. trade or business. The [publication 519][pub519] says:

> Foreign Income  
>
> You must treat three kinds of foreign source income as effectively connected with a trade or business in the United States if:
> - You have an office or other fixed place of business in the United States to which the income can be attributed,
> - That office or place of business is a material factor in producing the income, and
> - The income is produced in the ordinary course of the trade or business carried on through that office or other fixed place of business.

The three kinds of foreign source income are: (1) Rents, (2) Dividends, (3) Sale. The wage income is not included in the list. 

- IRS website

The IRS says in [this website][irs-web]:

> As a general rule, wages earned by nonresident aliens for services performed outside of the United States for any employer are foreign source income and therefore are not subject to reporting and withholding of U.S. federal income tax.

- Opinions from other practitioners

[This practitioner][thomson] from Thomson Reuters says clearly:

> ... wages for work days outside the United States which are foreign-source income and not subject to U.S. tax. 

We should always take the opinions from other practitioners (including mine) with a grain of salt, but in this case I believe the opinion is supported by the higher authorities. 

#### State residency

State residency rules are different from federal rules: if you live in the state then you are a resident of the state.
While each state has its own rules to determine residency, California
is most welcoming. That you left California does not necessarily mean
you are not a resident; it depends on your intent to return
("domicile"). While intention is hard to measure, California kindly provides a safe
harbor rule in [this guideline][ca]: if you are outside of California for 546 consecutive days, then
you are permitted to consider yourself a nonresident of California.

After reading about tax law, I came to the conclusion that the law is more than a set of random rules. It has its own internal logic.
If you breathe American air, which may be sweet and free (as in freedom) but not free (as in free beer), you do not pay for each breath except
in the form of taxes.

[substantial]: https://www.irs.gov/individuals/international-taxpayers/substantial-presence-test
[first-year]: https://www.irs.gov/individuals/international-taxpayers/alien-tax-status-first-year-choice
[dual-rrc]: https://unixlabplus.com/tax/2021/02/18/dual-status-eip.html
[6013]: https://www.law.cornell.edu/uscode/text/26/6013
[physical]: https://www.irs.gov/individuals/international-taxpayers/foreign-earned-income-exclusion-physical-presence-test
[bona fide]: https://www.irs.gov/individuals/international-taxpayers/foreign-earned-income-exclusion-bona-fide-residence-test
[pauli]: https://en.wikipedia.org/wiki/Pauli_exclusion_principle
[exclusion-math]: https://unixlabplus.com/tax/math/2018/04/03/foreign-incom-exclusion.html
[xi]: https://en.wikipedia.org/wiki/Xi_Jinping
[862]: https://www.law.cornell.edu/uscode/text/26/862
[cfr]: https://www.law.cornell.edu/cfr/text/26/1.862-1
[pub519]: https://www.irs.gov/pub/irs-pdf/p519.pdf
[irs-web]: https://www.irs.gov/individuals/international-taxpayers/persons-employed-abroad-by-a-us-person
[thomson]: https://tax.thomsonreuters.com/site/wp-content/pdf/nra-tax/Challenges-Foreign-National-Taxpayers-ebook.pdf
[ca]: https://www.ftb.ca.gov/forms/2020/2020-1031-publication.pdf
