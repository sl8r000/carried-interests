Stock options for non-executive employees aren't common in most of corporate America, but for Silicon Valley startups they are the norm. Granting stock options is a way for companies to compensate employees at a time when they don't have a lot of cash on hand. Theoretically, granting options also aligns incentives, since it connects the economic interests of employees to the success of the firm.

So in general, options make sense. But: Options are also much more complicated than cash, so I want to talk about a few ways in which typical employee option plans lead to counterintuitive incentives for employees.

# The Curse of Success

Bob joins Initech right after its Series B, and is granted 20,000 stock options at a strike price of $1.00. Two years later, Initech raises it's Series D, at a price per (preferred) share of $50.00. Ignoring the difference between preferred and common stock, Bob's option grant is now worth 20,000x(50.00-1.00) = $980,000.00. Bob has been a valuable employee, so he is granted another 20,000 options starting in his second year; the rub, though, is that the strike price is now $40.00. So
Bob has:

* 20,000 shares from his initial grant at a $1.00 strike.
* 20,000 shares from his new grant at a $40.00 strike.

In other words, because Initech has been successful, the 409A price (which sets Bob's strike price) has risen from $1.00 to $40.00. The problem, from a compensation point of view, is that Bob's new options are worth a lot less than his old ones. While his old options are worth $49.00 each (again, ignoring common/preferred differences), his new options are worth $10.00 each.

If Initech "levels off" at around $50.00 a share (maybe in the next couple of years, the price creeps to $55.00, but 10x returns are a thing of the past, and outsize windfalls are over), this means that Bob's future compensation is dwarfed by his initial grant. From an economic point of view, this might make sense: Bob should be compensated for joining Initech early and contributing to its success. From a retention point of view, though, this is bad: Bob's future earnings potential at Initech is small relative to his initial grant.

Bob might thus be incented to "rest and vest" rather than work hard. Put another way: Bob is going to earn about $1M as long as he doesn't get fired. If he works really hard, maybe he'll get another 5,000 shares at a $40.00 strike -- worth a total of $50k. Will Bob be motivated to work hard for $50k when he has $1M already?

# Ownership Stake

[Sam Altman](http://blog.samaltman.com/employee-equity) has already written about this issue, but the point bears repeating: Employees options grant are often not meaningful enough to align incentives. Even in sub-$100M valuation companies, it's not uncommon for an individual employee's option grant to represent less than 0.01% of the total equity. From a self-maximizing, payout-oriented point of view: This employee is indifferent between

1. Adding $1M to the company's valuation.
2. Earning $100.00 on the side.

(2.) is much easier than (1.), so we wouldn't expect a self-maximizing employee to work very hard at increasing firm value.

# Join Date Envy

This is more of an emotional point than an economic one, but I imagine it also effects behavior: During the growth stage of a company, slightly different join dates may result in significantly different compensation for two people doing exactly the same job. Let's look at Etsy, for example. Here are a few strike prices listed in [Etsy's S1](https://www.sec.gov/Archives/edgar/data/1370637/000119312515077045/d806992ds1.htm)

| Grant Date | Exercise Price per Share |
|---|---|
| January 2013 | $2.38 |
| May 2013 | $2.79 |
| September 2013 | $3.01 |
| February 2014 | $4.13 |
| April 2014 | $5.18 |
| July 2014 | $5.23 |
| November 2014 | $6.19 |
| January 2015 | $8.50 |

Etsy announced it's IPO in March, 2015. The lockup expiration was on 13 October 2015, on which date the stock price was $11.60.

My experience, which may not generalize, is that grant sizes don't vary hugely from 409A to 409A at later stage startups. So, to me at least, it's not implausible that someone joining in February 2014 might get the same number of options as someone joining in April 2014. However, on the lockup expiry date:

* The person who joined in February 2014 has options that are worth (intrinsic value) $7.47 each.
* The person who joined in April 2014 has options that are worth (intrinsic value) $6.42 each.

These effects are magnified when the stock's trading price is closer to the strike price. Today (Sunday 10 April 2016), for example, ETSY trades for $8.26. With this price:

* The person who joined in February 2014 has options that are worth $4.13 each.
* The person who joined in April 2014 has options that are worth $3.08 each.

In other words, the February 2014 person's grant is about 34% more valuable.

What's strange about this is that the join date may determine someone's compensation more than performance, even when the difference is just two months! If the initial grant was 80,000 shares, for example, than the value in joining in February rather than April is $84k.

# Conclusions

My goal isn't to tear down options as a compensation mechanism: the aim is to call attention to some consequences of options that may not be obvious at first. For companies who don't have the cash to offer competitive salaries, stock options a great way to attract and compensate employees. They're just a bit more complicated than one might think.

In the spirit of suggesting a solution rather than just raising problems, here's an idea I had (which may be bad, impractical, or both): Offer "cash like" compensation through equity. For example, perhaps a certain equity account could be held aside for employees. During a liquidation event, this account would be sold and used to pay employees. I'll call "cash like" compensation from this account a "promise". A compensation offer  might look like the following:

* Cash compensation of $150k.
* Up to $250k of cash from the proceeds of the account sale. (That is, a $250k "promise".)

If the proceeds from the sale more than cover all promises, than the excess is shared equally amongst all employees. If the proceeds from the sale aren't enough to cover all the promises, then everyone would be paid n a pro-rata basis. I think the advantages of this approach are:

* It avoids 409A complications. This should help with the curse of success and the join date envy.
* It puts compensation closer to a dollar value, which is easier to understand.
* Compensation could be decided year-by-year, rather than having a tax-incentive to follow the typical 4-year vest, 1-year cliff structure.

One major downside of this plan is that it doesn't allow some employees, who may be crucial, to participate in outsize returns: If the value of the employee account ends up 10x the sum total of all promises, then after this star employee is paid all his or her promises, he or she is "only" compensated the same as other employees. One possible answer to this would be that star employees should be recognized with larger promises.

