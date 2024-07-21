---
layout: post
title: When summing digits and multiplying by 3 repeatedly
categories:
- math
---

This is a proof that for any positive integer, when summing its digits and multiplying by 3 repeatedly, will eventually equal 27. For example,

| Step                  | Value |
|:----------------------|------:|
| To start with         | 97    |
| Sum of digits         | 16    |
| Multiplied by 3       | 48    |
| Sum of digits         | 12    |
| Multiplied by 3       | 36    |
| Sum of digits         | 9     |
| Multiplied by 3       | 27    |

Now let us prove this mathematically step by step.

(a) First let us prove:

Let $$n$$ be a positive integer, and let $$s(n)$$ denote the sum of the digits of $$n$$. Then $$n$$ and $$s(n)$$ are congruent modulo 9, i.e.,
$$
n \equiv s(n) \pmod{9}
$$.

Consider a positive integer $$n$$ with decimal representation $$a_k\ a_{k-1} \ldots a_1\ a_0$$, where $$a_i$$ are the digits of $$n$$. We can write $$n$$ as:

$$
\begin{align*}
n &= 10^k \cdot a_k + 10^{k-1} \cdot a_{k-1} + \cdots + 10 \cdot a_1 + a_0 \\
  &= (10^k - 1) \cdot a_k + a_k + (10^{k-1} - 1) \cdot a_{k-1} + a_{k-1} + \cdots + 9 \cdot a_1 + a_1 + a_0 \\
  &= (10^k - 1) \cdot a_k + (10^{k-1} - 1) \cdot a_{k-1} + \cdots + 9 \cdot a_1 + s(n)
\end{align*}
$$

Since $$(10^k - 1), 10^{k-1} - 1), \cdots, 9$$ are all dividable by 9, $$n$$ and $$s(n)$$ are congruent modulo 9.

(b) Since $$n$$ and $$s(n)$$ are congruent modulo 9, $$3n$$ and $$3s(n)$$ are congruent modulo 9.

(c) By applying theorem in (a), $$3s(n)$$ and $$s(3s(n))$$ are congruent modulo 9.

(d) By combining (b) and (c), $$3n$$ and $$s(3s(n))$$ are congruent modulo 9.

(e) Since $$3n$$ and $$s(3s(n))$$ are congruent modulo 9, $$9n$$ and $$3s(3s(n))$$ are congruent modulo 9.

(f) Since $$9n$$ dividable by 9, $$3s(3s(n))$$ is a multiple of 9, which means that after two repetations of summing digits of an integer and multiplying by 3, the result becomes a multiple of 9.

(g) Let us continue with third repetition, by applying theorem in (a) again, $$s(3s(3s(n)))$$ and $$3s(3s(n))$$ are congruent modulo 9, i.e. $$s(3s(3s(n)))$$ is multiple of 9. Therefore,
$$3s(3s(3s(n)))$$ is multiple of 27. That is, after third repetition, the result is a multiple of 27. Since this conclusion is based on the number before the repetition is a multiple of 9,
the result will always be a multiple of 27 in any further repetitions.

(h) Now let us prove that the operation of summing its digits and multiplying by 3 will result in smaller number for a number greater or equal 30, i.e. $$3s(n) < n$$ for $$n >= 30$$.

Given:

$$
n = 10^k \cdot a_k + 10^{k-1} \cdot a_{k-1} + \cdots + 10 \cdot a_1 + a_0
$$

We have:

$$
\begin{align*}
n - 3s(n) &= (10^k - 3) \cdot a_k + (10^{k-1} -3) \cdot a_{k-1} + \cdots + (10-3) \cdot a_1 + (1 - 3)\cdot a_1 \\
           &> (10^k - 3) \cdot a_k + (10^{k-1} -3) \cdot a_{k-1} + \cdots + 7 \times 3 - 2 \times 9 \\
\end{align*}
$$

so,

$$
\begin{align*}
n - 3s(n) &> (10^k - 3) \cdot a_k + (10^{k-1} -3) \cdot a_{k-1} + \cdots +3 \\
           &> 0
\end{align*}
$$

(i) Based on (g), after third round, if the result is not 27, it is $$2\times27$$ or greater. Based on (h), each further repetation will reduce the result until it is below 30, and (h) tells us the result is a multiple of 27, A number that is below 30 and a multiple of 27 is 27. Q.E.D.

P.S. Finding the smallest number that requires 4 repetitions of summing its digits and multiplying by 3 to reach 27 by brute force is challenging due to the size of the number. Instead, we can first find $$X$$, the smallest multiple of 3 that requires 3 repetitions, and then work backward to find the smallest number leading to $$Xi$$. The results of this discovery are tabulated below.

| Step                  | Value | Note |
|:----------------------|------:| :--- |
| To start with         | $$ 2 \times 10^{259} + (10^{259} - 1) $$| It is 2 followed by 259 digits of 9 |
| Sum of digits         | 2333    | Computed as $$2 + 259\times9$$ |
| Multiplied by 3       | 6999    | First round |
| Sum of digits         | 33    | 
| Multiplied by 3       | 99    | Second round, multiple of 9 |
| Sum of digits         | 18     |
| Multiplied by 3       | 54    | Third round, multiple of 27 |
| Sum of digits         | 9     |
| Multiplied by 3       | 27    | Fourth round |
