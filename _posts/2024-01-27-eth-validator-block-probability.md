---
layout: post
comments: true
title: Estimating the Probability of Not Proposing an Ethereum Block
date: 2024-01-27 08:00:00
description: When your solo staking setup isn't proposing, you are asking "WHAT ARE THE ODDS?!"
---
**Update(May 2024)**: See pretty plot [yewjin.com/assets/html/eth_block_probability.html](https://www.yewjin.com/assets/html/eth_block_probability.html)

As an Ethereum staker, one of the key aspects of participation in the network is decentralization ... OK ... nevermind it's the opportunity to propose a block and hope for winning the block lottery. The probability of getting this chance, however, depends on several factors, most notably the total number of validators in the network and the number of validators you control. Here's how to calculate the probability of not proposing a block over different time periods - an hour, a day, a week, or even a month. Because, admit it, you are only asking this question after not getting a block proposal for that long and you are asking: "WHAT ARE THE ODDS?!"

The Ethereum PoS protocol, specifically in the context of block validation, operates with discrete time units called slots. A new block is proposed in each slot by a randomly selected validator. The probability of a specific validator being chosen for any given slot is inversely proportional to the total number of validators.

1. **Total Number of Validators (N):** The entire set of validators staking ETH in the network. You can use [validatorqueue.com](https://www.validatorqueue.com/) but as of Jan 27 2024, it's around 905,000.
2. **Your Validators (V):** The number of validators under your control.
3. **Time Period (T):** The duration for which you want to calculate the probability, measured in slots. (Note: The Ethereum network typically operates with a slot time of 12 seconds.)

### Calculating the Probability

The probability of not proposing a block in a single slot, for a user with V validators, is calculated as follows:

```
Probability (Single Slot) = 1 - (V / N)
```

To extend this to a specific time period, T slots, the formula becomes:

```
Probability (T Slots) = (1 - (V / N))^T
```

Handy number of slots in various time periods

- **For One Hour:** With T = 300 slots (assuming 12 seconds per slot).
- **For One Day:** T = 7,200 slots.
- **For One Week:** T = 50,400 slots.
- **For One Month:** Approximating a month as 30 days, T = 216,000 slots.

## Probabilities for 1 Validator

- **Probability of not proposing a block in one slot:** $$ 1 - \frac{1}{905,000} $$
- **One Hour (300 slots):** $$ \left( 1 - \frac{1}{905,000} \right)^{300} $$
- **One Day (7,200 slots):** $$ \left( 1 - \frac{1}{905,000} \right)^{7200} $$
- **One Week (50,400 slots):** $$ \left( 1 - \frac{1}{905,000} \right)^{50400} $$
- **One Month (approx. 30 days, 216,000 slots):** $$ \left( 1 - \frac{1}{905,000} \right)^{216000} $$

### Summary
- **Chance of not proposing a block in one hour:** Approximately 99.97%
- **Chance of not proposing a block in one day:** Approximately 99.21%
- **Chance of not proposing a block in one week:** Approximately 94.58%
- **Chance of not proposing a block in one month:** Approximately 78.75%
- **Chance of not proposing a block in 3 months:** Approximately 48.84%
- **Chance of not proposing a block in 6 months:** Approximately 23.86%
- **Chance of not proposing a block in 1 year:** Approximately 5.69%

## Probabilities for 100 Validators

- **Probability of not proposing a block in one slot (for any of the 100 validators):** $$ 1 - \frac{100}{905,000} $$
- **One Hour (300 slots):** $$ \left( 1 - \frac{100}{905,000} \right)^{300} $$
- **One Day (7,200 slots):** $$ \left( 1 - \frac{100}{905,000} \right)^{7200} $$
- **One Week (50,400 slots):** $$ \left( 1 - \frac{100}{905,000} \right)^{50400} $$
- **One Month (approx. 30 days, 216,000 slots):** $$ \left( 1 - \frac{100}{905,000} \right)^{216000} $$

### Summary
- **Chance of not proposing a block in one hour:** Approximately 96.74%
- **Chance of not proposing a block in one day:** Approximately 45.10%
- **Chance of not proposing a block in one week:** Approximately 0.38%
- **Chance of not proposing a block in one month:** Practically 0% (very close to zero)

Finally, this is a simple model yada yada (technically you should look at effective validator balances), if you want to see the latest's statistics on block proposal frequency, see [LuckyStaker.com](https://luckystaker.com/home/)
