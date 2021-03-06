---
layout: page
title: Site
description: Information about this website.
---
*This page is dedicated to information about this website. If you want to learn about me*
*read the [About](/about) page.*

## Content Overview

### Organization

The websites's content is arranged in **posts** and **pages**.
There are two main differences between posts and pages:

1. Posts are tracked by the category system, while pages are not.
2. Posts have metadata, while pages do not.

I use pages for storing "meta-information": Information which is about the website itself.
For an example, consider this page. 
This page contains information about the website's content, organization, and technical details. 
The information here isn't likely to change drastically.
Accordingly, I use a page.

Posts are designed to be more dynamic and flexible than pages.
A post can be a one-off write up, or an on-going project.
Posts make up the bulk of this website's content.

#### Metadata

I took the idea of post metadata from [gwern.net](https://www.gwern.net).
Post metadata is information about posts available at a glance.
As of April 2019, a post can define as many metadata items as it needs.
However, there are six metadata items that are inherent to all posts:

* **created** - the date the post was first created.
* **updated** - the date the post was last updated.
* **status** - the status of the post. Technically the value of status could be anything, but some common statuses are *on-going*, *continuous*, and *completed*.
* **categories** - the categories the post belong to. The first category listed is called the primary category.
* **links** - links relevant to the post.


#### Categories

Each posts belongs to one or more categories.

The first category a post belongs to is its primary category.
The primary category describes what a post is *mostly* about.
It is the category the post will appear under on the home page, and the first cateogory listed in the post's metadata.

All other categories a post belongs to are called secondary categories.

## Technical Overview

### Jekyll
The core tool this website uses is the static site generator [Jekyll](https://jekyllrb.com/).
This is the first project I've used Jekyll on.
In all prior web design projects I used either a content management system such as [WordPress](https://wordpress.com/), or wrote my own basic content management system.

I chose Jekyll because I wanted a website which was fast and simple.
Jekyll, being a static site generator, produces static websites which are typically faster than dynamic websites.
And, thanks to the templating engine [Liquid](https://shopify.github.io/liquid/) and the ability to write plugins with [Ruby](https://www.ruby-lang.org/en/), Jekyll is dynamic and extensible like content management systems.


### Eric Meyer's Reset

Most modern websites use some form of CSS reset. I use [Eric Meyer's Reset](https://meyerweb.com/eric/tools/css/reset/).

As Eric Meyer's website states:

> The goal of a reset stylesheet is to reduce browser inconsistencies in things like default line heights, margins and font sizes of headings, and so on. 

When designing a website I don't want to worry about overriding browser styles.
I want a clean foundation to build my code on.


### Skeleton


[Skeleton](http://getskeleton.com/) is a small CSS library for responsive design.
In the past I have used [Bootstrap](https://getbootstrap.com/), but for this project I wanted something I could wrap my head around.
This website's structure is simple, so I don't need the extra features which Bootstrap provides.
I've [modified my version of Skeleton](/assets/css/skeleton.css) by removing the styles I didn't want.
It clocks in at just over one hundred and fifty lines, and gets the job done.


### Strict CSS

From my past projects I've notice that CSS has a tendency to devolve into [spaghetti code](https://en.wikipedia.org/wiki/Spaghetti_code).
I hate having to hunt down and override CSS rules. 
I want my styling to be precise.
Accordingly, I've adopted a strict style of writing CSS for this project.

There are three central practices to this "strict" code style:

1. Write as few global rules as possible i.e. avoid styling HTML elements at the global scale.
2. Use Sass to define global variables which are then used to provide consistency across the website (Jekyll has built-in support for Sass).
3. Write "strict" rules using the [child combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator).

Here is an example of what most rules using this style look like:

```css
.post-wrapper > .post-body > blockquote > p
{
    font-style: italic;
}

.post-wrapper > .post-body > blockquote cite::before
{
    content: "-- ";
}

.post-wrapper > .post-body > blockquote cite
{
   font-style: normal;
   padding-left: 30px;
}
```

While this style *does* result in having to write more code overall, what that code does is clear.
By using a chain of child combinators each rule is encapsulated in a structure which has precise effect.
In addition, the HTML code is restricted into the hierachy of the CSS rule-sets.
The stylesheet for this website can be found [here](/assets/css/base.css).
