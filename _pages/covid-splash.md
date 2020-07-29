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
last_modified_at:  2020-07-29 23:45:00 -0400   


new_death_slug:                     new_death_20200729_1596007764           
leading_causes_slug:                leading_causes_20200729_1596007765      
daily_update_slug:                  daily_update_20200729_1596007769        
growth_factor_slug:                 growth_factor_20200729_1596007770       
logistic_curve_slug:                logistic_curve_20200729_1596007771      
recoveries_slug:                    recoveries_20200729_1596007772          
high_level_testing_slug:            high_level_testing_20200729_1596007773  
positive_test_proportion_slug:      positive_test_proportion_20200729_1596007776


state_new_case_proportion_slug: state_new_case_proportion_20200729_1596007819
state_trail_14d_case_proportion_slug: state_trail_14d_case_proportion_20200729_1596007819
state_total_case_proportion_slug: state_total_case_proportion_20200729_1596007820
state_new_tests_proportion_slug: state_new_tests_proportion_20200729_1596007820
state_new_death_proportion_slug: state_new_death_proportion_20200729_1596007820  


hot_zone_areas_slug: hot_zone_areas_20200729_1596007851  
middle_areas_slug: middle_areas_20200729_1596007855  
under_control_areas_slug: under_control_areas_20200729_1596007859

dgr_mvg_avg: 1.4

testing_snippet: "USA - Case Fatality Rate: 3.3%, Test-Positivity: 8.2%, Test per 1k pop: 160"

gfac_msg: "Aiming at a daily target below 1,000 new cases and given the recent 4d average Growth Factor (daily multiplier) of **0.95**, assuming this remains constant, it will take approximately **76.1 days** to get below 1,000 new cases daily. (For reference, a growth factor of 0.75 would reach the 1,000 new case threshold in 13.8 days).  "  


---


<!-- {% include plotly.html %} -->

{% include feature_row id="intro" type="center" %}


<p class="page__date"><strong><i class="fas fa-fw fa-calendar-alt" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Updated:" }}</strong> <time datetime="{{ page.last_modified_at | date: "%Y-%m-%d" }}">{{ page.last_modified_at | date: "%B %-d, %Y  %r  %Z %z" }}</time></p>



**Data as of: 28-July-2020[^1]**  

## tl;dr[^11] summary  

**Just The Data:**   
United States for 28-July-2020[^1]:  


- Total Positive Tests: 4,328,695; Total Tests: 52,985,577; Average Test-Positivity: 8.2%; National Tests per 1k. pop: 160  

- New Positive Tests: 53,507; Peak New Positive Tests: 77,233 [on 17-Jul-2020]; 7-Day Average New Cases: 64,448  

- Daily Test Total: 733,243; Daily Test-Positivity: 7.3%   

- Daily Tests, Trailing 7-Day Avg.: 813,889;  Test-Positivity, Trailing 7-Day Avg.: 7.9%   

- Total Fatalities: 141,430;  Case Fatality Rate: 3.3%   

- New Fatalities: 1,121; Peak Fatalities: 2,740 [on 07-May-2020]   


_FYI: This site treats positive tests to be an approximation for cases, and may use cases and positive tests interchangeably._
{: .notice--warning}   



<br>


**Monthly Data**  

| Month | New Cases<br>per month | New Cases<br>dly avg | DGR<br>avg | GF<br>avg | Total Tests<br>per month | T-Pos<br>avg | Tests<br>per 1k | Deaths | Death<br>per 100k | CFR<br>avg | In ICU<br>dly avg |  
| --- | ---: | ---: | :---: | :---: | ---: | :---: | :---: | ---: | :---: | :---: | ---: |  
| Mar | 199,029 | 7,371 |23.1% | 1.24 | 1,095,131 | 18.2% | 3.3 | 4,200 | 1.3 | 2.1% | 2,382 |  
| Apr | 875,668 | 29,189 |5.8% | 1.01 | 5,219,923 | 16.8% | 15.7 | 53,925 | 16.3 | 6.2% | 12,033 |  
| May | 720,087 | 23,229 |1.7% | 1.00 | 10,735,607 | 6.7% | 32.4 | 40,640 | 12.2 | 5.6% | 10,315 |  
| Jun | 832,203 | 27,740 |1.3% | 1.03 | 15,257,953 | 5.5% | 46.0 | 21,371 | 6.4 | 2.6% | 5,947 |  
| Jul | 1,700,951 | 60,748 |1.8% | 1.01 | 20,675,026 | 8.2% | 62.3 | 21,278 | 6.4 | 1.3% | 7,122 |  


