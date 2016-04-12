---
layout:     post
title:      Deal Access in Venture Capital
date:       2016-04-03
summary:    Does access to deals explain venture capital returns?
categories: venture
---

Venture capital is famous for performance persistence: The VC firms that were top quartile in the last (say) 10 year period are likely to be top quartile in the next 10 year period. As an investor, you'd hope that all your asset managers have this property, but it isn't so. If you've read Khaneman's *Thinking Fast and Slow*, for example, you know that mutual funds don't appear to have performance persistence; last year's top quartile fund and last year's bottom quartile fund have
roughly the same chance of being top quartile next year.

VC, though, [is different](http://faculty.chicagobooth.edu/steven.kaplan/research/HJKS.pdf). Performance persists, and firms that have done well in the past seem to do well in the future.

I've often wondered why this is true. In talking to folks in the industry, I hear two primary theses:

1. Top VC firms have a superior ability to predict which startups will be successful. (That is, top VCs are better at picking winners.)
2. Top VC firms have a superior ability to help and nurture startups to success. (That is, top VCs are better at *making* winners.)

Sometimes I hear a third hypothesis, which is:

3. Top VC firms have a superior ability to gain access to favorable fundraisings. (That is, top VCs are better at getting in on good deals.)

This last idea interests me, because it suggests that gaining a seat at the table to fund a great company is a determinant of VC success. The mental picture I have is the following: A great founder forms a great company, and gets early traction. He or she decides to raise money, so they start talking to "top" VC firms: They reach out to Sequoia, Benchmark, Kleiner Perkins, etc. They're a great startup, so this top tier of VCs happily invests. Thus, the top quartile VCs get in on a great company.

On the other hand, a less great founder forms a less great company, and doesn't get as much early traction. When he or she decides to raise money, they also start with top VC firms; but this time, Sequoia, Benchmark, and Kleiner Perkins pass on the deal. They recognize that the company isn't so hot, so they decline to invest. The founder then solicits funding from a lower tier of VCs. And a lower tier. And a lower tier. Until someone bites the apple. Let's say that the founder had
to go all the way to the bottom quartile.

So the great company went to the top quartile VCs, and the bottom quartile VCs never had any chance to get in on the deal. And the less great company was rejected by the top VCs, and thus a bottom-quartile VC ended up investing. This is interesting, because it suggests that top VCs remain top VCs (performance persists) because they get access to the best deals -- by virtue of being percieved as top VCs by founders! Sort of a self-fulfilling prophecy.

Is this idea plausible? It's hard to answer definitively without knowing:

1. For each VC firm, every deal they had access to.
2. For each startup, every VC firm they tried to raise money from.

But maybe we can at least probe the idea through some other means. First, a simple math thought experiment in which founders and VCs interact. Second, some data from CrunchBase.

## Simple Thought Experiment

Let's imagine a simple scenario in which there are just two VC firms: A "top" VC, and a "regular" VCs. There are some startups, each of which is worth a unicorn (worth $1B) or a dud (worth $0); each startup has a 2% chance of being a unicorn. The VCs are equally skilled: When a startup asks a VC for money, that VC has an 80% chance of correctly perceiving whether that startup is a unicorn, and a 20% chance of a random perception. By random perception, we mean flipping a coin to guess whether the company is a unicorn. Every startup asks the top VC for money first, and goes to the bottom VC only if the top VC declines.

So how do our VCs do? Let's run this with 1M startups to get the law of large numbers to kick in:

```
n_startups = 1000000
prob_unicorn = 0.02
prob_truth_perceived = 0.8

top_unicorns = 0
top_investments = 0
other_unicorns = 0
other_investments = 0

for i in range(n_startups):
    is_unicorn = np.random.binomial(1, prob_unicorn)
    top_vc_perceives_truth, other_vc_perceives_truth = np.random.binomial(1, prob_truth_perceived, size=2)
    
    top_vc_wants_deal = top_vc_perceives_truth*is_unicorn + (1-top_vc_perceives_truth)*np.random.binomial(1, 0.5)
    other_vc_wants_deal = other_vc_perceives_truth*is_unicorn + (1-other_vc_perceives_truth)*np.random.binomial(1, 0.5)
    
    if top_vc_wants_deal:
        top_investments += 1
        top_unicorns += is_unicorn
    elif other_vc_wants_deal:
        other_investments += 1
        other_unicorns += is_unicorn
        
print top_unicorns, top_investments
print other_unicorns, other_investments
```

In a run of this, top VCs made 116,415 investments of which 18,043 were unicorns, and other VCs made 89,996 investments, of which 1781 were unicorns. So about 15.5% of top VC investments were unicorns and about 2% of other VC investments were unicorns; more than 91% of unicorns went to top VCs. Remember, by "top" here just means that startups prefer these VCs; these VCs get more deal access, but otherwise are the same as other VCs.

This thought experiment doesn't prove anything, it just shows how the math would work out in practice.
