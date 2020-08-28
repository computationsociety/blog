---
layout: page
title: Contributing an article
permalink: /guide/
---

All articles are written in markdown with minimal formatting necessary. To a first approximation your article should simply be a plain text file. Here's the basic template your article should use:

```
---
layout:     post
title:      Using markdown
date:       2015-12-01 9:00:00
summary:    Learn to write a post in markdown
author:     Your name
permalink:  /guide/
visible:    False
---

Articles are written in markdown (kramdown).  
Please use minimal formatting for your article.

This is a single paragraph. It is separated by newlines. 
No need for html tags. A single line break does not start a new
paragraph.

This is a second paragraph. 
You can place subsections as follows.



## Using maths

You can use math as you would in latex, except that we always use double dollar signs, even for inline equation. Let $$n>2$$ be an integer.
Consider the centered equation (we use html tags to center it):

$$ a^n + b^n = c^n $$
{: style="text-align:center;"}

Wiles proved the following theorem.

> **Theorem** (Fermat's Last Theorem).
> The above equation has no solution in the positive integers.

## Links and images

You can place a link like [this](http://wikipedia.org).

You place a picture similarly:

![Lander](https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Albert_Bierstadt_-_The_Rocky_Mountains%2C_Lander%27s_Peak.jpg/320px-Albert_Bierstadt_-_The_Rocky_Mountains%2C_Lander%27s_Peak.jpg)

## Emphasis and boldface

Use *this* for emphasis and **this** for boldface.

## You're all set.

There really isn't more you need to know.
```
The post would appear like [this](/guide/example/) on the web.
If you need more than what is in the above example, check out this
[kramdown reference](http://kramdown.gettalong.org/quickref.html).
You may also use any valid HTML tag in your article, but please try to avoid this.

## Submitting an article

The blog lives in this [github repository](https://github.com/computationsociety/computationsociety.github.io). If you are a regular contributor and your github account has admin access to the repository, you can add an article like this from your command line:

```
git clone https://github.com/computationsociety/computationsociety.github.io
cd computationsociety.github.io/_posts
cp 2015-12-01-template.md 2015-12-01-your-post-tile.md
git add 2015-12-01-your-post-tile.md
# edit the article using your favorite editor
git commit -m "my post"
git push -u origin master
```

If after that you make more changes you can upload them as follows:

```
git commit -am "new changes"
git pull
git push
```

If you don't have admin access, you can either create a [pull request](https://help.github.com/articles/creating-a-pull-request/) (assuming you're comfortable with git) or send any regular contributor the article in markdown. If so, please start from [this template](https://raw.githubusercontent.com/computationsociety/computationsociety.github.io/master/_posts/2015-12-01-template.md) and follow the above.