_You can find column heading definitions in the [state level snapshot](#state-level-snapshot) section below._  


<br>
#### New Cases over the last 14 Days  

![Trailing 14d New Case Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.state_trail_14d_case_proportion_slug }}.png){: .align-center}  


<!-- horizontal amber <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> -->
<!--  red up <i class="fas fa-arrow-up" style="color: red;"> </i>-->
<!--  green down <i class="fas fa-arrow-down" style="color: green;"></i> -->

**My take**  
It seems the path forward will be a roller coaster of progress and regression (the growth factor moving average demonstrates this), as result, my commentary will be less focused on day to day changes.  While the daily trends are variable, the _big_ trends are positive (April was better than March), but the _small_ trends are  volatile (a single day may be better or worse than the day before).  I think the [growth factor moving average chart](#growth-factor) tells the story most succinctly.   

<!--  

- <i class="fas fa-arrow-up" style="color: red;"> </i> 37 states [have shown increasing cases](#experimental-charts) in the last 7d

- <i class="fas fa-arrow-down" style="color: green;"> </i> March average daily growth rate: 29%;   April average daily growth rate 5.9%.  

- <i class="fas fa-arrow-up" style="color: green;"> </i> March average doubling days of 2.6 days;  April average doubling days of 15 days.  


- <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> New fatalities remain above 1,600, but well below peak values.    
-->  

<!--
- <i class="fas fa-arrows-alt-h" style="color: #ffbf00;"></i> New Cases remain over 20,000, you can see the regression of growth factor as we slide back down the (logistic) growth curve.            
-->  

<br>
<!--http://localhost:5000/covid-page/#coronavirus-tracking-sites-and-data-sources -->

FYI:  [My list of Coronavirus Tracking sites and data sources.](#coronavirus-tracking-sites-and-data-sources)



## Impact in Lives Lost  


![New Death Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.new_death_slug }}.png){: .align-center}


<!--
There is a clear spike in reported deaths every 6-8 days, (Sa. April-4, Sa. April-11,  Wed. April-15, Tu. April-21, Wed. April-29, Tu. May-5).  I wonder if there is a systemic reason for this (e.g. pattern of when deaths are reported to health department or past deaths reclassified) or if the reported data is accurately reflecting a pattern in the actual COVID-19 fatalities (i.e. there are periodic spikes in the new case data)?  If you happen to know any systemic reasons amplifying this pattern, I'd love to know the answer; [drop me a line.]({{ site.url }}{{ site.baseurl }}/contact/)     
{: .notice--info}  
-->


<!-- {% include state_death_treemap.html %}{: align="center"} -->


![New Death Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.state_new_death_proportion_slug }}.png){: .align-center}




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

![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.leading_causes_slug }}.png){: .align-center}

## Spread / Containment      


The data shows physical distancing is working. The macro trend is that the daily growth rate is decreasing, and subsequently the number of days until the case count doubles is also improving, i.e. increasing.  

The daily growth rate is now stabilizing well below 2%, with the 3-day moving average currently at {{ page.dgr_mvg_avg }}%.  


![Daily Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.daily_update_slug }}.png){: .align-center}    


<br/>  

### Growth Factor    

