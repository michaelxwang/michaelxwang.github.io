---
layout: post
title: "Tax notes: Dependent filing requirements"
categories:
- tax
---

Some clients asked me whether their dependents are required to file tax, 
I hope the following graph can answer this question clearly.

<img src="/assets/images/20211105-dependent-filing.pdf">

This graph was created based on the IRS' "form language" in <a href="https://www.irs.gov/pub/irs-dft/p929--dft.pdf" target="_blank">IRS Publication 929</a> as reproduced below:

<table cellspacing="10" cellpadding="10">
<caption>Filing Requirement Worksheet for Most Dependents</caption>
<tbody>

<tr>
<td>1.
</td>
<td>
Enter dependent's earned income plus $350
</td>
<td>
</td>
</tr>

<tr>
<td>2.
</td>
<td>
Minimum amount
</td>
<td>
$1,100
</td>
</tr>

<tr>
<td>3.
</td>
<td>
Compare lines 1 and 2. Enter the larger amount
</td>
<td>
</td>
</tr>

<tr>
<td>4.
</td>
<td>
Maximum amount
</td>
<td>
12,550
</td>
</tr>

<tr>
<td>5.
</td>
<td>
Compare lines 3 and 4. Enter the smaller amount
</td>
<td>
</td>
</tr>

<tr>
<td>6.
</td>
<td>
Enter the dependent’s gross income. If line 6 is more than line 5, the dependent must file an income tax return. If the dependent is married and his or her spouse itemizes deductions on a separate return, the dependent must file an income tax return if line 6 is $5 or more
</td>
<td>
</td>
</tr>

</tbody>
</table>

The form language can be directly translate to a formula:

<img src="https://latex.codecogs.com/svg.latex?\small&space; f(x) = {\rm min}({\rm max}(x+350, 1100), 12550)">

(I guess min() and max() are not "true" mathematical functions, while WolframAlpha has it, GeoGebra does not.)
I have to translate it to the traditional math function as:

<img src="https://latex.codecogs.com/svg.latex?\small&space;
{\rm Gross\_Income}(x)= \left\{
\begin{array}{ll}
1100 & 0\leq x \leq 1100-350 \\
x+350 & 1100-350\leq x\leq 12550-350\\
12550 & 12550-350\leq x \\
\end{array}
\right.
">

While the IRS form language uses gross income, it is more insightful to use unearned income (investment) to determine
the dependent filing requirement. The formula is:

<img src="https://latex.codecogs.com/svg.latex?\small&space; 
{\rm Unearned\_Income}(x)= \left\{
\begin{array}{ll}
1100 -x & 0\leq x \leq 1100-350 \\
350 & 1100-350\leq x\leq 12550-350\\
12550 -x & 12550-350\leq x  \leq 12550 \\
0 & 12550\leq x \\
\end{array}
\right.
">

From either the formula or the graph, we can conclude:

- when the dependent has zero earned income, she is allowed to have up to \$1,100 unearned income without filing tax.
- The allowed unearned income reduces linearly to \$350 when earned income is between \$0 and \$750.
- The allowed unearned income stay flat when earned income is between  \$750 and \$12,200
- The allowed unearned income reduces linearly to \$0 when earned income is between \$12,200 and \$12,550, the standard deduction for single status.

When filing dependent return, be sure to check the "can be claimed as a dependent" box, or it results in a conflict
and both the dependent and the person which claimed the dependent will receive an IRS letter. Also when the dependent
has earned income, you can open a Roth IRA account for the dependent up to the earned income, or the maximum contribution allowed
for the year (\$6,000 for 2021), whichever is lower.
