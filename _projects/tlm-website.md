---
title: tlm13 Website
date: 2020-03-10 19:34:30 Z
excerpt: How I arrived at a Jekyll based website.
header:
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280,h:380,fit:crop/auto_image/compress/THb1f9EkR8y1WHWLXZwz"
  overlay_filter: 0.6
  caption: Photo by Hal Gatewood on Unsplash
  teaser: https://cdn.filestackcontent.com/resize=w:600,h:400,fit:crop/auto_image/compress/THb1f9EkR8y1WHWLXZwz
categories:
- Project
tags:
- Jekyll
- Content
- github
- Jekyll
last_modified_at:  2020-03-17 13:41:00 -0400
---


This project summary outlines how I decided upon a Jekyll based website.  


## Website vs Blog - What ballpark to play in    
The first major decision was if I really needed a website. If all I intended to do is write posts, perhaps a blogging solution, such as Medium, micro.blog, or even LinkedIn, would better suit my needs. I didn't have a clear picture of what I wanted this site to be, so I will outline the considerations that shaped the decisions.  

Primary considerations:  
 - _The kind of content to be published._ I am thinking about sharing content which is quite broad thematically. I can envision posts that are topical summaries, essays, project summaries, formal reports, sharing code, as well as personal DIY projects.  

 - _The structure of the content._ Since I am at the beginning, I want to keep the focus on what I am trying to communicate and not how to structure it, that is format it to conform with a specific tool. Given the broad thematic range in the previous point, flexibility on structure is beneficial, as each of the listed content types, may benefit from having specific content structure tailored to that content type.  The gist, is that I think multiple content structures will be inevitable.  

- _Action creates clarity._  At this stage, it's not clear to me how I would organize by substance or structure; I have no content to analyze.  The process of actually publishing content will provide the crucible to see which ideas actually come to fruition and which ideas should be discarded. Being able to iterate with different approaches with the least amount of re-work is important to this project.  


If the content were homogeneous, it would be an easier selection. For example, if I knew I would only be writing a collection of opinion pieces, a blog-site like Medium would be an ideal choice. However, the content is not homogeneous. Publishing mixed content types combined with the importance of supporting experiments of different structures and presentations, has nudged me to implement a proper website.  



## Broad Requirements and Relative Priority  
The decision to build a website brings the next round of questions: how best to build what I am looking for?  My first step was to outline some high level goals and requirements for the project, and group them into priority tiers, to ensure the most important considerations carried the most sway.  


### Universal Tier    
- **Goal for site / what do I want out of site**  
  Currently my goal for this website is to share selected projects and writings, providing concrete examples of my work. Additionally, I believe decision making will become more important as remote work continues to be a force in the modern workplace. Having a forum to share these projects allows me to also make visible the normally hidden  work of learning, decision making, and judgment. You will be able to see not only what was created, but how I got there.  

- **What do I want visitors to do on the site**  
  From a visitor functionality perspective, it is straight forward; two main areas I want visitors to be able to do:  
    1. Find and read content, hopefully interesting or helpful to you.  
    2. Be able to reach out to me if you want to get in touch.  


The main benefit of this tier is selecting items for the list of candidates, if a tool does not meet the **Universal Tier** requirements, it cannot be on the list. Since, there are many ways to implement a solution to satisfy these requirements, these requirements provide little help in choosing one candidate tool over another.  


### Tier 1  
Dimensions with the most influence.  

- **Cost**  
  Whatever comes next for me, will be bootstrapped, so the least expensive, on a monthly cash-flow basis, will be preferred.  

- **Content**  
  The heart of this topic was covered in the content substance discussion in the introduction. One additional detail, the vast majority of the content I plan on authoring will be static, so support for dynamic content is not required.  


- **Flexibility**   
  The structure discussion in the introduction highlights the need for content-type to structure flexibility, however, with so many unknowns in this project, flexibility in switching website builder tools should also be a consideration. If multiple tools have similar content-type flexibility, the ones with least amount of "lock-in" will be preferred.           


### Tier 2  
Dimensions with moderate influence.  

- **Existing Skills / Resources**   
  Ideally I would be able to hit the ground running; so tools that utilize existing skills will be preferred.  

- **Secondary Benefits**  
  Although I want to hit the ground running, I also want to continue to develop and improve my skills. Part of this project's objective is to gain, develop, or deepen my experience with technologies I am interested in.  


### Tier 3    
Dimensions with the least influence.   

- **User base**  
  How difficult will it be for the folks maintaining the website, to actually maintain the website.  

