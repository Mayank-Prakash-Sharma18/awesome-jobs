---
title: "Option Greeks – Delta, Gamma, Theta, Vega, RHOP"
date: 2022-10-12T10:08:18+06:00
# post thumb
images:
  - "images/post/option-greeks.png"
#author
author: "Mragank Shandilya"
# description
description: ""
# Taxonomies
categories: ["entrepreneur"]
tags: ["extra-income","money-online","share-market-trading"]
type: "epic" # available type (epic, trending, popular, or regular)
draft: false
---

In this article, we are going to understand the concepts of various Option Greeks. This will allow us to comprehend many other concepts related to options trading, such as premium decay, etc. 

<div class="toc-mak">
<img src="../../images/pencil.png">
<b>Table of Contents</b>
<ul>
<li>What are Option Greeks?</li>
<li>What is Delta (δ) Option Greek?</li>
<li>What is Gamma (γ) Option Greek?</li>
<li>What is Theta (θ) Option Greek?</li>
<li>What is Vega (ν) Option Greek?</li>
<li>Inter Greek Interactions</li>
<li>What is Rho (ρ) Option Greek?</li>
</ul>
</div>

## What are Option Greeks?

In laymen’s terms, Option Greeks are the outside forces that work on an option contract in real time, and increase or decrease the premium on a minute-by-minute basis. For example, Spot Price Change, Volatility, Time, etc. 

Options Greeks not only affect the premium directly, but also affect each other. This further increases the complexity of the system. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

Option Greeks are market driven values and are computed by the Black & Scholes (B&S) formula. You may use B&S option pricing calculator to find their exact values. 
</div>

Now, let’s have a look at the various Option Greeks one by one. 


## What is Delta (δ) Option Greek?

Delta of an option measures the rate of change of options premium based on the directional movement of the underlying asset. In other words, it tells us how much the premium of an option will change based on the change in the price of the underlying asset – how much will it change if spot price goes up or down 1 point? 

So, the value of the option premium changes as the spot price changes. 
* The call option premium increases with the increase in the spot value and vice versa. The value of delta Greek varies between 0 and 1 (or 0 and 100) for call option. 
* The put option premium decreases with the increase in the spot value and vice versa. The value of delta Greek varies between 0 and -1 (or 0 and -100) for put option.

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

The value of delta is always between 0 and 1 for a call option because:

* If delta is above 1, then it will mean that the option value is moving faster than the value of the underlying asset. This is not possible because option is a derivative contract – it drives its value from the underlying asset. Howe can it move faster than that?

* If delta is below 0, then it will mean that the option value is moving in the opposite direction than the value of the underlying asset – if the value of the underlying asset is increasing, the value of the call option is decreasing! This is not possible because the value of call option is supposed to increase with an increase in the price of the underlying asset (it is put option that decreases in value if the price of the underlying asset increases). Also, if delta is below 0, then there is a possibility for the premium to go below 0, which is impossible (premium of a call or put option can never be negative).

We can extend a similar logic to pull options. 
</div>

Let’s consider one example to better understand this concept. 

If delta for a call option is 0.8 (or 80), then it means that for every 1 point change in the underlying asset, the premium is likely to change by 0.8 points. 

Also, if option strike = 8250 Call Option; Spot price of option = 8300 at 10 AM; Spot price of option is expected to go up to 8400 by 11 AM; Premium = Rs. 150

Can you find out the premium value at 11 AM?

Expected change in spot price = 8400 – 8300 = 100 points <br>
As the spot price is increasing, the value of premium for a call option will increase. <br>
The new premium = old premium + change = old premium + (change in spot price × delta) = 150 + (100 × 0.8) = 150 + 80 = Rs. 230 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

If spot price would have fallen, the value of premium of call option would have fallen too. 
</div>

If everything else is same, we should aim to buy an option with higher delta Greek value. For example, if two call options have delta values of 0.1 and 0.2, then you should buy the call option having delta of 0.2. That’s because, if the price of the underlying asset moves in the right direction (after we have bought it), the premium value of our option will also rise faster, i.e. we will make more profit. 

