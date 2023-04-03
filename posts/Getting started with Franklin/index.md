+++
date = "2023-03-25"
title = "Adding a Custom Domain to a Franklin Site Hosted on Github"
var"layout-post" = nothing
tags = ["julia", "franklin"]
rss = "My initial experiences of using Franklin, particularly setting up custom domains when hosting a Franklin based site on Github pages"

# Dependent variables
website_description = replace(rss, "*" => "")
rss_pubdate = Date(date)
+++

~~~
<h1><a href="{{ get_url }}">{{ markdown2html title }}</a></h1>
~~~

## Introduction to my Franklin Experience

[Franklin][f-link] is a static site generator for Julia. It can be used to create simple websites that can then be hosted via Github pages or similar.

I am the very beginning of a journey to learn Julia, and wanted somewhere to record that journey. So starting a simple blog, using the language I wanted to learn seemed like a good place to start.

Ths documentation on the Franklin website is very straightforward and give you a good starting point. This, combined with searching the [Julia Discourse][j-discourse] and finding a suitable theme on github made the whole process pretty simple.

Coincidentally at the same time I needed to create a simple website for my local cricket team. So another opportunity to use Franklin before I'd even publishd this site.

Again, it was easy to set up. With some easy HTML and CSS tweaking I had the [Buckfastleigh Cricket Club][buckfastleighcc] website up in a couple of evenings.

However, one area where I found the Franklin documentation lacking was setting a custom domain for the website. A bit of online searching and piecing things together and I got there. 

I thought it might be helpful to record the steps I took to get there, and that it might the source of a good initial post for this site.

## Setting a Custom Domain for a Franklin Website on Github Pages

These are steps that workes for me; I can't promise they will work for you.

1. Purchase your desired domain name.
2. Add the domain name to the `config.md` file:
```julia
website_url = "https://yourdomain.com"
```
3. If your code is hosted as a project, which this site is, then also add the following to the `config.md` file:
```julia
@def prepath =
```



[f-link]: https://franklinjl.org/
[j-discourse]: https://discourse.julialang.org/
[buckfastleighcc]: https://buckfastleighcc.uk/