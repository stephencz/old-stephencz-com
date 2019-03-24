---
layout: page
title: Site
description: Information about this website.
---
*This page is dedicated to information about this website. If you want to learn about me*
*check out the [About](/about) page.*

## Content Structure

## Technical Overview
{:.padding-t-m}

In this section I will attempt to give an overview of the tools and methods I used when creating this website.

### Why Jekyll?
{:.padding-t-xs}

The core tool which this website uses is the static site generator [Jekyll](https://jekyllrb.com/).
A static website is a website which serves its web pages as they are stored.
There is little reliance on server-side applications to dynamically retrieve or generate content.
Pages are stored on the server as HTML files, and they are served from the web server to your web browser as HTML files[^1].
The benefit of building and using a static website is that they are often *much* faster than their dynamic counterparts.
Espcially, when the website is stored on a shared web server[^2].

The major downside, at least in the past, of using a static website is that they are... static. 
You see that simple looking sidebar at the top left of this page?
That sidebar appears on almost every single page of this website.
And each page of this website is a seperate file.
That means that if I was to maintain this website manually I would have to copy the code for the sidebar into *every single file*.
What happens if I want to change something about the sidebar?
I would have to go into every single file, and make the changes.
That would be an immense amount of work and would leave this website open to wild inconsistency and error.
A manually maintained static website is not an ideal solution.

Traditionally, the solution to is to keep the code for the sidebar in a single file, and dynamically insert that code where it is needed. 
The language [PHP](http://www.php.net/) has a neat statement called `include` which can achieve this.
Stored on your web server would be a file called `sidebar.php`, and everywhere you need it you would do something like this:

```php
include 'sidebar.php';
```

Now, when you want to make changes to the sidebar, all you have to do is change that one file, and those changes will be reflected everywhere there is an `include` statement.
This is an acceptable solution and is used by popular content management systems such as [WordPress](https://wordpress.com/). 
Dynamic solutions which rely on the web server to retrieve or generate content can yield highly maintable and highly dynamic websites.

The flaw with this solution stems primiarly from the limitations of cheap web hosting. 
The majority of those ten dollar a month web hosting plans that you see are shared hosting services.
This means that your website will be hosted on a web server which contains many other websites.
If your website is running a CMS such as WordPress, than chances are your website will exist on a web server containing many other websites *also running WordPress*.
Because of the server-side overhead of many WordPress websites performing many server-side operations, more often than not, your website will have poor and inconsistent performance.

There are ways around this.
Paying more for a virtual private server or, for larger websites, a dedicated server will probably result in a faster website.
And maybe even utilizing optimization plugins that are often available for popular content managment systems will make things a bit faster.
But if you are not willing to shell out more cash, or endlessly fiddle with a bulky content management system, what is the alternative?

**Jekyll provides the best of both worlds.** 
Through the use of plugins written in [Ruby](https://www.ruby-lang.org/en/) and a templating engine called [Liquid](https://github.com/Shopify/liquid), 
the maintaince problem of static websites can be avoided, and the dynamism of content management systems can be retained. 
And, with Jekyll being a "static site generator", the end result of a site build will be a fully static website.
The only overhead on the server-side will be the overhead introduced by the programmer.
Which means that in most cases your website will be faster than a website running on a content management system.

While Jekyll might not be the best choice for every web design project, it was right choice for mine, and I recommend it to anyone wanting to make a similar project.


### CSS Dependencies and Code Style
{:.padding-t-s}

This website uses two CSS libraries: Eric Meyer's [Reset](https://meyerweb.com/eric/tools/css/reset/) and a modified version of [Skeleton](http://getskeleton.com/).


[^1]: The flip side to a static website is a dynamic website. Websites built with content management systems
      such as WordPress, Drupal, Joomla, or any of the other innumerable CMS options, are dynamic websites. They 
      often use server-side languages such as PHP to dynamically generate content as it is requested. While dynamic
      websites *can* be fast, they often aren't. 

[^2]: A web server which hosts multiple websites.