- **Ecosystem**  
  The simpler the ecosystem, and the fewer number of total tools the better. Cost is the primary driver, with secondary consideration for re-use of existing platforms.  


- **Classic Web Stuff**  
  Most of the modern website building tools provides solutions for many of the most common website considerations, and as a result I grouped all the most common issues related to launching a website into a single item. The specific tool assessment will boil down to an estimate of the learning curve required for each tool and how well a tool matches the Tier 1 and Tier 2 requirements.  


  - domain name  
  - registry  
  - hosting  
  - design  
  - branding  
  - UX / Navigation   

## Decision  
There is no shortage of options for how to build a website in 2020. I have some Drupal experience from a previous project and I also quickly inspected of some the more popular options today - Wix, Squarespace, WordPress, and others. Each option seemed great in isolation, but intuitively I didn't feel like they were ideal fits for me; many options were ruled out due to higher cost than my budget would support.  


Knowing that most of my content will be static, I parked searching for additional 'drag and drop' website builders and started investigating static-site generators. Very early in the search process I discovered Jekyll, and soon thereafter learned [GitHub Pages](https://pages.github.com) uses Jekyll under the hood. I currently use GitHub for my [code repositories](https://github.com/mcmasty), and since I am an existing customer I can use GitHub Pages as basically a no additional cost web-hosting service. This was enough to take a more detailed look at Jekyll / GitHub Pages.  


Having additional cost of $0 is a great start on addressing one of the highest priorities. In terms of the remaining Tier 1 priorities, Content and Flexibility, [jekyll](https://jekyllrb.com/philosophy/#3-content-is-king) is a solid choice. Content is authored in plain text files and written in markdown. Each website is a GitHub repository, so the website will have built in versioning for content. It's hard to be simpler or more flexible than a collection of plain text files. The look and feel of how the content is presented depends on straight forward configurations and themes, and many different themes exist, to provide many options at a satisfactory design. Plain text content, many different themes, straight forward configuration, all combine to make it easy to experiment with different ways to handling the content. From a Tier 1 requirements, Jekyll &  GitHub pages is a strong candidate.  


Addressing the Tier 2 benefit of leveraging existing skills. I have experience with templating solutions, specifically Jinja and Liquid from other projects. Jekyll also uses Liquid templating, so that makes it a little bit easier to hit the ground running. On an existing project, content is authored in markdown, so writing markdown content for Jekyll is no problem. Across my existing or past projects, I have experience with templates, markdown, and themes; so it is a small conceptual step to start using Jekyll to build websites.  


In terms of improving skills and experience, the last tier 2 priority, working on a modern static-site generator would be new to me. I last built a static website way back in mid-1990's, that is the days of basically coding HTML for every page. Since those early days, I have built web application servers, managed a Drupal (CMS) site, and worked on several projects that delivered dynamic content over the web; which is to say I have had a sampling of web experience. Working on a modern static-site generator provides the opportunity to extend that experience and observe the pro's and con's of static sites first hand, creating more range of tools in my toolbox.  


Cost, platform re-use, hitting the ground running, while also gaining new experience --- all that resulted in this **tlm13** website, a Jekyll built website hosted on GitHub Pages.  


Feel free to [reach-out to me](/contact/){: target="_blank"} if you'd like additional information, about the tools, my workflow, or anything else.


## Technology Recap

### Misc. Technology Used  
- **Static Site Generator:** Jekyll  
  - Current Theme: [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/){: target="_blank"}
- **Content Authoring Format:** markdown  
- **Content Versioning:** GitHub  

### Applications & Tools
- **Short Posts, Confg File editing:**  [Atom Text Editor](https://atom.io){: target="_blank"}
- **Writing Longer Posts:**  [Scrivener](https://www.literatureandlatte.com/scrivener/overview){: target="_blank"}
- **Photo Editing:** [Affinity Photo](https://affinity.serif.com/en-us/photo/){: target="_blank"}
- **Working with Git Repository:** [GitHub Desktop Client](https://desktop.github.com){: target="_blank"}

### Platforms, Servers, Hosting   
- **Website Hosting:** [GitHub pages](https://pages.github.com){: target="_blank"}
- **Domain Registry, DNS:** [GoDaddy](https://www.godaddy.com/){: target="_blank"}
- **Forms:**  [Formspree](https://formspree.io){: target="_blank"}
- **CDN:**  [Filestack](https://www.filestack.com){: target="_blank"}  

### Photos and Imagery
- [Unsplash](https://unsplash.com){: target="_blank"}  
- [iStock](https://www.istockphoto.com){: target="_blank"}
- My own work  

### Other Gear
- iPhone X  (photos)
- Panasonic GH5  
