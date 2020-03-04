---
title: Lending Club Investing Performance, Part 1
date: 2020-03-01 19:34:30 Z
excerpt: This is the first in a series of posts analyzing my investing performance in peer-to-peer lending notes. 
header:
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280,h:380,fit:crop/compress/3vLHQUvRxyMfKDpkJD8N"   
  overlay_filter: 0.5 
  caption: "Photo by Fabian Blank on Unsplash"  
categories:
- Post
tags:
- Data
- Python
- Finance
last_modified_at:  2020-03-04 01:10:00 -0500
project_id: lc_analysis_2020  
---



## Introduction 
This is the first in a series of posts analyzing my investing performance in peer-to-peer lending notes. I aim to do two things:  

  1. Analyze my portfolio performance, and where possible place my performance in context of the broader peer-to-peer market where I invest.  

  2. Discuss various investment strategies I've had over the years and refine my future strategy.  

This series will not be a critique of any peer-to-peer platforms or services. The series is an exploration of my historical use of these financial instruments; did I utilize these instruments well, and if a suitable strategy can be found for future investing.

I don't have a set plan of attack for this analysis. I will start with broad exploratory analysis, and drill down if and when I find something interesting. 

> I write to find out what I am thinking...   
>  
> <cite>Joan Didion </cite> 


I am starting with broad strokes as that increases the likelihood of having some shared perspectives with you, and then as I layer on my assumptions and goals, you will have a map to see if anything is applicable to you. If we start on common ground and I explain the path I am taking, you can see where your path might diverge. Hopefully this approach increases the chances you will find something useful or interesting in this endeavor.


First I will explain how I got into the retail peer-to-peer lending market in the first place. 


### Why Peer-to-Peer Lending, Part 1 - Search for Yield  

In general, I tend towards cash-flow generating investment strategies; as such, I frequently search for high yield investments.  I was not old enough to invest in 1980, when you could buy [10% 10-year Treasury](https://www.multpl.com/10-year-treasury-rate/table/by-year){: target="_blank"}  However, I was old enough in the early oughts to jump on the Internet Banking savings rate, my first foray was with ING Savings, which with promotions, etc had [interest rates from 5%  to 7% ](https://forums.whirlpool.net.au/archive/2039928)  


In today's low-yield environment, it seems like anything higher than 3%  requires significant additional risk over an FDIC insured savings account. 

The first search question was: What Fixed-Income / Bond like products exists that might produce a high-yield ? 

How much effort will it take to find a strategy to produce a yield better than a bond fund ETF, say [BND](https://finance.yahoo.com/quote/BND?p=BND&.tsrc=fin-srch){: target="_blank"}, which as a current yield of 2.67%.  

One place I looked was the retail lending marketplace. Which is how I started investing at [LendingClub](https://www.lendingclub.com){:target="_blank"}.


### Why Peer-To-Peer Lending, Part 2 - Affinity for the model  


I was intrigued by the Peer-to-Peer lending company [LendingClub](https://www.lendingclub.com){:target="_blank"}. I was an early adopter, setting my investor account in October of 2012. This post is neither sponsored nor an advertisement for LendingClub, it is only an analysis of the performance of my portfolio.

Putting some money in LendingClub however, was largely inspired by the mission of peer-to-peer lending - I was also a relatively early participant of [Kiva](https://www.kiva.org){:target="_blank"} with giving money to fund my [first loan in November 2006](https://www.kiva.org/lend/1147){:target="_blank"}. Having learned of peer-to-peer platform in the US, I was eager to support it, and hoped it would be successful.

In a nutshell, I was not hunting for pure returns when I started out, I was happy to vote with my dollars to encourage democratization of the financial services industry. However, in addition to feeling some moral satisfaction at helping upstarts, I did want want a reasonable return, since Lending Club is not in fact a charity. Kiva satisfies my charitable peer-to-peer desires.


### A nagging feeling  

I have always had a nagging feeling that LendingClub was underperforming for me; at least underperforming relative to my expectations and based on the published interest rates on LendingClub website.  

My account's combined, adjusted [NAR](https://www.lendingclub.com/public/about-nar-trader.action#what-are-nar){: target="_blank"} has been fluctuating between 1.95% and 2.25% for the duration of my Lending Club investing. While my portfolio has a positive return, not losing money is good thing, and that anything higher than 2% beats most savings accounts these days, my expectations were higher.


I have changed LendingClub investment strategies over the years.  In the early years, only traded notes from the secondary market, then automated invested with a suggested portfolio, then automated investing with my own blend, and now back to only traded notes, but with a specific strategy.

I have done two things in response to having lower than expected returns; the first, I revised my investing strategy in recent months, and the second, is this series of post taking a closer look at my investing performance. 


The early sign for the revised strategy are positive as in recent weeks my combined, adjusted NAR has been creeping up towards 2.5%. I plan to explore strategy performance in future posts.



**Note:** In the early years, automated investing was not allowed in my state. As a result from 2012 to 2015 I purchased notes on the secondary market without a specific strategy. I also had varying degrees of discipline to diversification, so my impatience might have led to larger investments in individual notes than was prudent.
{: .notice--info}  


## Analysis  

The first research question:  Is my nagging feeling justified ?

The approach for this analysis will be from broad strokes and refine based on what is discovered.


### Loan Vintage Mixture 

{% include figure image_path="/assets/images/lc/my_portfolio_ovintage_histogram.png" alt="portfolio pie chart" caption="My Portfolio by O-Vintage (aka order date year)." %}

~~When automated investing became available my volume of notes purchased increased dramatically.~~

{% include figure image_path="/assets/images/lc/my_portfolio_ivintage_histogram.png" alt="portfolio pie chart" caption="My Portfolio by I-Vintage (aka issue date year)." %}



### Loan Status Mixture

- [ ] Compare count of loans in each loan status:  my portfolio to a large sample of the Lending Club historical data  

{% include figure image_path="/assets/images/lc/my_portfolio_by_status_pie_count.png" alt="portfolio pie chart" caption="My Portfolio by Loan Status (count)." %}



{% include figure image_path="/assets/images/lc/lc_all_notes_by_status_pie_count.png" alt="portfolio pie chart" caption="Lending Club 2012-2016 Notes by Loan Status (count)." %}




- [ ] Compare value of loans if each loan status:  my portfolio vs Lending Club historical data 

### Charge-Offs 

- [ ] Compare total Charge percent of loans:  my portfolio vs LC Historical data  

- [ ] Compare charge off value:  my portfolio vs LC Historical Data 






This post is an exploration my own personal portfolio performance.


My initial thought was my portfolio performance was being dragged by a large number charge-offs.


My portfolio is just a sampling of the total market, which for 2019 was over 4 million loans issued ([as published on the LC stats page](https://www.lendingclub.com/info/statistics.action){:target="_blank"}).


My portfolio is roughly 1,300 loans.  There are a lot of ways to draw 1,300 loans from a pool of millions.



Given the size of LendingClub


- [ ] add pie or donut chart by status (of completed notes)
- [ ] add graph of failures by (by quarter of completed notes)
- [ ] add last payment by (by quarter)


- [ ] add percentage of term at time of order to vintages  

- [ ] add link to code
