---
title: Lending Club Analysis
date: 2020-03-02 19:34:30 Z
header:
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280,h:380,fit:crop/compress/WWsYBBGRnaIYRjfhXk4T"
  overlay_filter: 0.65
  caption: Photo by Mika Baumeister on Unsplash
  teaser: https://cdn.filestackcontent.com/resize=w:600,h:400,fit:crop/compress/WWsYBBGRnaIYRjfhXk4T
categories:
- Project
tags:
- Python
- Matplotlib
- Numpy
- Pandas
last_modified_at: 2020-03-17 16:39:00 -0400
excerpt: "Python & Pandas: Analyzing my Lending Club portfolio and Lending Club historical data"
--- 

A summary of the technical aspects of analyzing my Lending Club portfolio as well as Lending Club historical data.  


# Introduction  
This project summary is aimed at a more technical audience, focusing more on how the results were produced. If you are more interested in the conclusions of the analysis, [review the posts related](#posts-related-to-this-project) to this project.   

I am unsure how many posts the LendingClub series will ultimately comprise, therefore this summary will be more general to ensure it supports all the posts without getting unbearably long.  I will update this project summary when edits need to be made after writing additional posts in the series.  


## Background  
Having a general understanding of how loans work as an investment product is useful background. The necessary specific knowledge on peer-to-peer lending, or the specific tradable notes on offer, can be found on the LendingClub website.   

- [LendingClub Peer-to-Peer](https://www.lendingclub.com/investing/peer-to-peer){: target="_blank"}  

- LendingClub's [secondary market / tradeable notes](https://www.lendingclub.com/investing/investor-education/about-the-trading-platform){: target="_blank"}  



## Problem  
The general lines of inquiry are around the following topics:  

- How did my LendingClub investing perform historically  
- How should the investing strategy change  

Specific questions and analysis exploring one or both of these topics are covered in more detail in [individual posts related](#posts-related-to-this-project) to this project.  

<br/>  

# Data  

## Data Requirements  
The following data is required:

- **Notes Owned**  
  The notes I have purchased and hold in my account.  A **Note** is a fraction of a loan, so will have all the expected fields of a loan, such `Principal`, `Interest Rate`, and `Issue Date`, along with many more. Review the API docs in the [data sources](#data-sources) section below for more details.  


- **Lending Club Loans**  
  Loans issued by LendingClub. These loans are the source instruments for the individual notes purchased by investors. 

- **Lending Club Summary Statistics**  
  LendingClub provides some high level statistics on all the loans they have issued. Example statistics include, but not limited to, average interest rate, grade mix per issue date year, and loan performance summaries.  

## Data Sources  
There is no budget for data acquisition, and as a result, all data must be freely available or included as with existing accounts.  

- **My Owned Notes**  
  Data was collected using the [LendingClub API](https://www.lendingclub.com/developers/api-overview){: target="_blank"}.   

- **LendingClub Loan Data**  If you have a LendingClub account, you can download historical loan data with [the download data link on this page.](https://www.lendingclub.com/info/statistics.action){: target="_blank"}  

- **LendingClub Summary Statistics**  The summary statics can be [accessed here](https://www.lendingclub.com/info/demand-and-credit-profile.action){: target="_blank"}


## Data Preparation  

### Collection & Cleaning  
This section details specific issues, decisions, and assumptions that might have impacted data collection or cleansing.  

**Owned Notes / My Portfolio**  
The data for owned notes is accessed via REST API endpoint, it is returned in a JSON format. The JSON data is then converted into a Pandas DataFrame.  

The majority of the cleansing is converting individual fields to the appropriate data type, the most common was converting strings to date field, for fields such as `Issue Date` or `Last Payment Date`.  

Owned notes is a relatively small data set, on the order of 1,300 records.  


**LC Historical Data**   
LendingClub has issued over 4 million loans, compared to owned notes, the loan dataset is very large. From a data collection and preparation perspective, a minor challenge is managing and merging the multiple files which are required to get a complete dataset.   

Cleansing of loan data is similar to cleansing the note data, the majority of work is converting to appropriate data types.


### Representative Data  
The topics in the [problem section](#problem) explore financial gain or loss of a collection of notes, and how those notes might be selected differently in the future. These notes are created from the LendingClub loan pool. Therefore using LendingClub historical loans to build comparisons for a set of notes (my portfolio) is a representative dataset to analyze the problems outlined above.  


<br/>  




# Methodology  
This section outlines the decision made around analysis and modeling.  

## Modeling  
While the full history of LendingClub loan data is an appropriate dataset to use for analysis, how that data is used to create models is evolving. Data analysis is iterative. As more understanding of the data or performance is gained, it may require changes to modeling. Completing the analysis for a post may provide insight to change the modeling to support future posts.  


One area with open questions is sampling of the LendingClub historical data. The use of specific sampling techniques will be driven by the analysis being done, and therefore part of the analysis will be focused on questions around the sampling of the loan data.  


### Comments for LendingClub Post 1  
The initial LendingClub post focuses on exploratory analysis. Therefore, the analytic approach will be descriptive in nature, focusing on sums, proportions, etc.  

Regarding LendingClub historical loans, a convenience sample will be used covering the period of 2007 to 2016.  
  
  - This dataset is approximately 1.3 million loans.  

  - The longest loan term on offer from LendingClub is 60 months, therefore should be very few "current" loans in this period. As a result, the data won't need to be refreshed frequently to stay relevant.  

  - This period requires a smaller number of data files than other periods of the same length. 8 data files are required for the period of 2007 to 2016, but 4 of those files are for 2016. Starting in 2016, LendingClub issues quarterly data files.  


Since the primary objective is descriptive analysis, the full population of loans from 2007 - 2016 will be used in the analysis.  


Additional information on data usage is provided [in the first post.]({% link  _posts/2020-02-20-lending-club-part-one.md %})

# Technology Tools

Below is a list of all the major technology tools and libraries used in this analysis project. 

### Python & "core" libraries  
- Python 3
- Numpy
- Pandas
- Requests

#### Misc Libs (less mainstream libraries )  
- pyarrow / feather  for storing data frame after processing csv's.  This is a python implementation of feather binary serialization format as part of [apache arrow](https://arrow.apache.org){: target="_blank" }  

### Visualizations
- Matplotlib  

### Platform & tools
- Jupyter Notebook
- IBM Watson Studio
- IBM Object Storage



## Review the code  
_Look at the code:_  You can [browse the notebook](https://github.com/mcmasty/stunning-fortnight/blob/master/lending_club_analysis/My%20LC%20Portfolio%20Notes%20Analysis.ipynb){: target="_blank"}  I used to analyze my lending club portfolio on GitHub.



# Posts related to this project  

Below is a list of the related posts using analysis from this project.

<ul>
  {% assign my_posts = site.posts | sort: "date" %}
  {% for post in my_posts %}
    {% if post.project_id == "lc_analysis_2020" %}
    <li><a href="{{ post.url }}">{{ post.title}}</a>
    </li>  
    {% endif %}
  {% endfor %}
</ul>


***  
### Get in Touch  
Have a similar project ? Feel free to [reach-out to me](/contact/){: target="_blank"} if you'd like additional information, about the tools, my workflow, or anything else.