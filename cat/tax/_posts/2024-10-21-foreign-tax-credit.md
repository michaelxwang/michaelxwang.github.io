---
layout: post
title: Foreign tax credit for long term capital gains - the IRS algorithm
categories:
- tax
---

A lot of people think since they have paid taxes on their foreign income to the local authorities, they do not
need to pay tax again. While this is true to some extent, you should still report the foreign income, and
take either the foreign earned income exclusion or the foreign tax credit. This sounds fair, but the algorithm
that the IRS uses may surprise you.

In [this post][feic]{:target="_blank"},
I revealed the hidden formula used by the IRS to exclude the foreign earned income, which is _not_ as if the foreign
earned income were never included in taxable income, but rather pushes the rest of your income into a higher tax bracket. In this
post, I am going to uncover the flawed algorithm that the IRS employs in calculating the foreign tax credit
for long term capital gains and qualified dividends. 

The United States taxes its citizens and resident aliens on worldwide income. When a taxpayer sells stocks or
property in a foreign country that has been held for more than a year, they incur a long-term capital gain. In some countries, such
as India, taxpayers are required to pay taxes to local authorities. However, as a U.S. citizen or resident alien, they also need to report the income on their
Form 1040.

To avoid double taxation, the Internal Revenue Code allows for a foreign tax credit. This sounds good on paper, but the credit is not granted
as straightforwardly as one might think. For example, if Jane had $100,000 capital gain in India and paid $20,000 in foreign taxes,
and the same income reported on the U.S. return would generate a tax liability of $15,000, she would expect to pay no taxes in the U.S. as she already paid more in foreign taxes
than she would owe in the U.S. However the IRS thinks differently. Let me show you the algorithm they use to determine the tax credit.

The IRS computes the tax on foreign long-term capital gains not by the 0%, 15%, or the maximum 20% rates, but by using the foreign income ratio
multiplied by the total tax paid. This seems reasonable, but only if done correctly, as both methods should yield the same result.
To compute the ratio, we cannot simply use the face value of the foreign-long term capital gain income and the
U.S. regular income because they are taxed at different rates. We must apply weighted values to each income category. The IRS is right on this, but they
use 37%, the maximum tax rate, as the weight for U.S. regular income (denoted as U).
Meanwhile, the IRS uses 15% (or the applicable reduced tax rate) for U.S.
long-term capital gains and qualified dividends, which is the correct approach
for these types of income. However, the effect of this adjustment is smaller
for most people because long-term capital gains and qualified dividends
typically make up a smaller portion of their overall income.

More problematic is the fact that the IRS applies the 37% rate to U.S. regular income
when calculating the foreign tax credit, even though most taxpayers are subject
to a lower, graduated tax rate. This creates an unfair result because regular
income is not taxed at a flat 37%, and many people don’t reach that bracket.

Now, let's illustrate the IRS approach with some math. 
Suppose Jane's foreign long term capital-gains (denoted as F)
are taxed at [15% rate][long]{:target="_blank"}.
According to the IRS formula, Jane's foreign income ratio is:

$$
\begin{align*}
R &= \frac{F \times 15\%}{F \times 15\% + U \times 37\%} \\
  &= \frac{F \times \frac{15}{37}}{F \times \frac{15}{37} + U}
\end{align*}
$$

The IRS hides this formula in its "form language", but it clearly states in its [Form 1116 Instruction][f1116i]{:target="_blank"}:

> How to make adjustments. To adjust your foreign source
> qualified dividends or capital gain distributions, multiply your
> foreign source qualified dividends or capital gain distributions
> in each separate category by 0.4054 if the foreign source
> qualified dividends or capital gain distributions are taxed at a
> rate of 15%, and by 0.5405 if they are taxed at a 20% rate.
> Include the results on line 1a of the applicable Form 1116.
>
> You adjust your foreign source qualified dividends or
> capital gain distributions taxed at the 0% rate by not
> including them on line 1a.

Where do these numbers, 0.4054 and 0.5405, come from? Lo and behold, 0.4054 is just $$\frac{15}{37}$$, and likewise, 0.5405 is $$\frac{20}{37}$$.

