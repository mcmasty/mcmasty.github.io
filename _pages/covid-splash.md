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
last_modified_at:  2020-05-03 11:35:00 -0400
---


{% include plotly.html %}

{% include feature_row id="intro" type="center" %}



<p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Updated:" }}</strong> <time datetime="{{ page.last_modified_at | date: "%Y-%m-%d" }}">{{ page.last_modified_at | date: "%B %-d, %Y  %r  %Z %z" }}</time></p>

**Data as of:  2-May-2020[^1]**  

## tl;dr[^11] summary

**Just the Data:**  
United States for 02-May-2020[^1]:  

- 30,038 new positive tests, out of 264,537 total tests for a test positivity of 11.4%.  

- Total fatalities: 60,710 and daily fatalities: 1,651, leading to case fatality rate of: 5.4%.


<br>  

<!-- horizontal amber <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> -->
<!--  red up <i class="fas fa-arrow-up" style="color: red;"> </i>-->
<!--  green down <i class="fas fa-arrow-down" style="color: green;"></i> -->

**My take**  
It seems the path forward will be a roller coaster of progress and regression (the growth factor moving average demonstrates this.)  However, the _big_ trends are positive (April was better than March), but the _small_ trends are  volatile (a single day may be better or worse than the day before).    


- <i class="fas fa-arrow-down" style="color: green;"> </i> March average daily growth rate: 29%;   April average daily growth rate 5.9%.  

- <i class="fas fa-arrow-up" style="color: green;"> </i> March average doubling days of 2.6 days;  April average doubling days of 15 days.  


- <i class="fas fa-arrow-down" style="color: green;"> </i> New fatalities below 1,700; 3 consecutive days of decreasing fatalities.     

- <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> New Cases have stopped their recent growth spurt.       

- <i class="fas fa-arrow-up" style="color: green;"> </i> Two consecutive days surpassing 250,000 tests.    



<br>
<!--http://localhost:5000/covid-page/#coronavirus-tracking-sites-and-data-sources -->

FYI:  [My list of Coronavirus Tracking sites and data sources.](#coronavirus-tracking-sites-and-data-sources)



## Impact in Lives Lost  

In terms of fatality, the number of lives lost is remains high (near 2,000), but hopefully we're about to start a new trend of decreasing numbers.  

![New Death Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/new_death_20200503_1588531211.png){: .align-center}


<!-- {% include state_death_treemap.html %}{: align="center"} -->


![New Death Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/state_new_death_proportion_20200503_1588532636.png){: .align-center}




To put this daily death total in perspective, according to the CDC mortality data[^5], there were 2,813,503 deaths in 2017.  

**The leading causes:**   

|  Cause | Total Deaths |  
| :---: | ---: |  
| Heart Disease | 647,457 |  
| Cancer | 599,108 |  
| Accidents | 169,936 |  



Influenza & Pneumonia is the 8th highest leading cause of death with 55,672 deaths in 2017.  
{: .notice--info}  


Given we are still in the early days of the outbreak, the rate of change is more telling then the cumulative totals.  To compare mortality, compute the average deaths per day for each leading cause and compare to the daily death count for COVID-19.

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/leading_causes_20200503_1588531260.png){: .align-center}

## Spread / Containment      


The data shows physical distancing is working. The macro trend is that the daily growth rate is decreasing, and subsequently the number of days until the case count doubles is also improving, i.e. increasing.  

The daily growth rate is now stabilizing around  3%, with the 3-day moving average currently at 2.9%.  


![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_update_20200503_1588531287.png){: .align-center}    


<br/>  

### Growth Factor    

Growth factor is a measure of how quickly the infection is growing.  

A growth factor < 1 (green area on chart), means there are fewer cases today then yesterday, and If we can keep that up long-enough, the outbreak will die down.

In a perfect world the growth factor would approach 0, meaning no new cases.


_Growth Factor_[^4] is a ratio of new cases today compared to new cases yesterday.


![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/growth_factor_20200503_1588531305.png){: .align-center}


To get a better feel for growth factor, below is a basic logistic curve with different growth factor reference values plotted. Even though exponential growth ceases at growth factor = 1, the curve is still steep. In my opinion, the growth in total COVID-19 cases won't feel like it slowing until the growth factor is below 0.90.  




![Logistic Curve Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/logistic_curve_20200410_1586548277.png){: .align-center}  

> All models are wrong, but some are useful.  
> <cite>George Box</cite>  

See notes[^9] [^10] for more details on logistic curve and growth factor.


