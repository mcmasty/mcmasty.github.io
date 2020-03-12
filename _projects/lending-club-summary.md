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
last_modified_at: 2020-03-02 21:20:02 Z
excerpt: "Python & Pandas: Analyzing my Lending Club portfolio and Lending Club historical data"
---  


A summary of the technical aspects of analyzing my Lending Club portfolio as well as Lending Club historical data.

## Tech Stack

#### Python & "core" libraries  
- Python 3
- Numpy
- Pandas
- Requests

#### Misc Libs (less mainstream libraries )  
- pyarrow / feather  for storing data frame after processing csv's.  This is a python implementation of feather binary serialization format as part of [apache arrow](https://arrow.apache.org){: target="_blank" }  

#### Visualizations
- Matplotlib  

#### Platform & tools
- Jupyter Notebook
- IBM Watson Studio
- IBM Object Storage


## Data Flows

**My Portfolio**  
- Lending Club REST API endpoint, data captured in JSON.  
- Convert JSON to Pandas DataFrame  
- Perform clean-up and feature engineering.  
- Save cleansed DataFrame  


You can [browse the notebook](https://github.com/mcmasty/stunning-fortnight/blob/master/lending_club_analysis/My%20LC%20Portfolio%20Notes%20Analysis.ipynb){: target="_blank"}  I used to analyze my lending club portfolio on GitHub.


**LC Historical Data**   
- Download multiple CSV's  
- Load CSV's into DataFrames (one per file)  
- Concatenate all DataFrames into a single on  
- Drop unnecessary data, clean-up, feature engineering.  




## Posts related to this project  

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
