---
title: "My COVID-19 Page"
layout: splash
permalink: /covid-page/
date: 2020-04-06T18:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280/auto_image/compress/zZHxJaBNT1ab9jSlVeXl"
  caption: "Photo by [**CDC**](https://www.cdc.gov/) on [**Unsplash**](https://unsplash.com)"
  teaser: https://cdn.filestackcontent.com/resize=w:600,h:400,fit:crop/auto_image/compress/zZHxJaBNT1ab9jSlVeXl  
excerpt: "The current data available piqued my curiosity, so I started crunching the data myself."
intro:
  - excerpt: "There are a number of excellent coronavirus tracking websites (see list below) and many of them are making their data sources available. I found myself jumping between pages and sites, doing a few calculations I was interested in, and then emailing my analysis to friends and family. After a few weeks of this, I finally decided to move some of that analysis to the web."      

categories:
  - Post
tags:
  - COVID-19
last_modified_at:  2020-04-21 11:35:00 -0400
---


{% include feature_row id="intro" type="center" %}


<p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Updated:" }}</strong> <time datetime="{{ page.last_modified_at | date: "%Y-%m-%d" }}">{{ page.last_modified_at | date: "%B %-d, %Y  %r  %Z %z" }}</time></p>


### tl;dr summary

- 5th consecutive day of decreasing new deaths (longest such run)
- 3rd consecutive day of decreasing new cases (tied for longest such run)  
- Lowest level of new cases since March 30th
- Daily growth rate is lowest measured value (3.1%); Days until cases double is highest measured value (22.2 days)



### Coronavirus Tracking sites and Data Sources  
- [Johns Hopkins Tracker](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6){: target="_blank"}  -- Dashboard tracking the global outbreak  