As if this weren't enough injury, the IRS adds insult by allocating deductions to foreign income, which further reduces the foreign income ratio.
While this approach is already questionable since deductions apply regardless
of whether there is foreign income, it becomes even more problematic when
deductions are allocated based on face value of the foreign income which they previously
discounted when computing the foreign income ration:

> If you had to adjust your foreign qualified dividends or
> capital gains (discussed earlier), include those amounts
> without regard to any adjustments.

Adding the deduction (denoted as d), the IRS formula for foreign income ratio R becomes:

$$
\begin{align*}
R &= \frac{F \times \frac{15}{37} - d \times \frac{F}{F+U}}{F \times \frac{15}{37} + U}
\end{align*}
$$

In summary, the IRS uses the maximum tax rate (37%) for U.S. income as a weight
to make the foreign income ratio smaller and then prorates deductions on
unweighted income, further reducing the foreign income ratio.

Since total tax paid is $$F\times 15\% + U\times e\%$$, where $$e\%$$ is the effective tax rate on U.S. income, the
foreign tax paid on the US return, according to the IRS formula, is:

$$
\begin{align*}
{\rm Foreign Tax} &= \frac{F \times \frac{15}{37} - d \times \frac{F}{F+U}}{F \times \frac{15}{37} + U} \times (F\times 15\% + U\times e\%)
\end{align*}
$$

If the US income is much larger than foreign income (ignoring the deduction), the above formula approximately becomes:

$$
\begin{align*}
{\rm Foreign Tax} &= F \times 15\% \times \frac{e}{37}
\end{align*}
$$

In this case, the foreign tax paid per the IRS calculation is $$15%$$ reduced a factor of $$\frac{e}{37}$$. The reduction is caused by
the unrealistic weighting of 37% instead of the effective rate $$e\%$$. When the U.S. income is much larger, the effective rate $$e\%$$
approaches 37%, and the aberration becomes smaller.

Conversely, when U.S. income is much smaller (again ignoring the deduction), the formula can be approximated as:

$$
\begin{align*}
{\rm Foreign Tax} &= F \times 15\%
\end{align*}
$$

This reflects the actual foreign tax paid. It makes sense because when U.S. income is a smaller, the exaggerated weighting of U.S. income
becomes less prominent. 

The tax credit given is the smaller of the actual foreign tax paid on the IRS-calculated foreign tax on the U.S. return.

While the deductions allocated to foreign income are always included, there is an adjustment [exception][f1116i]:

> You qualify for the adjustment exception if you meet both
> of the following requirements.
>
> 1. Line 5 of the Qualified Dividends and Capital Gain Tax
> Worksheet in the Form 1040 instructions or line 18 of the
> Schedule D Tax Worksheet in the Schedule D (Form 1040)
> instructions is less than or equal to:
>
>     a. $364,200 if married filing jointly or qualifying surviving spouse,
>
>     b. $182,100 if married filing separately,
>
>     c. $182,100 if single, or
>
>     d. $182,100 if head of household.
>
> <ol start="2.">
>   <li> The amount of your foreign source net capital gain,
> plus the amount of your foreign source qualified dividends, is
> less than $20,000.

If your foreign long-term capital gains plus foreign qualified dividends are under $20,000, 
you qualify for the adjustment exception not only simplifies the situation, but also
prevents the unfair application of the 37% rate on U.S. income. The adjustment does not apply to foreign general income taxed
at the regular rates, which is outside the scope of this post.

Finally, let us illustrated the effect with a real example. A U.S. taxpayer sold a piece of property located in India in 2023, generating a long-term capital gain of $72,057.
The actual capital gains tax they had paid on their U.S. return is $$\$72,057 \times 15\% = \$10,808$$. Their effective tax rate was 16.1%, using the approximated formula based on
the IRS algorithm, they are allowed a credit of only $$\$10,808\times\frac{16.1}{37} = \$4703$$ (the exact calculation was $4,429), meaning only 44% of the capital gains tax paid were credited.

[feic]: https://taxandlife.com/cat/tax/math/2018/04/03/foreign-incom-exclusion.html
[long]: https://taxandlife.com/cat/tax/2021/11/13/capital-gain.html
[f1116i]: https://www.irs.gov/pub/irs-pdf/i1116.pdf
