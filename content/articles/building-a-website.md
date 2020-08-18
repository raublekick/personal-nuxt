---
title: Building a VueJS developer website and blog with Nuxt
description: How I learned to stop worrying and love Nuxt.
createdAt: 2020-08-01
tags: ["Vue","Nuxt"]
---

## Purpose

Every developer eventually creates a website to highlight their work as well as blog posts on various topics. This is mine. 

## Trials

I orignially wanted to create a simple static site and blog using Vuepress. I found that vanilla Vuepress required a lot of work to get blog functionality working. After searching on the topic I found a boilerplate project with the Vuepress blog component configured with many nice features.[^1] But what I found was that I did not like working with Vuepress layouts. In hindsight, I think I was being lazy. 

Saber had recently become the new kid on the block and generated a lot of buzz.[^2] I tried this out and while it was easy to set up for a static website, it had many of the same issues I had with Vuepress. On top of that, I found the docs and plugins to be very hard to navigate.

## Enter: Nuxt

Nuxt is something I've been putting off learning for a long time. My opinion of it was based on assumptions, but I finally decided to dive in. After setting up a project with the Nuxt CLI, I was pleasantly surprised. It has first-class support for Buefy, my preferred UI library, and also allows you to include the content module, which I hadn't even read about. The content module is a powerful tool to make docs, blogs, or any other content you like. What appealed to me with the content module is that it gives you the tools to make what you want, but gets out of the way with how you do it. 

## Layout

Creating the layout was a breeze, as I am used to making layouts using Buefy. 


[^1]: [https://github.com/bencodezen/vuepress-blog-boilerplate](https://github.com/bencodezen/vuepress-blog-boilerplate)
[^2]: [https://saber.land/](https://saber.land/)