### Delta of ATM, ITM and OTM options

* ITM options have a delta value between 0.5 and 1.
* ATM option has a delta of 0.5.
* OTM options have a delta value between 0 and 0.5.

However, as spot price of the underlying asset changes, the moneyness of the option may change. This will change the delta value too. So, delta is not a constant value – it keeps on changing as spot price of the underlying asset changes. 

Let’s consider some examples for option strike = 8250 Call Option. 
* If Spot price = 8300. It means that, 8250 CE is an ITM option. So, its delta value must be between 0.5 and 1.
* If Spot price = 8250. It means that, 8250 CE is an ATM option. So, its delta value must be 0.5.
* If Spot price = 8200. It means that, 8250 CE is an OTM option. So, its delta value must be between 0 and 0.5.
The logic is similar for put options too. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

No matter how much the spot price rises, going from ITM to deep ITM, the call option’s delta will remain at 1. 

No matter how much the spot price falls, going from OTM to deep OTM, the call option’s delta will remain at 0. 
</div>

### Stages in Delta Value Movement

The value of Delta Greek moves up and down in a particular order. To understand this, experts often divide this delta value movement in four stages: Predevelopment, Take-Off, Acceleration, and Stabilization. 

We will be able to understand these stages better if we take help of an example. Let’s assume that the call option bought by us is 8300 CE. 

***Predevelopment Stage***: When the option transitions from Deep OTM to OTM

* We bought this call option when it was a Deep OTM, say when the spot price was 8000. The delta then must have been very close to 0, say 0.05. The premium must have been very low too, say it was Rs. 10.
* If the spot price now moves up to 8100, the option will become an OTM. However, the value of the delta will still not move up much – it will still be very near to 0, say 0.06. The premium will also not appreciate much. The change in premium = change in spot price × delta = (8100 - 8000) × 0.05 = 100 × 0.05 = Rs. 5. So, new premium = 10 + 5 = Rs. 15. 

So, as Deep OTM changes to OTM, the absolute change in premium is small. But percentage-wise, the change is huge. In the above example, premium changed from Rs. 10 to Rs. 15, a change of 50%!

But we will see such large percentage changes only if the spot price changes by a huge margin. So, in general we should avoid buying deep OTM, as the deltas are very small. 

***Take-Off Stage***: When the option transitions from OTM to ATM

You stand to gain the maximum if option changes from OTM to ATM. 
* Say the spot price is at 8150. Here, 8250 CE is slightly OTM. Delta may be 0.25. Let the premium be Rs. 20. 
* If the spot price moves up to 8250 (or any value near 8250), the call option will become ATM. Delta value of ATM option is always 0.5. The change in premium = change in spot price × delta = (8250 - 8150) × 0.25 = 100 × 0.25 = Rs. 25. So, new premium = 20 + 25 = Rs. 45. 

So, as OTM changes to ATM, the absolute change in premium is small. But percentage-wise, the change is huge (much higher than in the case of transition of deep OTM to OTM). In the above example, premium changed from Rs. 20 to Rs. 45, a change of 125%!

So, as compared to the transition from Deep OTM to OTM, we get to see much higher percentage change in premium when OTM changes to ATM, even when the change in spot price was the same. This is because of the higher delta value in OTM as compared to Deep OTM. 

So, if you buy a slightly OTM option, and the price moves in the favourable direction, you will book huge profits – even double or triple your capital. However, even here the spot price will need to move a lot for you to book profits. Also, there should be plenty of time for the expiry of the option. So, because of these reasons it’s still a bit risky to buy slightly OTM options. 

***Acceleration Stage***: When the option transitions from ATM to ITM

