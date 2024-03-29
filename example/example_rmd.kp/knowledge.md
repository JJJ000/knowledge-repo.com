---
title: Example post for a R Markdown file
authors:
- sally_smarts
- wesley_wisdom
tags:
- knowledge
- example
thumbnail: images/unnamed-chunk-1-1.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: This is short description of the content and findings of the post.
---

_NOTE: In the TL,DR, optimize for **clarity** and **comprehensiveness**. The goal is to convey the post with the least amount of friction, especially since notebooks require much more scrolling than blog posts. Make the reader get a correct understanding of the post's takeaway, and the points supporting that takeaway without having to strain through paragraphs and tons of prose. Bullet points are great here, but are up to you. Try to avoid academic paper style abstracts._

* Having a specific title will help avoid having someone browse posts and only finding vague, similar sounding titles
* Having an itemized, short, and clear tl,dr will help readers understand your content
* Setting the reader's context with a motivation section makes someone understand how to judge your choices
* Visualizations that can stand alone, via legends, labels, and captions are more understandable and powerful

**Contents**

[TOC]

_NOTE: this will include a table of contents when rendered on the site._


### Motivation

_NOTE: optimize in this section for **context setting**, as specifically as you can. For instance, this post is generally a set of standards for work in the repo. The specific motivation is to have least friction to current workflow while being able to painlessly aggregate it later._

The knowledge repo was created to consolidate research work that is currently scattered in emails, blogposts, and presentations, so that people didn't redo their work. 

### This Section Says Exactly This Takeaway

Here is some example code.


```r
plot(density(runif(100)), lwd=2, main="100 uniforms")
abline(h=0, v=0)
```

![](images/unnamed-chunk-1-1.png)<!-- -->


_NOTE: in graphs, optimize for being able to **stand alone**. As we aggregate and put things in presentations, we want to not have to recreate and add code to each plot to make it understandable without the entire post around it. When we compare this plot to other people's from other posts, will it be understandable without several paragraphs?_


### Common Mistakes

There are some requirements around how an R Markdown is developed to make the markdown render properly on the site. Here is a list of the ones that often lead to questions:

 - There should be one plot display call in each R block. The add_knowledge script currently gets confused if there are multiple plots in a given block:


```r
  ### My Header (treated as R comment, as it is in a code block)
  library(ggplot2)
  test_data <- data.frame(y1 = rnorm(100), y2 = runif(100), x = 1:100)
  ggplot(test_data, aes(y = y1, x = x)) + geom_line()
```

![](images/unnamed-chunk-2-1.png)<!-- -->

```r
  ggplot(test_data, aes(y = y2, x = x)) + geom_line()
```

![](images/unnamed-chunk-2-2.png)<!-- -->

 - Do not put markdown headers in R blocks. The knitr code will interpret the header #'s as R comments. This means that they will either be rendered properly as R comments within the block, or left out entirely if echo=FALSE

### Appendix

Put all the stuff here that is not necessary for supporting the points above. Good place for documentation of paths not pursued without distraction.