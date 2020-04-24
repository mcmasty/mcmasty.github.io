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
last_modified_at:  2020-04-24 11:25:00 -0400
---


{% include feature_row id="intro" type="center" %}


<p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Updated:" }}</strong> <time datetime="{{ page.last_modified_at | date: "%Y-%m-%d" }}">{{ page.last_modified_at | date: "%B %-d, %Y  %r  %Z %z" }}</time></p>


### tl;dr[^11] summary

<!-- <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> -->


- <i class="fas fa-arrow-down" style="color: green;"></i> New deaths saw a second consecutive day of reductions.  

- <i class="fas fa-arrow-up" style="color: red;"></i> The number of new cases rose yesterday, as a result the growth factor has also increased

- <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"> </i> The huge jump in testing was not sustained, however, testing appears to be increasing from the plateau.  

- **New Data**  State level test positivity data available near the bottom of this page.  




### Coronavirus Tracking sites and Data Sources  
- [Johns Hopkins Tracker](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6){: target="_blank"}  -- Dashboard tracking the global outbreak  

- [worldometer](https://www.worldometers.info/coronavirus/){: target="_blank"}   -- High Level coronavirus stats for all the countries in the world      

- [The Covid Tracking Project](https://covidtracking.com){: target="_blank"} -- The most complete testing dataset I've found, aggregating information from  state public health authorities    

- [The New York Times Data Files](https://github.com/nytimes/covid-19-data){: target="_blank"}  -- NYT compiles data at the state and county level from state and local governments      

- [The New York Times Growth Tracker](https://www.nytimes.com/interactive/2020/04/03/upshot/coronavirus-metro-area-tracker.html){: target="_blank"}  -- Different data visualization tools to examine how fast coronavirus is spreading   


- [University of Washington Institute for Health Metrics and Evaluation](https://covid19.healthdata.org/projections){: target="_blank"}   -- Projections on when peak new cases and peak new deaths will happen along with impact to projected hospital resources   

- [1point3acres](https://coronavirus.1point3acres.com/en){: target="_blank"}  -- The core data is similar to other sites, but the visualizations are slightly different, and they are starting to track things like PPE requests and jobs (hiring and layoffs)     

## Impact in Lives Lost  

In terms of fatality, the number of lives lost is remains high (near 2,000), but hopefully we're about to start a new trend of decreasing numbers.  

![New Death Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/new_death_20200424_1587754919.png){: .align-center}

The Lancet[^8] has reported that the time between symptom onset and death can range between 2 and 8 weeks. Combining The Lancet report with the observed spike of new case spikes on 10th and 11th of April (chart below), we might anticipate the death rate to stay relatively high for a few more weeks.   
{: .notice--info}      


To put this daily death total in perspective, according to the CDC mortality data[^5], there were 2,813,503 deaths in 2017.  

**The leading causes:**   

|  Cause | Total Deaths |  
| :---: | ---: |  
| Heart Disease | 647,457 |  
| Cancer | 599,108 |  
| Accidents | 169,936 |  



Influenza & Pneumonia is the 8th highest leading cause of death with 55,672 deaths in 2017. As of this writing, the total number of reported COVID-19 deaths in the US is approaching 46,000.
{: .notice--info}  


Given we are still in the early days of the outbreak, the rate of change is more telling then the cumulative totals.  To compare mortality, compute the average deaths per day for each leading cause and compare to the daily death count for COVID-19.

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/leading_causes_20200424_1587754882.png){: .align-center}

## Spread / Containment      

**Data as of:  23-April-2020[^1]**  

The data shows physical distancing is working. The macro trend is that the daily growth rate is decreasing, and subsequently the number of days until the case count doubles is also improving, i.e. increasing.  

The daily growth rate has stabilized under 4%, with the 3-day moving average currently at 3.7%.  


![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_update_20200424_1587754966.png){: .align-center}    


<br/>  

### Growth Factor    

Growth factor is a measure of how quickly the infection is growing.  

A growth factor < 1 (green area on chart), means there are fewer cases today then yesterday, and If we can keep that up long-enough, the outbreak will die down.

In a perfect world the growth factor would approach 0, meaning no new cases.


_Growth Factor_[^4] is a ratio of new cases today compared to new cases yesterday.


![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/growth_factor_20200424_1587755033.png){: .align-center}


To get a better feel for growth factor, below is a basic logistic curve with different growth factor reference values plotted. Even though exponential growth ceases at growth factor = 1, the curve is still steep. In my opinion, the growth in total COVID-19 cases won't feel like it slowing until the growth factor is below 0.90.  




![Logistic Curve Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/logistic_curve_20200410_1586548277.png){: .align-center}  

> All models are wrong, but some are useful.  
> <cite>George Box</cite>  

See notes[^9] [^10] for more details on logistic curve and growth factor.


## Testing Snapshot

The US has surpassed 4 million total tests.  

![High Level Testing]({{ site.url }}{{ site.baseurl }}/assets/images/covid/high_level_testing_20200424_1587755091.png){: .align-center}

California's jump in testing has not continued. On the bright side, it appears testing throughput has increased to approach the 200k test per day, up from the 150k per day plateau of the last few weeks.  



Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days. This thought experiment is only to suggest the scale of testing that might be necessary for effective public health management as part of a strategy to relax physical distancing restrictions.  
{: .notice--info}




**How much testing is enough?**   
One measure might be the proportion of positive tests as a share of total testing. We know that asymptomatic contagious individuals are making this outbreak particularly challenging to deal with. Any attempt to identify the asymptomatic carriers of the disease will require testing many healthy people, who are also asymptomatic. The impact of testing more asymptomatic people, would drive down the number of positive tests as more healthy people are tested.   

The below graph shows the number of positive tests as a proportion of total testing.  
![Positive Test Proportion]({{ site.url }}{{ site.baseurl }}/assets/images/covid/positive_test_proportion_20200424_1587755140.png){: .align-center}  

United States for 22-April-2020[^1]: test positivity: 8.7%, case fatality rate: 5.1%    


**Comparison to other Countries[^7]:**   

| Country | Test Positivity | Case Fatality Rate |
| :--- | :---: | :---: |
| Taiwan     |     0.7% |     1.4% |  
| S. Korea   |     1.9% |     2.2% |  
| Iceland    |     4.0% |     0.6% |  
| Canada     |     6.8% |     4.8% |  
| Germany    |     8.6% |     3.4% |  
| Italy      |    12.7% |    13.4% |  
| UK         |    23.8% |    13.6% |    


Test positivity is measured with aggregate test data unless noted otherwise.

{% capture testing-example %}
Thought experiment on test-positivity: If we use 5% as a threshold for relaxing physical distancing, there are two levers we can pull to reach it; (1) decrease the number of new positive tests ( aka continue with physical distancing measures), (2) increase the number tests completed each day.

Assuming no increase in testing capacity, our current capacity is around 150,000 test per day, 5% of that number is 7,500.  To reach 5% positive test proportion, we'd need to keep physical distancing guidelines in place until the number of new cases falls to 7,500 per day.  

Alternatively, given the 30,000 new case on 15-April, we'd need 600,000 total tests, with all additional tests negative, for the proportion of positives to be 5%.  

Ideally we will make progress on both strategies.  
{% endcapture %}  

<div class="notice--info"> {{ testing-example | markdownify }} </div>



### State Level Snapshot

Some field definitions:  

- `Pop.` is state population in millions  
- `Tot.Case` is the total number of cases measured by positive test results  
- `Tests per 1k` is number of tests per 1,000 in state's population  
- `T-Positivity` is the test-positivity percentage; ratio of positive tests to total tests    
- `Fatality per 1M`  number of deaths per 1 million in population  
- `As-Of Date`  the date when the data was last modified



| State|    Pop.| Tot.Case | Tests per 1k | T-Positivity | Fatalities | Fatality per 1M | As-Of Date |  
| :---:  | ---:   |  ---:    |   :---:  |:---:  |   ---:   |  :---: |  :---: |
| AK  | 0.7 M   | 337  | 17  | 2.8%  | 9  | 12    | 23-Apr |
| AL  | 4.9 M   | 5,832  | 11  | 11.1%  | 197  | 40    | 23-Apr |
| AR  | 3.0 M   | 2,599  | 11  | 7.5%  | 45  | 15    | 24-Apr |
| AZ  | 7.3 M   | 5,769  | 8  | 9.8%  | 249  | 34    | 23-Apr |
| CA  | 39.5 M   | 37,369  | 12  | 7.8%  | 1,469  | 37    | 22-Apr |
| CO  | 5.8 M   | 11,262  | 9  | 21.5%  | 552  | 96    | 23-Apr |
| CT  | 3.6 M   | 23,100  | 20  | 32.3%  | 1,639  | 460    | 23-Apr |
| DC  | 0.7 M   | 3,361  | 23  | 21.1%  | 139  | 197    | 22-Apr |
| DE  | 1.0 M   | 3,308  | 17  | 19.6%  | 92  | 94    | 22-Apr |
| FL  | 21.5 M   | 29,648  | 14  | 9.8%  | 1,006  | 47    | 23-Apr |
| GA  | 10.6 M   | 21,883  | 10  | 21.6%  | 881  | 83    | 23-Apr |
| HI  | 1.4 M   | 591  | 19  | 2.2%  | 12  | 8    | 22-Apr |
| IA  | 3.2 M   | 3,924  | 9  | 13.4%  | 96  | 30    | 22-Apr |
| ID  | 1.8 M   | 1,836  | 11  | 9.6%  | 54  | 30    | 23-Apr |
| IL  | 12.7 M   | 36,934  | 14  | 21.3%  | 1,688  | 133    | 23-Apr |
| IN  | 6.7 M   | 13,039  | 11  | 18.1%  | 706  | 105    | 23-Apr |
| KS  | 2.9 M   | 2,482  | 7  | 11.6%  | 112  | 38    | 23-Apr |
| KY  | 4.5 M   | 3,481  | 10  | 8.1%  | 191  | 43    | 23-Apr |
| LA  | 4.6 M   | 25,739  | 31  | 18.0%  | 1,540  | 331    | 23-Apr |
| MA  | 6.9 M   | 46,023  | 28  | 23.6%  | 2,360  | 340    | 22-Apr |
| MD  | 6.0 M   | 15,737  | 13  | 19.6%  | 748  | 124    | 23-Apr |
| ME  | 1.3 M   | 937  | 13  | 5.3%  | 44  | 33    | 23-Apr |
| MI  | 10.0 M   | 35,291  | 13  | 27.5%  | 2,977  | 298    | 23-Apr |
| MN  | 5.6 M   | 2,942  | 9  | 5.7%  | 200  | 35    | 22-Apr |
| MO  | 6.1 M   | 6,321  | 11  | 9.7%  | 218  | 36    | 23-Apr |
| MS  | 3.0 M   | 5,153  | 19  | 9.3%  | 201  | 68    | 22-Apr |
| MT  | 1.1 M   | 442  | 11  | 3.7%  | 14  | 13    | 23-Apr |
| NC  | 10.5 M   | 7,608  | 9  | 7.9%  | 253  | 24    | 23-Apr |
| ND  | 0.8 M   | 709  | 21  | 4.3%  | 15  | 20    | 23-Apr |
| NE  | 1.9 M   | 2,124  | 10  | 11.4%  | 47  | 24    | 23-Apr |
| NH  | 1.4 M   | 1,670  | 12  | 9.9%  | 51  | 38    | 23-Apr |
| NJ  | 8.9 M   | 99,989  | 23  | 50.0%  | 5,368  | 604    | 23-Apr |
| NM  | 2.1 M   | 2,210  | 20  | 5.4%  | 71  | 34    | 23-Apr |
| NV  | 3.1 M   | 4,208  | 11  | 12.1%  | 195  | 63    | 24-Apr |
| NY  | 19.5 M   | 263,460  | 36  | 37.9%  | 15,740  | 809    | 23-Apr |
| OH  | 11.7 M   | 14,142  | 9  | 13.8%  | 656  | 56    | 23-Apr |
| OK  | 4.0 M   | 3,017  | 12  | 6.6%  | 179  | 45    | 23-Apr |
| OR  | 4.2 M   | 2,127  | 10  | 4.8%  | 83  | 20    | 23-Apr |
| PA  | 12.8 M   | 36,647  | 14  | 20.5%  | 1,421  | 111    | 23-Apr |
| RI  | 1.1 M   | 6,256  | 42  | 14.1%  | 189  | 178    | 23-Apr |
| SC  | 5.1 M   | 4,917  | 9  | 11.1%  | 150  | 29    | 23-Apr |
| SD  | 0.9 M   | 1,956  | 16  | 13.9%  | 9  | 10    | 22-Apr |
| TN  | 6.8 M   | 8,266  | 18  | 6.7%  | 170  | 25    | 23-Apr |
| TX  | 29.0 M   | 21,944  | 8  | 9.7%  | 561  | 19    | 23-Apr |
| UT  | 3.2 M   | 3,612  | 25  | 4.5%  | 35  | 11    | 23-Apr |
| VA  | 8.5 M   | 10,627  | 8  | 16.5%  | 372  | 44    | 23-Apr |
| VT  | 0.6 M   | 825  | 22  | 6.0%  | 43  | 69    | 23-Apr |
| WA  | 7.6 M   | 12,753  | 20  | 8.3%  | 711  | 93    | 23-Apr |
| WI  | 5.8 M   | 5,052  | 10  | 8.9%  | 257  | 44    | 23-Apr |
| WV  | 1.8 M   | 981  | 16  | 3.4%  | 31  | 17    | 23-Apr |
| WY  | 0.6 M   | 332  | 14  | 4.2%  | 7  | 12    | 23-Apr |




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

  ![Recoveries]({{ site.url }}{{ site.baseurl }}/assets/images/covid/recoveries_20200423_1587678331.png){: .align-center}


<br/>

Hopefully coming soon, a number of vaccines and treatments.   [Summary of Vaccine and Treatments](https://www.visualcapitalist.com/every-vaccine-treatment-covid-19-so-far/?from=timeline&isappinstalled=0){: target="_blank"}

[Summary of Treatment Research by WHO](https://www.who.int/blueprint/priority-diseases/key-action/novel-coronavirus/en/){: target="_blank"}  


This is not an exhaustive list; anything missing is accidental.  


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