A lot of trade experts buy ATM options and hope for it to move to ITM. 
* Say the spot price is at 8250. Here, 8250 CE is ATM. Delta will be 0.50. Let the premium be Rs. 45. 
* If the spot price moves up to 8350, the call option will become ITM. Delta value of ITM option is always between 0.5 and 1. The change in premium = change in spot price × delta = (8350 - 8250) × 0.50 = 100 × 0.50 = Rs. 50. So, new premium = 45 + 50 = Rs. 95. 

So, as ATM changes to ITM, the absolute change in premium is pretty good. Also, percentage-wise, the change is huge. In the above example, premium changed from Rs. 45 to Rs. 95, a change of more than 100%!

So, ATM options are more sensitive to changes in the spot price as compared to OTM options. Even a slight variation in the spot price will create large changes in the premium. That’s why a majority of traders buy ATM option. However, to buy an ATM option, you will also have to pay a larger premium as compared to OTM options. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

Most experts suggest intra-day traders to buy ATM or slightly OTM options. 
</div>

***Stabilization Stage***: When the option transitions from ATM to ITM to Deep ITM

As the option moves from ATM to ITM and Deep ITM, the delta value moves towards 1, and starts to stabilize at 1. 
* Say the spot price is at 8350. Here, 8250 CE is ITM. Delta may be 0.75. Let the premium be Rs. 95. 
* If the spot price moves up to 8450, the call option will become Deep ITM. The change in premium = change in spot price × delta = (8450 - 8350) × 0.75 = 100 × 0.75 = Rs. 75. So, new premium = 95 + 75 = Rs. 170. 

In the above example, premium changed from Rs. 95 to Rs. 170, a change of less than 100%!

So, if we compare the transition from ATM to ITM, with transition from ITM to Deep ITM, we can see that in absolute terms the premium rises much more when option moves from ITM to Deep ITM. However, in percentage terms transition from ATM to ITM is more beneficial. Traders buy ITM when they want to play safe – though premiums that you have to pay for ITM options are higher, the chances of you making a profit are also higher. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

When delta is 1, it means that the value of the option contract will move in line with the underlying asset. So, a change of 1 point in the underlying asset will lead to a change of 1 in the option contract. 

In other words, if delta value is 1, buying the option contract is as good as buying the underlying asset itself, or buying a futures contract. For every point change in the underlying’s spot value the futures also changes by 1 point, i.e. if we were to assign a delta value to futures, the future’s delta value would be 1. However, keep in mind that futures contract is only affected by the direction of the market (i.e. spot price change), but the options contracts are affected by many other variables besides the direction of spot price change.

That’s why some traders often buy Deep ITM option rather than buying the underlying asset directly. It allows them to lessen their margin burden. However, if you do so, you will have to constantly make sure that the delta value remains at 1 (i.e. make sure that Deep ITM option continues to remain Deep ITM). You will also have to keep an eye on the liquidity of the contract.
</div>

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

OTM options have low premium, low rewards (in absolute terms, not percentage-wise), and low chances of booking a profit. So, it’s less risky as you need to invest less, but it’s riskier as your chances of booking profit are less. Some experts do buy slightly OTM options sometimes when they expect a huge swing in the spot price, but only once in a while. 

ATM options have medium premium, medium rewards, and medium chances of booking a profit. Most experts prefer to trade in ATM or slightly ITM options. 

ITM options have high premium, high rewards (in absolute terms, not percentage-wise), and high chances of booking a profit. So, it’s riskier as you need to invest more, but it’s less risky as your chances of booking profit are more.
</div>

### Adding Deltas

If you have bought multiple options of the same underlying asset, you may add up their deltas. Even the deltas of the call and put options can be added together. 

For example, if a trader has three options having deltas 0.30, 0.80, -0.20, then: <br>
Their combined delta = 0.30 + 0.80 – 0.20 = 0.90 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

Owning two ATM option is equivalent to owning one futures contract. That’s because, delta of ATM option is 0.5. So, combined delta of two ATM options = 0.50 + 0.50 = 1. 
</div>

### Delta as a probability

The Delta of an option is also the probability for the option to expire In-the-Money (ITM). In other words, Delta also gives us the probability of us making a profit. 