- [worldometer](https://www.worldometers.info/coronavirus/){: target="_blank"}   -- High Level coronavirus stats for all the countries in the world      

- [The Covid Tracking Project](https://covidtracking.com){: target="_blank"} -- The most complete testing dataset I've found, aggregating information from  state public health authorities    

- [The New York Times Data Files](https://github.com/nytimes/covid-19-data){: target="_blank"}  -- NYT compiles data at the state and county level from state and local governments      

- [The New York Times Growth Tracker](https://www.nytimes.com/interactive/2020/04/03/upshot/coronavirus-metro-area-tracker.html){: target="_blank"}  -- Different data visualization tools to examine how fast coronavirus is spreading   


- [University of Washington Institute for Health Metrics and Evaluation](https://covid19.healthdata.org/projections){: target="_blank"}   -- Projections on when peak new cases and peak new deaths will happen along with impact to projected hospital resources   

- [1point3acres](https://coronavirus.1point3acres.com/en){: target="_blank"}  -- The core data is similar to other sites, but the visualizations are slightly different, and they are starting to track things like PPE requests and jobs (hiring and layoffs)     

## Impact in Lives Lost  

In terms of fatality, the number of lives lost is moving in the right direction. Yesterday was the 5th consecutive day of a decreasing death total; the longest stretch we've had in this outbreak.  

![New Death Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/new_death_20200421_1587496139.png){: .align-center}

The Lancet[^8] has reported that the time between symptom onset and death can range between 2 and 8 weeks. Combining The Lancet report with the observed spike of new case spikes on 10th and 11th of April (chart below), we might anticipate the death rate to stay relatively high for a few more weeks.   
{: .notice--info}      


To put this daily death total in perspective, according to the CDC mortality data[^5], there were 2,813,503 deaths in 2017.  

**The leading causes:**   

|  Cause | Total Deaths |  
| :---: | ---: |  
| Heart Disease | 647,457 |  
| Cancer | 599,108 |  
| Accidents | 169,936 |  



Influenza & Pneumonia is the 8th highest leading cause of death with 55,672 deaths in 2017. As of this writing, the total number of reported COVID-19 deaths in the US is approaching 15,000.
{: .notice--info}  


Given we are still in the early days of the outbreak, the rate of change is more telling then the cumulative totals.  To compare mortality, compute the average deaths per day for each leading cause and compare to the daily death count for COVID-19.

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/leading_causes_20200421_1587496074.png){: .align-center}

## Spread / Containment      

**Data as of:  20-April-2020[^1]**  

The data shows physical distancing is working. The macro trend is that the daily growth rate is decreasing, and subsequently the number of days until the case count doubles is also improving, i.e. increasing.  

The daily growth rate continues to improve and is now under 4%, with the 3-day moving average of 3.8%.  


![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_update_20200421_1587496198.png){: .align-center}    


<br/>  

### Growth Factor    
More to come here, but for folks who received my emails, I discussed _Growth Factor_[^4] as a ratio of new cases today compared to new cases yesterday. As long as growth factor > 1, exponential growth will continue. A Growth Factor = 1, is the inflection point; that is, the point when new case growth changes from exponential to logarithmic. Stopping exponential growth is a critical first step to managing the pandemic.  

![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/growth_factor_20200421_1587496226.png){: .align-center}


To get a better feel for growth factor, below is a basic logistic curve with different growth factor reference values plotted. Even though exponential growth ceases at growth factor = 1, the curve is still steep. In my opinion, the growth in total COVID-19 cases won't feel like it slowing until the growth factor is below 0.90.  


![Logistic Curve Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/logistic_curve_20200410_1586548277.png){: .align-center}  

> All models are wrong, but some are useful.  
> <cite>George Box</cite>  


A few notes:  
- The logistic curve above is not a measurement, it is a model, and therefore it is an approximation. The goal is to provide some context of where we might be on the curve, based on the actual measurement and calculation of growth factor.   

- The distance between time points on the plot is not fixed. The distance between t0 and t1, might be 30 days, while the distance between t6 and t7 might be 3 days. One complicating factor of epidemics is the feedback loop. We can influence what shape the outbreak takes. The total number of COVID-19 cases depends on us, and what we do.  How quickly we flatten the curve depends on us, and what we do. Therefore, the duration between t5 and t6 is not a fixed number of days, but instead, depends on us, and what we do.   

## Testing Snapshot

The US has surpassed 4 million total tests.  

![High Level Testing]({{ site.url }}{{ site.baseurl }}/assets/images/covid/high_level_testing_20200421_1587496301.png){: .align-center}

Testing throughput continues to improve, but in my opinion is not yet sufficient to effectively manage the relaxation of physical distancing guidelines. (It looks like data on April 4th is bad data.)    

Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days. This thought experiment is only to suggest the scale of testing that might be necessary for effective public health management as part of a strategy to relax physical distancing restrictions.  
{: .notice--info}




**How much testing is enough?**   
One measure might be the proportion of positive tests as a share of total testing. We know that asymptomatic contagious individuals are making this outbreak particularly challenging to deal with. Any attempt to identify the asymptomatic carriers of the disease will require testing many healthy people, who are also asymptomatic. The impact of testing more asymptomatic people, would drive down the number of positive tests as more healthy people are tested.   

The below graph shows the number of positive tests as a proportion of total testing.  
![Positive Test Proportion]({{ site.url }}{{ site.baseurl }}/assets/images/covid/positive_test_proportion_20200421_1587496328.png){: .align-center}  


**Reference Countries[^7]:**   

|  Country | Proportion of Positive Tests |  
| :---: | :---: |  
| Taiwan | 0.8% |  
| South Korea | 1.9% |  
| Iceland | 4.1% |  
| Canada | 6.4% |
| Germany | 7.7% |  
| Italy | 13.0% |  
| United States (daily)| 16.7% |    

Test positivity is measured with aggregate test data unless noted otherwise.


If we use 5% as a threshold for relaxing physical distancing, there are two levers we can pull to reach it; (1) decrease the number of new positive tests ( aka continue with physical distancing measures), (2) increase the number tests completed each day.

Assuming no increase in testing capacity, our current capacity is around 150,000 test per day, 5% of that number is 7,500.  To reach 5% positive test proportion, we'd need to keep physical distancing guidelines in place until the number of new cases falls to 7,500 per day.  

Alternatively, given the 30,000 new case on 15-April, we'd need 600,000 total tests, with all additional tests negative, for the proportion of positives to be 5%.  

Ideally we will make progress on strategies.  



## Fighting COVID-19  

The best tools we have today

- (Prevention) Frequent hand washing

- (Prevention) Physical distancing

- (Treatment) Blood plasma transfusion from people who have recovered and have COVID-19 antibodies

  [Johns Hopkins convalescent serum therapy](https://hub.jhu.edu/2020/04/08/arturo-casadevall-blood-sera-profile/){: target="_blank"}  

  [National COVID-19 Convalescent Plasma Project](https://ccpp19.org/index.html){: target="_blank"}

  [In use in NYC](https://www.nbcnews.com/health/health-news/plasma-treatment-being-tested-new-york-may-be-coronavirus-gamechanger-n1178436){: target="_blank"}

  [More info at the Red Cross for Recovered Patients](https://www.redcrossblood.org/donate-blood/dlp/plasma-donations-from-recovered-covid-19-patients.html){: target="_blank"}

  An increasing number of people recovered, means more people can help - a single person's blood plasma donation produces enough serum to treat 3 people.[^6]    

  ![Recoveries]({{ site.url }}{{ site.baseurl }}/assets/images/covid/recoveries_20200421_1587496257.png){: .align-center}


<br/>

Hopefully coming soon, a number of vaccines and treatments.   [Summary of Vaccine and Treatments](https://www.visualcapitalist.com/every-vaccine-treatment-covid-19-so-far/?from=timeline&isappinstalled=0){: target="_blank"}

[Summary of Treatment Research by WHO](https://www.who.int/blueprint/priority-diseases/key-action/novel-coronavirus/en/){: target="_blank"}  


This is not an exhaustive list; anything missing is accidental.  


## Citations

[^1]:  <cite>Data for these charts sourced from [The Covid Tracking Project](https://covidtracking.com)</cite>

[^2]:  <cite>Healthcare employment data from [Kaiser Family Foundation](https://www.kff.org/other/state-indicator/total-health-care-employment/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D){: target="_blank"} </cite>  

[^3]:  <cite>Worldometer Incubation [data page](https://www.worldometers.info/coronavirus/coronavirus-incubation-period/){: target="_blank"}</cite>

[^4]: <cite>[3 Brown 1 Blue](https://youtu.be/Kas0tIxDvrg){: target="_blank"} for inspiration on calculating growth factor</cite>  

[^5]:  <cite>[CDC Mortality Data](https://www.cdc.gov/nchs/fastats/deaths.htm){: target="_blank"}</cite>  

[^6]:  <cite> Dr. Tatiana Prowell, a guest on [Radiolab](https://www.wnycstudios.org/podcasts/radiolab){: target="_blank"}, [Dispatch 3: Shared Immunity episode](https://www.wnycstudios.org/podcasts/radiolab/articles/dispatch-3-shared-immunity){: target="_blank"}</cite>

[^7]: <cite>Country Level testing summary from [Wikipedia](https://en.wikipedia.org/wiki/COVID-19_testing){: target="_blank"}

[^8]: <cite>Mortality following infection, [The Lancet](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30195-X/fulltext){: target="_blank"}  
