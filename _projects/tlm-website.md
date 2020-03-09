---
title: tlm13 Website
date: 2020-02-29 19:34:30 Z
excerpt: How I arrived at a Jekyll based website.
header:
  overlay_image: "https://cdn.filestackcontent.com/resize=w:1280,h:380,fit:crop/compress/THb1f9EkR8y1WHWLXZwz"
  overlay_filter: 0.6
  caption: Photo by Hal Gatewood on Unsplash
  teaser: https://cdn.filestackcontent.com/resize=w:600,h:400,fit:crop/compress/THb1f9EkR8y1WHWLXZwz
categories:
- Project
tags:
- Jekyll
- Content
- github
- Jekyll
last_modified_at:  2020-03-04 10:10:00 -0500
---  

This project summary will outline how I decided upon a Jekyll based website.


## Website vs Blog - What ballpark to play in  

The first consideration was if a website is actually the best choice.  Perhaps a blogging solution, either Medium, or micro.blog, or even LinkedIn might better suit my needs if all I want to do is write posts.

Two main considerations:  
 - I am thinking about sharing content which is quite broad thematically, topical summaries, essays, project summaries, formal reports, sharing code, as well as some DIY projects. Publishing all these different subject matters into single blog, seems forced to me. Creating multiple blogs, one per theme, seemed to lack an overarching cohesive structure.  

   Additionally, I am not sure I specifically know how best to group related content at this point. Throwing all content into a single pool with no structure, seems a high burden to potential readers, and creating structures that need to be replaced every few months is time-consuming, and usually arduous.


 - At this point in the process, I want to keep the focus on what I am trying to communicate and not how to format it to conform with any specific tool or platform. I don't know what I don't know. I have a conceptual idea of what I am trying to demonstrate, but no concrete examples. Being able to iterate with different approaches, to find what works best for me, with the least amount of re-work is very important.  


If the content were homogeneous, it would be an easier selection. For example, if I knew I would only be writing a collection of opinion pieces, an blog-site like Medium would be an ideal choice, however the content is not homogeneous. Additionally, supporting experimentation of different structures for different content types, has nudged me to select website for the general approach of creating my online presence.  


## Broad Requirements and Relative Priority

The decision to build a website brings the next round of questions: how best to build what I am looking for?  My first step was to outline some high level goals and requirements, and group them into priority tiers, to ensure the most important considerations carried the most sway.


### Universal Tier  
- **Goal for site / what do I want out of site**  
  Currently my goal for this website is to share selected projects and writings. I like to think, I like to learn, and I like to experiment. Having a forum to share these projects connects the sometime private work of learning to something more visible.


- **What do I want visitors to do on the site**  
  From a functionality perspective, it is straight forward, two main areas I want visitors to be able to do:  
    1. Find and read content, hopefully interesting or helpful to you.  
    2. Be able to reach out to me if you want to get in touch.  


These requirements would be the same for all potential solution options. There are many ways to implement a solution to meet these requirements. As a result, there is very little influence these considerations would have in choosing one option over another.



### Tier 1

Dimensions with the most influence.  

- **Cost**  
  Whatever comes next for me, will be bootstrapped, so the least expensive, on a monthly cash-flow basis, will be preferred

- **Content**  
  Right now, the vast majority of the content I plan on authoring will be static.

- **Flexibility**   
  With so many future unknowns, I can envision having to migrate to a different solution in the future. By flexibility, I mean the ease of migrating of content, as well as ease of winding down existing site.   


### Tier 2  

Dimensions with moderate influence.  

- **Existing Skills / Resources**   
  Want continue / use existing skills to hit the ground running.

  I have used templating tools in the past (Jinja, Liquid).  

  I currently write some content in markdown, so obviously have markdwon content and experience.



- **Secondary Benefits**  
  Learning & Development...

  Through this project a goal is to gain, develop, or deepen experience with technologies used in this project.

  I have used Drupal in previous projects, so am comfortable with CMS-backed, dynamic websites. I wanted to some practical experience with static-site generators.




### Tier 3  

Dimensions with the least influence.  

- **User base**  
  Currently it is only me and I do not need a fancy user interface.

- **Ecosystem**  
  The simpler and fewer the better. Cost is the primary driver, with secondary consideration for re-use of existing platforms.

  A reminder to be mindful of the Tier 2 "Secondary Benefits" priority, if it a platform where I would like additional experience on, that influence the technology choices.


- **Classic Web Stuff**  
  Most of these will be covered by learning how to use the technology selected or re-using existing tools. That is, how hard is it to use the technology selected to build a reasonably decent looking website. As a result, these areas, while important, were not considered independently.

  - domain name ... uh, [see about page](/about/){: target="_blank"} for naming this site  
  - registry ... re-use existing provider
  - hosting ... driven by Tier 1 &  Tier 2 considerations.
  - design ...  any solution will have templates / themes, so pick a theme that seems reasonable.   
  - branding ... do the minimum amount of branding to see how things evolve and adjust along the way.  
  - UX / Navigation ... similar to "design", pick a reasonable theme; learn and adjust along the way.


***  
***  
***  

- **Cost**   

- **Content**   

- **Flexibility**  
  Things have a way of changing, evolving once they are released to the wild. That is, I expect evolution once I start getting feedback.

- **User base**  
  Right now, this is a solo-endeavor.  I am comfortable with coding, markdown, using the command-line (terminal), etc.  So the lack of an admin or content editing UI is not an issue.  

- **Ecosystem**    
  In general, Fewer accounts, fewer servers  

-  **Classic Web Stuff**   ... domain name, registrar,  hosting, Design, Branding, UX / Navigation, Mobile / Responsive  

- **What do I want to do**  

- **What do I want visitors to do**  


## Decision  
There is no shortage of options for how to build a website today (in 2020). I have some Drupal experience from a previous project. I did a quick inspection of some the more popular options today - Wix, Squarespace, WordPress, and others. Each option seemed great in isolation, but intuitively I didn't feel like they were ideal fits for me; many options were ruled out due to higher cost than my budget would support.  


Blending cost with leveraging existing skills and experience, I ended up with [GitHub Pages](https://pages.github.com), since GitHub is what I use to manage my [code repositories](https://github.com/mcmasty). That is a win on the cost front, since GitHub Pages is basically a no additional cost web-hosting service from GitHub. With cost and platform re-use nudging me towards GitHub Pages, the **classic web considerations** have been dealt with.


In terms of the remaining Tier 1 priorities, **Content** and **Flexibility**, [jekyll](https://jekyllrb.com/philosophy/#3-content-is-king) is a solid choice.  The content is authored straight forward text files written in markdown, and since I am using GitHub, each page is version controlled.  The look and feel, as well as where content shows up, depends on straight forward configurations, and which directory the files are stored in. This is makes it very easy to experiment with different ways to handling the content.  


A tier 2 benefit (leveraging existing skills), is I have experience with templating solutions, specifically Jinja and liquid from other projects. Jekyll also uses Liquid templating, so that makes a little bit easier to hit the ground running.  On the project that uses Jinja templates, the core content is stored in markdown.  Basically, I am already using the core pattern of Jekyll but with Python and Jinja, so it is a small conceptual step to follow how Jekyll sites are built.    


In terms of improving skills (last tier 2 priority), I haven't worked on a static website since the days of coding HTML for every page.  I have built web application servers, managed a Drupal (CMS) site, and worked on several projects that delivered dynamic content over the web, so working on a modern static-site generator provides the opportunity to experience the pro's & con's of static sites.


All that resulted in this **tlm13** website:  A Jekyll built site hosted on GitHub Pages.


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