Growth factor is a measure of how quickly the infection (new cases daily) is growing. You can think of this as a *daily multiplier*, that is, what do you need to multiply yesterday's new case count by in order to reach today's new case count. For example, if yesterday's new case count were 437 and the growth factor were 1.2, then today's case count would be 524, and the infection would be spreading rapidly, or if the growth factor were 0.8 then todays case count would be 350, and the infection would be dying down.


A growth factor < 1 (green area on chart), means there are fewer cases today then yesterday, and If we can keep that up long-enough, the outbreak will die down. In a perfect world the growth factor would approach 0, meaning no new cases.  


_Growth Factor_[^4] is calculated as a ratio of new cases today compared to new cases yesterday.  


![Growth Factor Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.growth_factor_slug }}.png){: .align-center}


Repeated multiplication results in exponential growth, however pandemics will not grow exponentially forever. At some point the growth will shift to linear growth, and eventually, the growth will level out or stop. The resulting shape of combining these properties is a logistic curve. The growth factor is also the instantaneous slope of a point on the logistic curve. We can plot points based on growth factor values to estimate where we might be on the trajectory of the pandemic.


![Logistic Curve Summary]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.logistic_curve_slug }}.png){: .align-center}  

Since growth factor is the _daily multiplier_ we can use this value to estimate how long until we are below some threshold number of daily new cases.  

{{ page.gfac_msg }}  

> All models are wrong, but some are useful.  
> <cite>George Box</cite>  

See notes[^9] [^10] for more details on logistic curve and growth factor.


## Testing Snapshot


![High Level Testing]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.high_level_testing_slug }}.png){: .align-center}



<!-- It appears testing throughput has increased to approach the 200k test per day, up from the 150k per day plateau of the last few weeks.  -->



Thought experiment on testing:  There are roughly 17,000,000 health care workers in the U.S.[^2]. The average incubation period of coronavirus is around 5 days[^3]. Until treatments are available, to keep our healthcare workers safe, a weekly test seems pragmatic.  17 million divided by 7 days  is roughly 2.4 million tests per day, or 3.4 million tests per day if we test every 5 days. This thought experiment is only to suggest the scale of testing that might be necessary for effective public health management as part of a strategy to relax physical distancing restrictions.  
{: .notice--info}



**How much testing is enough?**   
One measure might be the proportion of positive tests as a share of total testing. We know that asymptomatic contagious individuals are making this outbreak particularly challenging to deal with. Any attempt to identify the asymptomatic carriers of the disease will require testing many healthy people, who are also asymptomatic. The impact of testing more asymptomatic people, would drive down the number of positive tests as more healthy people are tested.   

The below graph shows the number of positive tests as a proportion of total testing.  
![Positive Test Proportion]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.positive_test_proportion_slug }}.png){: .align-center}  




**Comparison to other Countries[^7]:**   

{{ page.testing_snippet }}       


| Country | Pop. | Cases | Test Positivity | Case Fatality Rate | Test Per 1k Pop
| :--- |  ---: | ---: | ---: | ---: |  ---: |
| Taiwan     |     23.8 M |       455 |     0.6% |     1.5% |        3 |  
| S. Korea   |     51.3 M |    13,771 |     0.9% |     2.1% |       29 |  
| Iceland    |      0.3 M |     1,930 |     1.7% |     0.5% |      332 |  
| UK         |     67.9 M |   294,792 |     2.2% |    15.4% |      196 |  
| Germany    |     83.8 M |   202,845 |     2.9% |     4.5% |       82 |  
| Russia     |    145.9 M |   771,546 |     3.1% |     1.6% |      171 |  
| Canada     |     37.8 M |   110,338 |     3.1% |     8.0% |       93 |  
| Italy      |     60.5 M |   244,434 |     3.9% |    14.3% |      103 |  
| India      |  1,380.7 M | 1,118,107 |     8.1% |     2.5% |       10 |  
| Sweden     |     10.1 M |    77,281 |    11.3% |     7.3% |       67 |    