If delta of an OTM option is 0.4, then it means that we have 40% chance of making a profit if we buy that option, i.e. for the option to transition from OTM to ITM. 

Now, if the delta of a Deep OTM option is 0.1, then it would mean that you only have 10% chance of making a profit. And if there are only 3 days left for that option to expire, will you buy that option contract, even if it has very low premium? – Most expert traders won’t. However, selling such an option makes sense, as there is 90% chance for the option to expire as an OTM option. 


## What is Gamma (γ) Option Greek?

Gamma of an option measures the rate of change of delta itself. 

Unlike delta, which can be positive or negative, gamma is always a positive number for both call and put options. 

Let’s try to understand it better. 
* Delta is the first order derivative of the premium, as it measures the change in premium with respect to change in the underlying asset. This is similar to velocity, which measures the change in distance with respect to change in time (and so is the first order derivative of position).
* Gamma is the second order derivative of the premium, as it measures the change in delta with respect to change in the underlying asset. This is similar to acceleration, which measures the change in velocity with respect to change in time (and so is the second order derivative of position).

Now, let’s consider an example. This will make things even clearer. 
* If spot price is 8200, then call option of 8300 CE will be considered as OTM. Let’s assume that delta value of this option is 0.3 (we know that delta value of OTM option is between 0 and 0.5).
* If spot price now rises to 8400, then call option of 8300 CE will be considered as ITM. The delta value of this option will also rise, say it becomes 0.7 (we know that delta value of ITM option is between 0.5 and 1).
Now, to find the gamma Greek, we need to use calculus (differential equations and stochastic calculus).

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

The gamma of a future contract is zero. That’s because the delta of a futures contract is always 1, it does not change. So, rate of change of delta is zero. 
</div>

### Calculating Delta using Gamma

Gamma may also be defined as the deltas gained or lost per one-point change in the underlying asset value. 

In other words, delta increases by the amount of the gamma per unit increase in the underlying asset. And, delta decreases by the amount of the gamma per unit decrease in the underlying asset.

So, New Delta = Old Delta + Change in Delta = Old Delta + (Gamma × Change in the value of underlying asset)

Let’s consider an example.

Call option 8210 CE; Bought when spot price was 8000. So, the option was slightly OTM.

Let its premium be Rs. 20; Delta be 0.10; Gamma be 0.0020

If the spot price rises to 8200, what will be the new premium, delta, and moneyness?

The moneyness now is ATM. 

New premium = Old premium + (Delta × Change in Spot Price) = 20 + (0.10 × 200) = 20 + 20 = Rs. 40 <br>
New Delta = Old Delta + Change in Delta = Old Delta + (Gamma × Change in Spot Price) = 0.10 + (0.0020 × 200) = 0.10 + 0.40 = 0.50 (we have added the change, as we know that call option gains delta when spot price of the underlying asset increases)

Some more tips related to Gamma:
* The premium for OTM options doesn’t change much in terms of absolute point terms (even though the change is bigger in percentage terms). For example, if the premium of an OTM option changes from Rs.2 to Rs.2.5, the absolute change is just 50 paisa, but the percentage change is 25%. That’s because gamma value is low for OTM Options.
* ATM option has the highest gamma. This essentially means that, rate of change of delta is highest for ATM options, which in turn implies that ATM options are most sensitive to the changes in the underlying asset. (Since ATM options have the highest Gamma, you should avoid shorting ATM options.)
* The gamma value is low for ITM Options too (just as OTM), but the delta for ITM options is pretty high (between 0.5 and 1). That’s why the ITM delta reacts slowly to the change in spot price of the underlying asset (due to low gamma), but still the change in premium is big (due to high base value of delta).

So, remember this:
* ATM option has the highest gamma. So, delta changes rapidly for ATM option. 
* OTM and ITM options have lower gamma. So, delta changes slowly for OTM and ITM options.
* As ATM options have high gamma, you should never short them (with a hope that they will expire worthless upon expiry). Same holds true for ITM options. 
* You may short OTM options, as they have low gamma (if you intend to hold these short trades until expiry wherein you expect the option to expire worthlessly).

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

