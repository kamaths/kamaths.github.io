---
layout: post
title: Starting a blogging website using Jekyll and Github pages!
excerpt: Some useful links and tips on how I setup this website using Jekyll and Github pages.
tags: [Jekyll, Github, Atom]
comments: true
---

I was looking into some easy ways to create a blogging website, and using Jekyll hosted on Github pages had pretty amazing reviews. There is good documentation and blogs which explain how to get started. Here I will briefly describe some of the links that I found useful.

Why I found Jekyll on Github useful:

* It can be run locally to visualize your website before it goes live.
* Integration with Github => free hosting and using Git :)
* Easy to understand directory structure.
* Maintenance is easy => editing ```_posts``` folder to add new posts.

For a good introduction to Jekyll:

* <http://jekyllbootstrap.com/lessons/jekyll-introduction.html>
* <https://jekyllrb.com/docs/home/>

For more hands-ons introduction:

* <http://jmcglone.com/guides/github-pages/>

Editor for Mac OS

* <https://atom.io/>

Theme I used here:

* <https://github.com/mmistakes/minimal-mistakes>

Setup

* Once you have a repository with `<username>.github.io`
* My directory structure looks like this:

```
.
├── _config.yml
├── _data
|   ├── navigation.yml
├── _includes
|   └── _analytics.html
|   └── _author-bio.html
|   └── _disqus_comments.html
|   └── _header.html
|   ├── _footer.html
|   └── _navigation.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── hikes
|   |   └── 2016-07-13-hello.md
|   └── tech
├── _site
├── _sass
├── _templates
├── assets
├── about
├── posts
├── .jekyll-metadata
└── index.md
```

* Jekyll configuration exists in ```_config.yml```. With Minimal Mistakes theme, you can add social media user names here.
* ```_includes``` folder contains files that are can be included in the main layout files in ```layouts```.
* To add analytics, register your website with [Google Analytics](https://analytics.google.com/). The code can be included in ```_config.yml``` and insert script provided after registering in ```_includes``` as ```_analytics.html```. This file can be included in all files in ```_layouts``` to provide analytics for your web pages.
* Similarly, to add comments, register your website with [Disqus](https://disqus.com/admin/universalcode/). Add the disqus short name in ```_config.yml```. The script in ```_disqus_comments.html```.
* I got the icons and other UI components in ```_sass``` and ```assets``` from the Minimal Mistakes theme.
* `about` contains the markdown page which the layout for about page.
* Similarly, the content in each of the `_posts` gets substituted in the layout `post` where ```{ {  content} }``` is present. 

Now once you are ready, with a simple ```git push``` to your main repo, your website is live.
