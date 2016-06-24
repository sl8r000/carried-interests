---
title: "Deal Carry"
---

I learned the other day that angel/seed stage syndicates often earn "deal carry", a particular type of carried interest that pays out at the **deal level** rather than the **fund level**. This makes sense, since there isn't a persistent "fund" for a syndicate, so deal carry is a pragmatic solution. But to my mind, deal carry is extremely intersting for statistical reasons: there's a selection bias to the payout curve, creating an incentive to take large risk, even at a negative expected ROI. Here's why:

## What is Deal Carry?

Hedge funds, VCs, and private equity firms all earn carried interest in the investments they make, usually at the 20% level. For example: If a VC firm raises $100m, invests it, and later receives (through IPOs, M&A, etc.) $300m back, then the firm has created a profit of $200m. The VC firm keeps 20% of this profit as carried interest; in this case, the firm would get $40m. This is a bit oversimplified because their are things like hurdle rates, high water marks, paybacks for deal fees, etc. But this is the rough picture.

That's how "normal" carried interest works; carry is paid at the fund level. Deal carry, in contrast, is paid out on a deal-by-deal basis. This means that deal carry doesn't require the investor to "pay" for his or her losing investments. The difference is easiest to explain via example.

Let's say our VC firm, with its $100m fund, deploys its cash by investing $5m each in 20 companies. 18 of those companies go bust (go to zero), one of them makes a modest return and sells for $10m, and one of them is sold for $290m. As above, the fund carry in this case is 20% x ($300m - $100m) = $40m. But for **deal carry**, the one company that sold for $300m would generate 20% x ($300m - $5m) = $59m in carried interest. The company that sold for $10m would genrate 20% x ($10m - $5m) = $1m. All the companies that went to zero don't factor in. And all told, the deal carry investor made $60m in carried interest and the fund carry investor made $40m.

(For more examples: As is often the case with subjects like this, Fred Wilson has already written a [great post](http://avc.com/2016/02/fund-level-vs-deal-by-deal-carry/).)

## What does Deal Carry Incentivize?

Deal carry incentivizes more extreme risk taking than does fund-level carry. To maximize payouts, the deal-carry-compensated manager should seek to maximize returns on his or her best deals, rather than on the aggregate portfolio. This means it could be more lucrative to put together a portfolio with a **lower** expected value as long as the variance is sufficiently higher. As an extreme example, let's say that you have $100m to manage. And let's say that on one hand, you have a strategy that very stably, very predictably, turns $100m into $120m over the lifetime of your management by investing in a single company. In that case, your carry would be 20% x ($120 - $100) = $4m. Now let's look at an alternative strategy; You make a hundred little investments of $1m each, each of which has a 99% chance of going to zero, and a 1% chance of returning 50x. The expected value of this portfolio is $50m, meaning that you're **destroying** $50m of capital on average. This is clearly way worse in expectation than your $100m to $120m strategy. But: If you're compensated with deal carry, then you'd actually earn 20% x ($50m - $1m) = $9.8m. You would come out with much more money by following the value-destroying strategy.

A fun thought experiment here is to imagine what deal carry would look like for a hedge fund; you earn 20% on trades that go well, and lose nothing on trades that go south. In such a situation, you'd look for trades that have a lot of upside, without caring much about the downside.

Another interesting thought is think about the financial instrument whose payoff is equivalent to that of deal carry: it's a call option. The value of a call option increases as the volatility of the underlying asset increases; so if you're getting paid in call options when you buy securities, you'd want to buy the most volatile securities possible. Something cool about public markets is that we can see exactly how this plays out by looking at the options chain on publicly traded companies. So let's say that I have an imaginary hedge fund that gets compensated via deal carry. As of this writing, SPY is trading at $208.42 a share, so I could invest $208.42m in SPY by buying 1m shares. For this placement, my 20% carry is equivalent to a call option on 200k shares of SPY at a $208.42 strike. Let's say that we plan to exit in 1 year. Right now, $210 calls on SPY with a 16 June 2017 expiry are trading for about $12.10. So my deal carry of 200k options is worth about $2.42m. But: I could do better if I bought something more volatile, since call options on volatile securities are more valuable. For example, EEM is a more volatile ETF. The same $208.42m investment here would generate about $3.21m of carry. I'm incentivized to take more risk, because at-the-money options on volatile stocks are worth more than at-the-money options on stable stocks.

This bias towards risk is true of "normal" carry too, by the way; but rather than being a call option on each individual investment, it's a call option on the overall fund. Deal carry incentivizes risk-seeking more strongly.

## Tempered Response

Of course, an investment vehicle can't blatently maximize its carry at the expense of its investors (limited partners). Reputation and trust are extremely important in the investing world, and openly exploiting the people who invest in a fund would, of course, destroy the reputation of the fund managers.

At the same time, incentives steer behavior, so it's worth thinking about the incentives that deal carry creates. I think this is particularly true when angel/seed deals are syndicated from a large number of individual investors writing small checks, in which case the LPs are less equipped to police the reputations of their syndicates' managers and probably less familiar with the economics of carried interest.

