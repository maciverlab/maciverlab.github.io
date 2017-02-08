# maciverlab.github.io
Jekyll page for MacIver Lab: 

## MacIver Lab Repository Site:

This repository is the organization github page for the MacIver Lab, and contains the required jekyll files to compile the static site

### Structure:

There are three main pages
1. Research
2. Projects
3. Data

### Research Page:

Research page information about current research that goes on in the lab. Each research area (active electrosense, neuromechanics,...)
are created through posts located in the _posts directory. 

### How to add research or modify:

You can add any posts in markdown or html to the _posts directory. 
Jekyll posts are named in a particular convetion: yyyy-mm-dd-title.md/html, and have at the beginning what is called the front matter

To add posts into the research page the frontmatter of the post should look like:

```
---
title: Active Electrosense (a descriptive title of reseach)
categories: research
---
```

The html file of the research page searches through the posts directory to find posts that have the category research and posts
them to the page.

### Projects Page:

This page is dedicated for projects that have a github repo. 


