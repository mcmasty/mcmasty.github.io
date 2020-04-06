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
excerpt: "I wasn't really finding the numbers I was curious about so I started crunching the data myself."
intro:
  - excerpt: There are a number of excellent coronavirus tracking websites (see list below) and many of them are making their data sources available. I found myself jumping between pages and sites, doing a few calculations I was interested in, and then emailing my analysis to friends and family. After a few weeks of this, I finally decided to start to move a few bits of analysis to the web. This page will update as I repeat analysis I like or share more of my past work to the web.      

---



{% include feature_row id="intro" type="center" %}

### Coronavirus Tracking sites and Data Sources  
- [Johns Hopkins Tracker](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6){: target="_blank"}  -- Dashboard tracking the global outbreak  

- [worldometer](https://www.worldometers.info/coronavirus/){: target="_blank"}   -- High Level coronavirus stats for all the countries in the world      

- [The Covid Tracking Project](https://covidtracking.com){: target="_blank"} -- The most complete testing dataset I've found, aggregating information from  state public health authorities    

- [The New York Times Data Files](https://github.com/nytimes/covid-19-data){: target="_blank"}  -- NYT compiles data at the state and county level from state and local governments      

- [The New York Times Growth Tracker](https://www.nytimes.com/interactive/2020/04/03/upshot/coronavirus-metro-area-tracker.html){: target="_blank"}  -- Different data visualization tools to examine how fast coronavirus is spreading   


- [University of Washington Institute for Health Metrics and Evaluation](https://covid19.healthdata.org/projections){: target="_blank"}   -- Projections on when peak new cases and peak new deaths will happen along with impact to projected hospital resources   

- [1point3acres](https://coronavirus.1point3acres.com/en){: target="_blank"}  -- The data presented here is slightly different than other sites and they are starting to track things PPE requests and jobs     




## Daily Summary 5-April-2020[^1]  

The data shows physical distancing is working. The daily growth rate continues to decrease, which means there are fewer new cases each day, and subsequently the number of days until the current number of cases double is improving (aka increasing.)  


![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200406_1586223856_.png){: .align-center}    

Testing throughput continues to improve, but in my opinion is not yet sufficient to effectively manage the relaxation of physical distancing guidelines. (It looks like data April 4th is bad data.)  

Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days.
{: .notice--info}


***  

More to come here, but for folks who received my emails, I discussed **Growth Factor**[^4] as a ratio of new cases today compared to new cases yesterday. As long as growth factor > 1, exponential growth will continue. A Growth Factor = 1, is the inflection point; that is, the point when new case growth changes from exponential to logarithmic. Stopping exponential growth is a critical first step to managing the pandemic.  

![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/daily_recap_20200406_1586214683_.png){: .align-center}

[^1]:  <cite>Testing Data from [The Covid Tracking Project](https://covidtracking.com)</cite>

[^2]:  <cite>Healthcare employment data from [Kaiser Family Foundation](https://www.kff.org/other/state-indicator/total-health-care-employment/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D){: target="_blank"} </cite>  

[^3]:  <cite>Worldometer Incubation [data page](https://www.worldometers.info/coronavirus/coronavirus-incubation-period/){: target="_blank"}</cite>

[^4]: <cite>[3 Brown 1 Blue](https://youtu.be/Kas0tIxDvrg){: target="_blank"} for inspiration on calculating growth factor</cite>  