Test positivity is measured with aggregate test data unless noted otherwise.

{% capture testing-example %}
Thought experiment on test-positivity: If we use 4% as a threshold for relaxing physical distancing, there are two levers we can pull to reach it; (1) decrease the number of new positive tests ( aka continue with physical distancing measures), (2) increase the number tests completed each day.

Assuming a testing capacity around 800,000 test per day, 4% of that number is 32,000.  To reach 4% positive test proportion, we'd need to keep physical distancing guidelines in place until the number of new cases falls to 32,000 per day.  

Alternatively, using 65,000 as the average number of new cases, we'd need 1,625,000 total daily tests, with all additional tests to be negative, for the proportion of positive results to be 4%.  

Ideally we will make progress on both strategies.  
{% endcapture %}  

<div class="notice--info"> {{ testing-example | markdownify }} </div>



### State Level Snapshot

Field definitions:  

Generally a `*` means this metric is a moving-average.

- `State` State code, followed by that state's contribution to the total number of new cases as a percent.
- `Pop.` is state population in millions  
- `Cases` is the total number of cases measured by positive test results  
- `New.C` New Cases. Lower is better.
- `DGR*` Daily Growth Rate. This is 4-day, exponential moving average. Lower is better.
- `Tests per 1k` is number of tests per 1,000 in state's population. Higher is better.   
- `T-Pos.` is the test-positivity percentage; ratio of positive tests to total tests.  Lower is better.     
- `Fat.`  Total number of fatalities
- `Fat./1M`  number of deaths per 1 million in population  
- `CFR*`  Case Fatality Rate. Exponential moving average with a 4-day span.
- `GF*` Growth Factor, 4-day span, exponentially weighted moving average. Todays value has more weight, than the measure of 4 days ago.  Lower is better.    
\- `GF-14day`   Summation of GF-m.a. from last 14 days. The lower the better. Values below 14 indicate exponential has stopped.   
- `Dbl.Days`  Given the current daily growth rate, how many days until cases double.  Higher is better.    
- `CDD` Consecutive days of declining new cases or new cases at or below a threshold of 5.[^12]   A value greater than 14, might signal preparedness to reopen. This may be too rigorous, see notes[^12] for more detail.     
- `As-Of Date`  the date when the data was last modified

- `SparkLines`  The embedded graphs in the table are a plot of the last 14-days of the metric in question. For example, in the `Cases` column, the sparkline shows visually how the total number of cases has changed over the last 14 days. Similar metrics share a color; metrics related to cases are gray, testing are brown, fatalities are blue, and (exponential) growth are black.  

{%  include state_table.md  %}




<br>

**State's share of new cases today**  

![New Case Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.state_new_case_proportion_slug }}.png){: .align-center}  

![New Tests Proportions]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.state_new_tests_proportion_slug }}.png){: .align-center}  





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

  ![Recoveries]({{ site.url }}{{ site.baseurl }}/assets/images/covid/{{ page.recoveries_slug }}.png){: .align-center}


<br/>