* When you buy options (Calls or Puts) you are long Gamma.
* When you short options (Calls or Puts) you are short Gamma.
</div>


## What is Theta (θ) Option Greek?

Theta of an option measures the impact on premium based on time left for expiry. 

The aim of option buyers is to buy an option that expires in ITM. While, aim of option sellers or writers is to sell an option that expires valueless in OTM. The more the time left for the expiry of an option, more is the chance that it may eventually end up in ITM. 

So, more the time left for expiry, the better it is for option buyers. On the other hand, time is a risk factor for option sellers. More the time left, more the risk an option seller is taking. As the time passes, option sellers pocket more and more premium and option buyers keep on losing premium (called premium decay). 

We can understand it better with the help of an example.

Suppose we buy a 8200 CE option, when the spot price is 8000. So, this option is OTM. What is the probability that it will eventually expire in ITM? Well, it depends on time left for its expiry. 
* Say, if one month is left for the expiry of the option, then the probability of this OTM option to eventually expire as ITM is pretty high. This is good for option buyer, but bad for option seller. So, seller will charge more premium for such an option. 
* However, if only 2 days are left for the expiry of the option, then the probability of this OTM option to eventually expire as ITM is pretty low. This is bad for option buyer, but good for option seller. So, seller will charge less premium for such an option, as he wants to attract more traders to buy his option contract.

While studying the delta Greek we saw that the premium paid by option buyers is for the intrinsic value of the option (intrinsic value depends on the money you will receive if you were to exercise your option today). But now, we can see that the premium we pay also depends on the time factor. 

So, Premium = Intrinsic Value + Time value

Let’s consider the previous example again. 

Suppose we buy a 8200 CE option for a premium of Rs. 100, when the spot price is 8000. <br>
So, this option is OTM. We know that the intrinsic value of OTM option is always 0. So, the premium option buyers are paying is just for the time value of that option. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

The premium value not only depends on intrinsic value (which in turn depends on the spot price), and time factor, but also on the volatility (generally measured by India VIX). As volatility increases, premiums increase too. We will study about the volatility factor later on in this article. 
</div>

So, when you buy an option, keep in mind that it’s a depreciating asset (other things being constant). Premium of an option erodes daily, be it a call or put option. But by how much?

Theta Greek is used to answer this question. It tells us by how much the premium of an option erodes per day. 

Other conditions remaining constant, theta is the points lost in premium per day, i.e. it is the rate at which an option loses its value with time. That’s why theta is also known as Time Decay Factor. 

Theta is always positive because time moves in one direction, and with time any kind of option will lose value. Though often theta is expressed as a negative number (for option buyers), because it leads to loss in the value of an option. 

Let’s see an example.

If an option is trading at Rs.3.75 with a theta of -0.05, then:
* the next day it will trade at Rs.3.70,
* the next to next day it will trade at Rs. 3.65, and so on. 
 (provided other things are kept constant).

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

* A long option (option buyer) always has a negative theta. It means that, the option buyer will lose money on a day-by-day basis. 

* A short option (option seller) always has a positive theta. It means that, the option seller will gain money on a day-by-day basis. So, theta Greek works in favour of the option seller.
</div>

### Change in Theta

The value of theta does not remain constant. It keeps on changing as expiry date arrives. Let’s understand how theta changes with time. 
* If a lot of days are remaining for the expiry of the option, theta value is low. So, option does not lose much value quickly. Sellers can pocket large premiums in such a case – as a lot of time is remaining before the option expires, the time value of option is high. As effect of theta is less, premium will decay slowly. 
* If only a few days are remaining for the expiry of the option, theta value is high. So, option loses much value quickly. Sellers cannot pocket large premiums in such a case – as not much time is remaining before the option expires, the time value of option is low. As effect of theta is more, premium will decay quickly. 

