---  
title: CoffeeQuandary  
date: 2022-12-07  
share: true  
type: article  
description: "A site providing coffee reviews, discussions, and rants."  
demo: "https://coffeequandary.com"  
tech: React, NextJS  
permalink: "projects/coffee-quandary-v1/"  
tags: projects  
---  
  
[CoffeeQuandary](https://coffeequandary.com) is another website that I operate. My first foray into blogging was actually a site that was mostly for post reviews of various coffees and coffee gadgets that I've tried. In the summer of 2022, as I was writing down some notes on a coffee one morning, the itch to be posting these publicly came back. As of Fall 2022 and the launch of the site you are currently reading, I am planning to rewrite CoffeeQuandary and integrate it into my **Memex** publishing workflow. More on that below.  
  
# Lessons Learned  
At the time I was very interested in Next.js, so the site is built with it and deployed to Vercel. I really appreciate the developer experience that Vercel adds to their deployment tooling, but unfortunately I found Next.js itself to be lacking in few areas.   
  
## Content Authoring and Publishing  
First, was the actual publishing of static content like posts. With SSGs for blogs, the experience that Jekyll provides is my baseline. It was a bit of a pain to set something like that up for Next.js. At one point I figured that I wanted to take advantage of being able to write react components in my posts, so I tried to integrate MDX content using [ContentLayer](https://contentlayer.dev). For all the discussion about ease of use and react integration, I found it too buggy to fully commit to.   
  
For a long time, my workflow for coffee tasting notes and reviews is to enjoy some coffee and create notes in my **Memex** which was something like Evernote, Apple Notes, or Simplenote for a long time. I came to realize that it was going to be a pain to publish content from my **Memex** into a Next.js site in combination with all the other factors and system qualities that I wanted. This reason alone is why this project is called "Coffee Quandary ,v1" -- now that I've worked out a much smoother publishing system for this site, CoffeeQuandary needs to be rewritten and integrated into that flow.  
  
## Images  
Second, Next.js has a focus on website performance, but it gets there through very complicated means. Pages are server-side rendered by default, but in order have decent SEO, the page loading process is something like this:  
  
1. Load static version of the page  
2. Load react  
3. Let react do what it's going to do to further format the page  
  
As complex as this is, I assumed that it was going to be very usable given the popularity of Next and the dev time that has gone into perfecting this flow. Unfortunately, I found this flow to be problematic for basic things like loading images. Next has a react image component that does image optimization, but as you might image, if performance is optimized by loading react *later*, then loading images comes later too. I understand there is a new version of the image component that overcomes this, but something as basic as this not being flawless by version 12 of the framework gave me the heebie jeebies. For this site, Eleventy's image plugin works much better -- it optimizes images at build time and lets the browser handle html, css, js, and image loading in the all the ways that it knows best. For the types of sites I'm creating, I think this would be preferable. 