Hopefully coming soon, a number of vaccines and treatments.   [Summary of Vaccine and Treatments](https://www.visualcapitalist.com/every-vaccine-treatment-covid-19-so-far/?from=timeline&isappinstalled=0){: target="_blank"}

[Summary of Treatment Research by WHO](https://www.who.int/blueprint/priority-diseases/key-action/novel-coronavirus/en/){: target="_blank"}  


This is not an exhaustive list; anything missing is accidental.  

***   

## Experimental Charts  

I am experimenting. As a result, this section might be short-lived as I am not sure how this will be folded into the site, if at all. This section also may not be updated as frequently.

**State and U.S. Territory Trends** 14-day slope, 7-day slope  

A measure of how a state is trending over the last 14 days and last 7 days, presented as color coded icons,
one for each period. The 14 day period is the first icon and the second icon represents the 7 day period.
A red up arrow <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>
means the trendline is up (positive slope),
a green down arrow <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>
means the trendline is down (negative slope),
a yellow horizontal arrow <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>
means the trendline is flat,
a green chevron <i class="fa fa-chevron-left" aria-hidden="true" style="color: green;"></i>
means the average daily new cases is below a threshold of 5 new cases per day; so 70 new cases in
the last 14 days or 35 new cases in the last 7 days.


I think this assessment is lower order than peak coverage percentage. That is, peak cover percent is a better summary of
the overall status and these arrows are just the recent trends.  


- <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>, <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>: 12 States: AR, HI, MA, MD, NH, NJ, NM, OK, PA, PR, RI, VA
- <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>, <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>: 3 States: DC, ND, WY
- <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>, <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>: 8 States: CO, CT, IL, IN, KY, MN, MS, NE
- <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>, <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>: 2 States: ME, OR
- <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>, <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>: 1 States: VT
- <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>, <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>: 3 States: DE, SD, WV
- <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>, <i class="fas fa-arrow-up" aria-hidden="true" style="color: red;"> </i>: 3 States: AK, MI, WA
- <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>, <i class="fas fa-arrows-alt-h" aria-hidden="true" style="color: #ffbf00;"></i>: 1 States: VI
- <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>, <i class="fas fa-arrow-down" aria-hidden="true" style="color: green;"></i>: 20 States: AL, AZ, CA, FL, GA, IA, ID, KS, LA, MO, MT, NC, NV, NY, OH, SC, TN, TX, UT, WI
- <i class="fa fa-chevron-left" aria-hidden="true" style="color: green;"></i>, <i class="fa fa-chevron-left" aria-hidden="true" style="color: green;"></i>: 3 States: AS, GU, MP  



### Proximity to peak cases  

This section is a geometric analysis in which the area under peak number of cases (orange line) is compared to the actual cases (blue line and shaded area). The percent of peak area, bounded by the peak cases line, that is covered by the actual cases area, is a metric I call "Peak Coverage".  The higher the percent, the closer the state is to average peak conditions.    

The peak line is defined by the average of 3 highest values in the last 8 weeks.  

The visual explanation is more straight forward: The greater the green area, the greater the distance between new cases and peak cases.  Simply:  Mo' green, mo' better; No green, no good.  


The states are sorted in decreasing order of peak cover.


### States seeming near peak number of cases  
<figure style="width: 850px" >
  <img src="{{ site.baseurl }}/assets/images/covid/{{ page.hot_zone_areas_slug}}.png" alt="">
  <figcaption>The worst third states and territories based on actual cases coverage. </figcaption>
</figure>{: .align-center}  




### States "in the middle"  
<figure style="width: 850px" >
  <img src="{{ site.baseurl }}/assets/images/covid/{{ page.middle_areas_slug}}.png" alt="">
  <figcaption>States whose cases coverage falls in the middle third of values. </figcaption>
</figure>{: .align-center}  



### States whose new cases seem under control  
<figure style="width: 850px" >
  <img src="{{ site.baseurl }}/assets/images/covid/{{ page.under_control_areas_slug}}.png" alt="">
  <figcaption>States whose actual cases coverage is the third of states with the lowest values. </figcaption>
</figure>{: .align-center}  

<br>



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

[^12]: The Whitehouse published guidelines for reopening calls for a  "14-day downward trajectory" of declining metrics. Since "downward trajectory" is not precisely defined, this metric counts the number of consecutive days for each state that have a new case count less than the day before or less than or equal to 5. That is, for states with small case number (MT, HI, AK, VT, etc), the metric treats new cases equal to or less than a threshold of 5, the same as a day with declining case count.  This metric is counting consecutive days, which may be more rigorous than actual <cite>[Whitehouse / CDC Guidelines](https://www.whitehouse.gov/openingamerica/#criteria){: target="_blank"}) </cite> as single day of increasing metrics will reset the consecutive day count back to 0, and the Whitehouse only calls for a "downward trajectory".  
