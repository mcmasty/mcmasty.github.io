---
title: "My COVID-19 Page"
layout: splash
permalink: /covid-page/
date: 2020-04-06T18:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280/compress/zZHxJaBNT1ab9jSlVeXl"
  caption: "Photo by [**CDC**](https://www.cdc.gov/) on [**Unsplash**](https://unsplash.com)"
  teaser: https://cdn.filestackcontent.com/resize=w:600,h:400,fit:crop/compress/zZHxJaBNT1ab9jSlVeXl  
excerpt: "I wasn't really finding the numbers I was curious about so I started crunching the data myself."
intro:
  - excerpt: "There are a number of excellent coronavirus tracking websites (see list below) and many of them are making their data sources available. I found myself jumping between pages and sites, doing a few calculations I was interested in, and then emailing my analysis to friends and family. After a few weeks of this, I finally decided to move some of that analysis to the web."      

last_modified_at:  2020-04-08 12:48:00 -0400
---


{% include feature_row id="intro" type="center" %}


<p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Updated:" }}</strong> <time datetime="{{ page.last_modified_at | date: "%Y-%m-%d" }}">{{ page.last_modified_at | date: "%B %-d, %Y  %r  %Z %z" }}</time></p>



### Coronavirus Tracking sites and Data Sources  
- [Johns Hopkins Tracker](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6){: target="_blank"}  -- Dashboard tracking the global outbreak  

- [worldometer](https://www.worldometers.info/coronavirus/){: target="_blank"}   -- High Level coronavirus stats for all the countries in the world      

- [The Covid Tracking Project](https://covidtracking.com){: target="_blank"} -- The most complete testing dataset I've found, aggregating information from  state public health authorities    

- [The New York Times Data Files](https://github.com/nytimes/covid-19-data){: target="_blank"}  -- NYT compiles data at the state and county level from state and local governments      

- [The New York Times Growth Tracker](https://www.nytimes.com/interactive/2020/04/03/upshot/coronavirus-metro-area-tracker.html){: target="_blank"}  -- Different data visualization tools to examine how fast coronavirus is spreading   


- [University of Washington Institute for Health Metrics and Evaluation](https://covid19.healthdata.org/projections){: target="_blank"}   -- Projections on when peak new cases and peak new deaths will happen along with impact to projected hospital resources   

- [1point3acres](https://coronavirus.1point3acres.com/en){: target="_blank"}  -- The core data is similar to other sites, but the visualizations are slightly different, and they are starting to track things like PPE requests and jobs (hiring and layoffs)     

## What caught my eye today    

Sadly, the daily death count jumped yesterday, to over 1,900.  

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200408_1586374197_.png){: .align-center}


<br/>  
To put this daily total in perspective, according to the CDC mortality data[^5], there were 2,813,503 deaths in 2017.  


**The leading causes:**   

|  Cause | Total Deaths |  
| :---: | ---: |  
| Heart Disease | 647,457 |  
| Cancer | 599,108 |  
| Accidents | 169,936 |  



Influenza & Pneumonia is the 8th highest leading cause of death with 55,672 deaths in 2017. As of this writing, the total number of reported COVID-19 deaths in the US is approaching 13,000.
{: .notice--info}  


Given we are still in the early days of the outbreak, the rate of change is more telling then the cumulative totals.  To compare mortality, compute the average deaths per day for each leading cause and compare to COVID-19 for 7-April-2020.   

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200408_1586375084_.png){: .align-center}

## Daily Summary  

**Data as of:  7-April-2020[^1]**  

The data shows physical distancing is working. The daily growth rate continues to decrease, which means there are fewer new cases each day, and subsequently the number of days until the current number of cases double is improving (aka increasing.)   

The daily growth rate appears to have stabilized and the last 3 days has been approximately 8.7%.

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200408_1586371494_.png){: .align-center}    

Testing throughput continues to improve, but in my opinion is not yet sufficient to effectively manage the relaxation of physical distancing guidelines. (It looks like data April 4th is bad data.)  

Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days. This thought experiment is only to suggest the scale of testing that might be necessary for effective public health management as part of a strategy to relax physical distancing restrictions.  
{: .notice--info}


***  

More to come here, but for folks who received my emails, I discussed **Growth Factor**[^4] as a ratio of new cases today compared to new cases yesterday. As long as growth factor > 1, exponential growth will continue. A Growth Factor = 1, is the inflection point; that is, the point when new case growth changes from exponential to logarithmic. Stopping exponential growth is a critical first step to managing the pandemic.  

![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200408_1586371414_.png){: .align-center}


## Fighting COVID-19  

The two best tools we have today

- Avoid infection and transmission by physical distancing

- Blood Plasma Transfusion from people who have recovered  

  [Johns Hopkins convalescent serum therapy](https://hub.jhu.edu/2020/04/08/arturo-casadevall-blood-sera-profile/){: target="_blank"}  

  [National COVID-19 Convalescent Plasma Project](https://ccpp19.org/index.html){: target="_blank"}

  [In use in NYC](https://www.nbcnews.com/health/health-news/plasma-treatment-being-tested-new-york-may-be-coronavirus-gamechanger-n1178436){: target="_blank"}

  [More info at the Red Cross for Recovered Patients](https://www.redcrossblood.org/donate-blood/dlp/plasma-donations-from-recovered-covid-19-patients.html){: target="_blank"}


## Citations

[^1]:  <cite>Data for these charts sourced from [The Covid Tracking Project](https://covidtracking.com)</cite>

[^2]:  <cite>Healthcare employment data from [Kaiser Family Foundation](https://www.kff.org/other/state-indicator/total-health-care-employment/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D){: target="_blank"} </cite>  

[^3]:  <cite>Worldometer Incubation [data page](https://www.worldometers.info/coronavirus/coronavirus-incubation-period/){: target="_blank"}</cite>

[^4]: <cite>[3 Brown 1 Blue](https://youtu.be/Kas0tIxDvrg){: target="_blank"} for inspiration on calculating growth factor</cite>  

[^5]:  <cite>[CDC Mortality Data](https://www.cdc.gov/nchs/fastats/deaths.htm){: target="_blank"}</cite>
