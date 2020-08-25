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

Creating the layout was a breeze, as I am used to making layouts using Buefy. Generally I am used to cramming many things into the main.js or App.vue files. It is nice to have a clean, simple layout file defined here with not much more going on. 

## Server-side Rendering

Server-side rendering is a nice feature of Nuxt, and Nuxt certainly makes it painless to get up and running. What I don't like is how black-boxed it is. It's running on a Node server, but it's not exactly obvious how or why it is doing anything. I cut my teeth in the olden days of ASP.NET with code-behind files and other such concepts that I'm glad we've moved beyond. But it was always obvious in ASP.NET-land what was client-side and what was server-side. This is certainly an area that I will have to brush up on with Nuxt, and I'm sure as I gain more of an understanding of the enviornment it will all make sense. 

## Conclusion

So far, Nuxt is very easy to get up and running with some advanced features not present in the vanilla Vue/vue-cli ecosystem. I like many of the features Nuxt brings, but there is plenty that requires digging into the documentation. 


[^1]: [https://github.com/bencodezen/vuepress-blog-boilerplate](https://github.com/bencodezen/vuepress-blog-boilerplate)
[^2]: [https://saber.land/](https://saber.land/)