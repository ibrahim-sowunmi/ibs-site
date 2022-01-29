---
title: "A contemporary static site tech stack"
date: 2021-01-10T11:10:36+08:00
draft: true
language: en
description: 


---



I rebuilt my website. I wanted something that was easier to work with, faster, sleeker and more futureproof than my previous website. I'm not exactly sure what all of those would entail but I guess that's the purpose of future proofing. I'll be doing a series of posts about the obstacles I faced whilst building the website. Pointing to resources, that worked FOR ME, to get out of technical ruts. Of which there were many. Whilst building this, which in all honesty actually took me about two weeks as I just dove straight in and learnt as I went, I used a TON of blog posts, videos and documenation and I kind of wanted to give back.

My previous website was a bit of a nightmare and existed on React, AWS (Route 53, S3, Cloudfront).

I had everything stored in an S3 bucket, all images were manually placed in a folder. Then painstakingly refferenced. Every blog post was painfullly formatted with a ton of html 

<< ADD IMAGE >>

This is fine for long, fancy blog posts that display unqie info. When you want to blast out a 200 - 300 word into piece it really dissuades you from producing content. After doing this I'd log onto S3, manually drag and drop my build folders (sometimes I would forget to run build commands).

You're probably reading this thinking, the poor boy is a dunce, yes, I am. I have previously used terraform, beanstalk and even aws s3 sync. I was just so lazy. so so lazy. The laziness actually ended up costing me a hell of a lot of time. Everytime I would update the site I could barely remeber the process since I did it so infrequently. After a year of being held in a chokehold buy this site.

I had prior knowledge with HTML, CSS, Javascript react and AWS. So continuing working with that seemed intuitive. My old website was slow as anything. Long to work with in every sense.  It had an absolutely sickening load time. Taking a whole 3.7 seconds to load up on a 100Mb/s down line. I was exposing my readers (if any), to 1998 AOL dial up speeds. I broke 21st century geneva convention.

On the 10th of Jan, 2022. I said no more, and built a decided to build a new site on a new stack. After some preliminairy research I realised what I wanted. A static site, updatable via markdown, simple deploys, some CI/CD and minimal infrastructure to manage. DevOps is cool but not when I'm trying to leave a bookmark about << LINK >> the UX on children.

I settled on React (Front-end), Chakra (Front-end +) , Hugo, Netlify & AWS. React and Chakra, I had worked with before and that meant minimal fiddling. Hugo is the new kid on the block? 

> Hugo is **for people who want to hand code their own website** without worrying about setting up complicated runtimes, dependencies and databases. Hugo is for people building a blog, a company site, a portfolio site, documentation, a single landing page, or a website with thousands of pages.

It's meant to be dead fast and dead easy to deploy. It lets me easily create blogs and they're written in markdown. Which means one day if I every decide to burn everything down the ground it will be easy to move. That paragraph along got me. 

I also needed something to host the site on 

> The platform helps developers to build, test, and deploy websites.

Netlify seemed pretty popular and the only alternative in the space seemed to be cloudflare pages. After lurking through some forums where developers were discussing the pros and cons of each it seemed natural to settle on netlify. 

For a static site. This would be a large project. I created a trello board

 << BOARD >> 

And decided to break down development into phases. Home -> Blog -> Media (Books, Booksmarks) -> Art (Drawings, Photosets). I shamlessely took inspiration from a few sources. They are pretty well known in the nerd blogosphere. I wanted to create something that was a shrine to me I guess? Vain, but I'm fallible w/e.

After some resaech the stack mentioned above may have been very feasible but similair to my initial site build. It would have been a bit superfluous. So I decided to dive into a term I happened to come across a few times when googling around Hugo. Jamstack.

> JAMstack is a term that describes a modern web development architecture based on **JavaScript, APIs, and Markup (JAM)**. JAMstack isn’t a specific technology, but rather a different way of building apps and websites.

I liked the sound of it. It also meant to react. I had to use straight HTML. Which also meant straight CSS, pure pain. I haven't built a front-end project without react since I was 20 (24 as of writing this). Which is a decade in developer years. This may be painful. Fortunately, we live in the guilded age of information exchange. Some googling around also introduced me to tailwind. 

> Rapidly build modern websites without ever leaving your HTML.

That tagline said it all. I was in. So I had settled on a new stack for my build.

* Hugo
* Tailwind
* Netlify
* AWS

Oh, yeah, AWS for hosting my photosets (which as of writing this haven't been built yet but will be a behemoth in terms of storage ) and eventual domain routing. So that is a modern stack. They come with their cons but learning these technologies and mashing something together is a fun small/medium sized project.





 