So, do keep in mind that theta increases with time; closer we get to the expiry date, the more will be the value of theta.  

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

If the underlying asset is showing a sideways movement, then delta will not have much effect on the premium value. Rather theta will keep on eroding its premium. That’s why options buyers avoid trading during sideways movement of the underlying asset. However, if the market moves in our favourable direction, the premium will increase, which may overshadow the premium decay due to time elapsed. 
</div>


## What is Vega (ν) Option Greek?

Vega of an option measures the rate of change of premium based on change in volatility. 

So, before we talk about Vega, we need to understand the concept of volatility. Volatility may be of three kinds, which are as follows:
* Historical Volatility: To calculate the historical volatility we take into account the past closing prices of the stock/index. 
* Forecasted Volatility: It is the prediction of volatility over the desired time frame. Predicting the volatility of option is important as profitability of many option strategies depends on the expected volatility. In fact, many option traders find it more efficient to forecast volatility, than to forecast market direction. Yes, as an option trader you need not even have a view on the direction of the markets – some traders just focus on volatility prediction. Professional traders use volatility forecasting statistical models such as ‘Generalized AutoRegressive Conditional Heteroskedasticity (GARCH) Process’, specifically GARCH (1,1) or GARCH (1,2), which are considered better in forecasting volatility.
* Implied Volatility (IV): It represents the market participant’s expectation on volatility. While Historical Volatility and Forecasted Volatility are kind of manufactured, Implied Volatility is consensus based – a consensus amongst market participants with respect to the expected amount of underlying price fluctuation over the remaining life of an option. As Implied Volatility affects the premium price, it is considered the most significant kind of volatility amongst all three. An example of implied volatility index in Indian stock market is India VIX on NSE website, which is the official ‘Implied Volatility’ index in NSE. It represents the implied volatility over the next 30 days period. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Volatility Smile</b><br>

Though ideally, all the options that are derivatives of the same underlying asset and having the same expiry day should have the same IV, but that’s not the case. Implied Volatility (IV) of ITM, ATM and OTM options vary. This phenomenon is often referred to as Volatility Smile.

Implied Volatility (IV) is the least for ATM option. As we move away from ATM option (towards ITM or OTM), the Implied Volatility (IV) increases. This is true for both call and put options. 
</div>

Once the option expires, we may look back at the actual volatility that occurred during the expiry series, which is called ***Realized Volatility*** (as it’s in the past – it already has been realized). Looking at past Realized Volatility data may be useful and is used in some option trading strategies. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Volatility cone</b><br>

Volatility Cone is a graphical representation of the historical realized volatility.

The concept of Volatility cone helps options traders to evaluate the costliness of an option, i.e. it helps them identify options that are trading costly/cheap. 

Not only can this be done across various options based on the same underlying asset (i.e. different strikes of a security), but also across different securities as well.

A trader can plot volatility cone for stocks and overlap it with the option’s current IV. In a sense, the volatility cone helps us develop an insight about the state of current implied volatility with respect to the past realized volatility.

Experts suggest traders to short options which are costlier and go long on options which are trading cheap.
</div>

Now, let’s understand Vega Greek. 

When volatility increases, we witness large swings in the price of stock/index. For example, if volatility is high, a stock trading at Rs. 100 may start swinging heavily between Rs. 90 and Rs. 110. This is bad news for option sellers (for both call and put), as with high volatility the chances of options expiring in ITM increase. That’s why as volatility increases (or is expected to go up), the premiums of both call and put options go up. 
* More the days left for expiry of an option, more is the effect of increase in volatility on premium price. So, premium price varies a lot. If an option seller writes such an option, he may gain the differential in premium once the volatility (and hence the premium swing) cools down. 
* Less the days left for expiry of an option, less is the effect of increase in volatility on premium price. So, premium price varies a lot less. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Note</b><br>

Theta favours option sellers. While, Vega favours option buyers. In other words, Vega favours long positions, while it works against short positions. 

