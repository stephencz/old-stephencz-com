---
layout: page
title: Site
description: Information about this website.
---
*This page is dedicated to information about this website. If you want to learn about me*
*read the [About](/about) page.*

## Technical Overview
{:.margin-top-l}

This section contains a series of vignettes about the technical side of this website.

### Jekyll
{:.margin-top-m}
The core tool this website uses is the static site generator [Jekyll](https://jekyllrb.com/).
This website is the first project I've used Jekyll on.
In all prior web design projects I either used a content management system such as [WordPress](https://wordpress.com/), or wrote my own basic content management system.
I chose Jekyll because I wanted a website which was fast and simple.
Jekyll, being a static site generator, produces fast websites.
And, thanks to the templating engine [Liquid](https://shopify.github.io/liquid/) and the ability to write plugins with [Ruby](https://www.ruby-lang.org/en/), dynamism similar to a content management system.


### Eric Meyer's Reset
{:.margin-top-l}

Most modern websites use some form of reset. I use [Eric Meyer's Reset](https://meyerweb.com/eric/tools/css/reset/).

As Eric Meyer's website states:

> The goal of a reset stylesheet is to reduce browser inconsistencies in things like default line heights, margins and font sizes of headings, and so on. 

When designing a website I don't want to worry about overriding individual browser styles.
Eric Meyer's Reset provides me with a clean baseline to work from.


### Skeleton
{:.margin-top-l}


[Skeleton](http://getskeleton.com/) is a small CSS library for responsive design.
In the past I have used [Bootstrap](https://getbootstrap.com/), but for this project I wanted something which I could fully wrap my head around.
This website's structure is simple, so I figured I could go without the extra features which come with Bootstrap.
I've [modified my version of Skeleton](/assets/css/skeleton.css) by removing the styles I didn't want.
It clocks in at just over one hundred and fifty lines, and gets the job done.


### Strict CSS
{:.margin-top-l}

From my past projects I've notice that CSS code has a tendency to devolve into [spaghetti code](https://en.wikipedia.org/wiki/Spaghetti_code).
I hate having to hunt down and override CSS rules. 
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
By using a chain of child combinators each rule is encapsulated into a structure which has precise effect.
In addition, the HTML code is indirectly restricted into the form of the rule-sets.
The stylesheet for this website can be found [here](/assets/css/base.css).