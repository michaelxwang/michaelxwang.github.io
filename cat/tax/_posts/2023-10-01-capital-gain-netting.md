---
layout: post
title: Capital gain and loss netting rules
categories:
  - tax
---

The process starts with netting the gain and loss within both short-term and long-term categories. This will result in one of the following six scenarios:

1. **Both short-term and long-term gain.**
2. **Both short-term and long-term loss.**
3. **Short-term gain and long-term loss**, with the gain being greater than the loss.
4. **Short-term gain and long-term loss**, with the loss being greater than the gain.
5. **Short-term loss and long-term gain**, with the gain being greater than the loss.
6. **Short-term loss and long-term gain**, with the loss being greater than the gain.

As shown in the picture below:

```
 Pay both S&L           Offset S gain               Offset L gain
 capital gain           with L loss                 with S loss
                        pay S gain                  pay L gain
      L
      ┌┐                     S                             L
      ││                     ┌┐
      ││                     ││                            ┌┐
   S  ││                     ││                            ││
   ┌┐ ││                     ││           S                ││
   ││ ││                     ││           ┌┐               ┼┼ offset
   ││ ││                     ││           ││               ││            L
   ││ ││                     ┼┼ offset    ││               ││            ┌┐
   ││ ││                     ││           ││               ││            ││
   ││ ││                     ││           ││               ││            ││
   ││1││          2          ││3          ││4            5 ││          6 ││
───┴┴─┴┴────┼───┬┬─┬┬───┼────┴┴─┬┬───┼────┴┴─┬┬───┼────┬┬──┴┴───┼────┬┬──┴┴───
                ││ ││           ││           ││        ││            ││
                ││ ││           ││           ││        ││            ││
                ││ ││           ││           ││        ││            ││
                ││ ││           └┘           ││        ││            ┼┼ offset
                ││ ││           L            ││        └┘            ││
                ││ └┘                        ┼┼ offset  S            ││
                ││ L                         ││                      ││
                ││                           ││                      ││
                └┘                           └┘                      └┘
                S                            L                       S

            Take loss                 Offset S gain             Offset L gain
            up to 1.5k/3k             to 0, take loss           to 0, take loss
            from S then L             up to 1.5k/3k             up to 1.5k/3k
            carryover rest            carryover rest            carryover rest
```

- For the *first scenario* where you you have gains in both short-term and
  long-term, you pay the short-term gain at the marginal rate, and
  the long-term gain at 0-20% or the marginal rate, whichever is less, as
  explained [here][long].

- In the *second scenario* where both short-term and long-term losses are present, you can take your losses up to $1,500 if you are married but filing separately
  or $3,000. You first take the loss from the short-term then the long-term until the maxium is reached.
  Any loss that exceeds these limit can be carried over to the next
  year. The loss taken, whether from short-term or long-term, reduces your tax liability
  by offsetting against your ordinary income at your marginal rate.

- If you have a net loss in one category and net gain in the other, use the
  loss to offset the gain until one of the categories reaches zero. After that,
  you either pay tax on the gain or take the loss in the remaining
  category.

[long]: https://taxandlife.com/cat/tax/2021/11/13/capital-gain.html