However, as per some experts if you see very high IV (above 20%), you should avoid buying the option. As volatility will decrease (ideally below 9%), the premium will decrease too. 
</div>

So, we know that with increasing volatility, the premium increases too. Vega Greek tells us by how much. 
That is, Vega measure the rate of change of premium (i.e. option’s value) with every percentage change in volatility.

As premium always increases with increase in volatility (for both call and put options), it is always a positive number. 

Now, let’s consider an example. 

If an option has a vega value of 0.20, then for each percentage change in volatility, the option will gain or lose 0.20 in its theoretical value.


## Inter Greek Interactions

Now, as we mentioned it earlier in this article, these Greeks not only affect the premium directly, but they affect each other too. So, their affect is multidimensional, not unidimensional. They generally work together, not one at a time. 

So, we have to consider all these factors while calculating the value of an option (i.e. its premium):
* direction of market (gauged by delta)
* time left for expiry (gauged by theta)
* volatility (gauged by vega)
* liquidity of the options

Let’s consider a couple of such Greek interactions.

### Change in Gamma with Time

As the spot price of the underlying asset changes, the gamma also changes (and not only delta). This change in gamma is calculated using the third derivative of the underlying asset, which is called Speed, Gamma of Gamma, or DgammaDspot. But for all practical purposes retail traders may ignore it. It comes into play when you are trading millions of rupees. 

But we may highlight a general trend:
* When there’s a lot of time left for expiry: All three options ITM, ATM, OTM have low Gamma values. Gamma of ITM options tends to be lower as compared to ATM or OTM options.
* When options are half way through the expiry: The gamma values for all three (ATM, OTM, ITM) remain fairly constant.
* As we approach expiry: ITM and OTM options race towards zero gamma. While, gamma of ATM option increases drastically. 

<div class="toc-mak">
  <img src="../../../images/pencil.png">
  <b>Shorting options</b><br>

Shorting options is considered risky, because of the change in the value of gamma. When you short options, you need to be aware of the Greeks and what they can do to your positions. 

Specifically, try to avoid shorting option contracts that have a large gamma, e.g. ATM options near the expiry date. 

But even if you short option contracts that have a low gamma, there’s always a risk of the gamma getting large with time. So, you need to keep monitoring. 

Also, monitoring gamma value change across time involves interaction of various variables – option strike, gamma, and theta (time to expiry). So, it’s a bit complex to understand, visualize, and make use of while trading. 
</div>

### Delta versus Implied Volatility (IV)

We already know that, delta of deep ITM options is 1 (for call) and -1 (for put).

As strike price increases, the call option changes from ITM to ATM (delta of 0.50) and then OTM (delta of 0). 

Also, as strike price decreases, the put option changes from ITM to ATM (delta of -0.50) and then OTM (delta of 0). 

However, the way delta changes from ITM to OTM depends on Implied Volatility (IV). 
* When IV is low, the rate at which delta changes is low near the ITM and OTM range, which means that the rate at which the option premium moves is low. That is, deep ITM options tends to behave exactly like a futures contract (when volatility is low) and OTM option prices will be close to zero. 
* But the delta changes quickly near the ATM even when volatility is low. In other words, only a small range of options around ATM are sensitive to spot price changes, when volatility is low.
* When IV is high, the rate at which an option’s premium changes with respect to change in underlying asset is high. The change is kind of uniform from 1 to 0 (for call), or from -1 to 0 (for put). In other words, a large range of options around ATM are sensitive to spot price changes, when volatility is high. 
* Also, the far/deep OTM options do tend to have a non-zero delta value if volatility is high. 


## What is Rho (ρ) Option Greek?

Rho essentially measures an option's sensitivity to changes in the risk-free rate of interest, e.g. to changes in interest rates set by RBI (in case of India). 
* Premium of call options rises as interest rates increase. Call options have positive Rho. 
* Premium of put options decreases as interest rates increase. Put options have negative Rho.

Rho Greek has almost negligible effect on option trading, at least in the Indian market. 
