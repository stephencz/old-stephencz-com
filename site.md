---
layout: page
title: Site
description: Information about this website.
---
*This page is dedicated to information about this website. If you want to learn about me*
*check out the [About](/about) page.*

## Content Structure

## Technical Details
{:.padding-t-m}

In this section I will attempt to give an overview of the tools and methods I used when creating this website.

### Why Jekyll?
{:.padding-t-xs}

In the past I've tried several different approaches for managing my website and its content. 
I started with a static website: A website which serves content as stored and doesn't rely on a server-side application.
This approach works well for websites that don't changed often, but is impractiable for websites that grow. 
Having larger, more long term, ambitions in mind, I needed a more dynamic and maintainable solution. 

A CMS seemed like the obvious choice. 
At first I didn't like the idea of using a massive platform such as WordPress, so I tried to build my own CMS with PHP. 
I had some minor success with this. 
I managed to get my CMS to the point where it had a primitive backend which could create and store posts in a database. 
But, ultimately, I wanted to build a website, not reinvent the wheel. 
Having to build and maintain a website *and* a CMS isn't something I wanted to do.

After two or three months of stagnation I finally decided to give WordPress a try. 
And I liked it. 
WordPress is a great platform.
Espcially for people with little technical experience. 
Installing it is easy. 
There are plenty of free and paid themes to choose from. 
There is an endless supply of useful plugins. 
Its backend is straightforward and looks nice. 
Its well documented. 
I managed to learn the basics of creating a custom theme in an afternoon.
 My one problem with it is that it was *incredibly* slow.

Because of my website's size and relative infancy I use a shared hosting service. 
This means that my website exists on a web server containing many other websites. 
Before optimizations my WordPress site's performance was slow and inconsistent. 
There were times when a page would load instantly, and times when it would take tens of seconds. 
After optimizing the website, which consisted of installing plugins design for optimization, the performance increased marginally, but it still wasn't acceptable. 
On top of that, as someone who *does* have a technical background, I didn't like the idea of relying on plugins for my website to work.
I want to know what's going on behind the scenes and I want to be able to get my hands dirty.
While WordPress does allow that to an extent, it never felt organic to me. 

Enter [Jekyll](https://jekyllrb.com/): A static site generator. A 

*[HTML]: Hypertext Markup Language
*[CSS]: Cascading Style Sheets
*[PHP]: Hypertext Preprocessor
*[CMS]: Content Management System