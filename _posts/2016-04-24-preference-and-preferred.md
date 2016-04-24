---
title: Liquidation Preferences and Participation Rights
---

I've been reading Feld and Mendelson's excellent *Ventures Deals* book, and was interested to learn that there's a big difference between **liquidation preferences** and **stock participation rights**. Both can significantly affect the economics of a venture deal, but in different ways. Quoting from Feld and Mendelson:

> [For liquidation preferences], a certain multiple of the original investment per share is returned to the investor before the common stock receives any consideration.

> [Fully participating stock] will receive its preference amount and then share in the liquidation proceeds on an as-converted basis, where "as converted" means as if the stock were converted into common stock based on its conversion ratio.

Brad and Feld have an illustrative example for a startup that raises $50M and which investors own 60% of (so a $83.3M post-money valuation). If the startup is acquired for $100M, then:

1. If the investors have a 1x preference and no participation, they will receive 60% or $60M in this case.
2. If the investors have a 1x preference and full participation, they will receive their $50M back and will then receive 60% of the remainder (i.e. 60% of $50M). In total, they'll receive $80M.

Sometimes term sheets are negotiated in which there's a cap to stock participation; if the startup exits below this cap, participation occurs, and if it exits above this cap, it does not.

For me, it's interesting to think about all this for a range of outcomes. What does investor ownership look like if the company is really successful? What does investor ownership look like if the company does a down round? Etc. So I put together a [Jupyter notebook](https://gist.github.com/sl8r000/35003252f53523578d37ebdaa1c43598) that lets you see what happens under different term sheet structures. Let's take another Feld and Mendelson example in which a startup raises $5M at a $10M pre-money valuation ($15M post-money valuation). So the investors own 1/3 of the company. Let's take a 1x liquidation preference as a given, and look at what happens to the economics under different stock participation plans:

![participation](http://i.imgur.com/Od8w3pV.png)

There are three interesting points here:

1. For large exits (in the sense that the exit valuation is much higher than the investment valuation), the percentage-wise impact of stock participation converges to zero like 1/x. However, it still makes a substantial dollar-value difference (see the chart on the left).
2. Participation rights matter much more at small exits, where they can substantially change the economics of the deal.

I think participation rights can be reasonable depending on the circumstances. If, for example, a founder things the valuation of his or her company should be much higher than investors believe, then prudently-capped participation rights could be a reasonable compromise. On the other hand, irresponsible participation rights could really harm the economics of the business for the founder. I think the lesson is: It's important to think about how liquidation preferences and participation rights affect the deal, and to make sure the outcomes at different exit valuations are fully understood.