## Testing Snapshot

As of this writing, the US is nearing  7 million total tests.  

![High Level Testing]({{ site.url }}{{ site.baseurl }}/assets/images/covid/high_level_testing_20200503_1588531329.png){: .align-center}

Consecutive days of surpassing 250,000 tests.  
<!-- It appears testing throughput has increased to approach the 200k test per day, up from the 150k per day plateau of the last few weeks.  -->



Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days. This thought experiment is only to suggest the scale of testing that might be necessary for effective public health management as part of a strategy to relax physical distancing restrictions.  
{: .notice--info}




**How much testing is enough?**   
One measure might be the proportion of positive tests as a share of total testing. We know that asymptomatic contagious individuals are making this outbreak particularly challenging to deal with. Any attempt to identify the asymptomatic carriers of the disease will require testing many healthy people, who are also asymptomatic. The impact of testing more asymptomatic people, would drive down the number of positive tests as more healthy people are tested.   

The below graph shows the number of positive tests as a proportion of total testing.  
![Positive Test Proportion]({{ site.url }}{{ site.baseurl }}/assets/images/covid/positive_test_proportion_20200503_1588531349.png){: .align-center}  






**Comparison to other Countries[^7]:**   

| Country | Pop. | Test Positivity | Case Fatality Rate | Test Per 1k Pop
| :--- |  ---: | ---: | ---: |  ---: |
| Taiwan     |     23.8 M |     0.7% |     1.4% |        3 |  
| S. Korea   |     51.3 M |     1.7% |     2.3% |       12 |  
| Russia     |    145.9 M |     3.1% |     1.0% |       24 |  
| Iceland    |      0.3 M |     3.7% |     0.6% |      142 |  
| India      |  1,379.1 M |     4.2% |     3.3% |        1 |  
| Germany    |     83.8 M |     6.4% |     4.0% |       30 |  
| Canada     |     37.7 M |     6.7% |     5.9% |       21 |  
| Italy      |     60.5 M |    10.4% |    13.6% |       33 |  
| Sweden     |     10.1 M |    17.7% |    12.3% |       12 |  
| UK         |     67.9 M |    20.9% |    15.6% |       12 |  


Test positivity is measured with aggregate test data unless noted otherwise.

{% capture testing-example %}
Thought experiment on test-positivity: If we use 5% as a threshold for relaxing physical distancing, there are two levers we can pull to reach it; (1) decrease the number of new positive tests ( aka continue with physical distancing measures), (2) increase the number tests completed each day.

Assuming no increase in testing capacity, our current capacity is around 150,000 test per day, 5% of that number is 7,500.  To reach 5% positive test proportion, we'd need to keep physical distancing guidelines in place until the number of new cases falls to 7,500 per day.  

Alternatively, given the 30,000 new case on 15-April, we'd need 600,000 total tests, with all additional tests negative, for the proportion of positives to be 5%.  

Ideally we will make progress on both strategies.  
{% endcapture %}  

<div class="notice--info"> {{ testing-example | markdownify }} </div>



### State Level Snapshot

Field definitions:  

- `State` State code, followed by that state's contribution to the total number of new cases as a percent.
- `Pop.` is state population in millions  
- `Cases` is the total number of cases measured by positive test results  
- `New.C` New Cases. Lower is better.
- `DGR` Daily Growth Rate. This is 4-day, exponential moving average. Lower is better.
- `Tests per 1k` is number of tests per 1,000 in state's population. Higher is better.   
- `T-Pos.` is the test-positivity percentage; ratio of positive tests to total tests.  Lower is better.     
- `Fat.`  Total number of fatalities
- `Fat./1M`  number of deaths per 1 million in population  
- `GF-m.a.` Growth Factor, 4-day span, exponentially weighted moving average. Todays value has more weight, than the measure of 4 days ago.  Lower is better.    
- `GF-7day`   Summation of GF-m.a. from last 7 days. The lower the better. Values below 7 indicate exponential has stopped.  
- `GF-14day`   Summation of GF-m.a. from last 14 days. The lower the better. Values below 14 indicate exponential has stopped.   
- `Dbl.Days`  Given the current daily growth rate, how many days until cases double.  Higher is better.    
- `As-Of Date`  the date when the data was last modified

- `SparkLines`  The embedded graphs in the table are a plot of the last 14-days of the metric in question. For example, in the `Cases` column, the sparkline shows visually how the total number of cases has changed over the last 14 days.

