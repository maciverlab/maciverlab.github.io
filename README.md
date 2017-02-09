# maciverlab.github.io
Jekyll page for MacIver Lab: 

## MacIver Lab Repository Site:

This repository is the organization github page for the MacIver Lab, and contains the required jekyll files to compile the static site

### Structure:

There are three main pages
2. Projects
3. Data

### Research Page:

Research page information about current research that goes on in the lab. Each research area (active electrosense, neuromechanics,...)
are created through posts located in the _posts directory. 

### How to add research or modify:

You can add any posts in markdown or html to the (\_posts) directory. 
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

This page is dedicated for projects that have a github repo. In creating the page the html looks for posts in the directory _ posts that have the type: about and paper: related paper. 

Eg. For bigeye this would be

```
---
title: Massive increase in visual range preceded the origin of terrestrial vertebrates
paper: bigeye
type: about
---
```

This will put the abstract along with the title to the page. For an explanation of code page, a post in markdown needs to be created and placed in the \_projects folder. The project post needs to have a title, paper and category specified. 

Eg. For bigeye
```
---
title: Massive increase in visual range preceded the origin of terrestrial vertebrates
paper: bigeye
categories: bigeye
---
```

The paper front matter links the post that resides in \_posts that contains the abstract to the project explanation post that is in \_projects. This creates custom domain that is dependent on the category specified in the \_projects/mm-dd-yy-posttitle.md, such as maciverlab.github.io/projects/bigeye/bigeye-explanation.html

## Data Page:

Data page works similar to the projects page but this time abstract or explanation regarding the paper are not provided. Data index.html looks through posts to see if there are ones that are type: about and goes to the \_projdata directory to search through posts 