{%  include state_table.md  %}


<br>

**State's share of new cases today**  

![New Case Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/state_new_case_proportion_20200503_1588532531.png){: .align-center}





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

  ![Recoveries]({{ site.url }}{{ site.baseurl }}/assets/images/covid/recoveries_20200503_1588531397.png){: .align-center}


<br/>

Hopefully coming soon, a number of vaccines and treatments.   [Summary of Vaccine and Treatments](https://www.visualcapitalist.com/every-vaccine-treatment-covid-19-so-far/?from=timeline&isappinstalled=0){: target="_blank"}

[Summary of Treatment Research by WHO](https://www.who.int/blueprint/priority-diseases/key-action/novel-coronavirus/en/){: target="_blank"}  


This is not an exhaustive list; anything missing is accidental.  

***   

## Coronavirus Tracking sites and Data Sources  
- [Johns Hopkins Tracker](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6){: target="_blank"}  -- Dashboard tracking the global outbreak  

- [worldometer](https://www.worldometers.info/coronavirus/){: target="_blank"}   -- High Level coronavirus stats for all the countries in the world      

- [The Covid Tracking Project](https://covidtracking.com){: target="_blank"} -- The most complete testing dataset I've found, aggregating information from  state public health authorities    

- [The New York Times Data Files](https://github.com/nytimes/covid-19-data){: target="_blank"}  -- NYT compiles data at the state and county level from state and local governments      

- [The New York Times Growth Tracker](https://www.nytimes.com/interactive/2020/04/03/upshot/coronavirus-metro-area-tracker.html){: target="_blank"}  -- Different data visualization tools to examine how fast coronavirus is spreading   


- [University of Washington Institute for Health Metrics and Evaluation](https://covid19.healthdata.org/projections){: target="_blank"}   -- Projections on when peak new cases and peak new deaths will happen along with impact to projected hospital resources   

- [1point3acres](https://coronavirus.1point3acres.com/en){: target="_blank"}  -- The core data is similar to other sites, but the visualizations are slightly different, and they are starting to track things like PPE requests and jobs (hiring and layoffs)     

## Citations and Notes  

[^1]:  <cite>Data for these charts sourced from [The Covid Tracking Project](https://covidtracking.com)</cite>

[^2]:  <cite>Healthcare employment data from [Kaiser Family Foundation](https://www.kff.org/other/state-indicator/total-health-care-employment/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D){: target="_blank"} </cite>  

[^3]:  <cite>Worldometer Incubation [data page](https://www.worldometers.info/coronavirus/coronavirus-incubation-period/){: target="_blank"}</cite>

[^4]: <cite>[3 Brown 1 Blue](https://youtu.be/Kas0tIxDvrg){: target="_blank"} for inspiration on calculating growth factor</cite>  

[^5]:  <cite>[CDC Mortality Data](https://www.cdc.gov/nchs/fastats/deaths.htm){: target="_blank"}</cite>  

[^6]:  <cite> Dr. Tatiana Prowell, a guest on [Radiolab](https://www.wnycstudios.org/podcasts/radiolab){: target="_blank"}, [Dispatch 3: Shared Immunity episode](https://www.wnycstudios.org/podcasts/radiolab/articles/dispatch-3-shared-immunity){: target="_blank"}</cite>

[^7]: <cite>Country Level testing summary from [Wordodmeter Country Page](https://www.worldometers.info/coronavirus/){: target="_blank"}

[^8]: <cite>Mortality following infection, [The Lancet](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30195-X/fulltext){: target="_blank"}  

[^9]: The logistic curve above is not a measurement, it is a model, and therefore it is an approximation. The goal is to provide some context of where we might be on the curve, based on the actual measurement and calculation of growth factor.   

[^10]: The distance between time points on the plot is not fixed. The distance between t0 and t1, might be 30 days, while the distance between t6 and t7 might be 3 days. One complicating factor of epidemics is the feedback loop. We can influence what shape the outbreak takes. The total number of COVID-19 cases depends on us, and what we do.  How quickly we flatten the curve depends on us, and what we do. Therefore, the duration between t5 and t6 is not a fixed number of days, but instead, depends on us, and what we do.   

[^11]: <cite>The tl;dr label is often used to point out excessive verbosity or to signify the presence of and location of a short summary in case the reader doesn't want to take the time to read the entire detail. [Wikipedia Entry](https://en.wikipedia.org/wiki/Wikipedia:Too_long;_didn%27t_read){: target="_blank"}  </cite>
