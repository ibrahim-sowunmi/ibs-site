---
title: "My first foray into SEO"
date: 2021-10-04T11:10:36+08:00
draft: false
language: en
description: The OG blog post and the beginning for ibrahimsowunmi.com
---

Hello Reader,

 

 

I have a problem. After building this website I wanted it to be google’able. I want someone to be able type my name and that very first link to be my personal site.

 

ibrahim sowunmi seo ranking
As it currently stands, I don’t even come up in the first 10 links and my link actually comes up on the second bloody page! (95% of traffic is on the first page)

 

Google has a very intelligent algorithm (googlebot) that trawls and indexes the whole of the light web (the part of the web accessible by google without authentication)! We want this algorithm to place my website with a higher ranking. Please, Serg & Larry!
 


How do I fix this? SEO. “Search engine optimization”, improving my site to increase its visibility to the algorithm. Awesome, so how do I improve this? I wasn’t really sure. So I googled tools to measure the SEO-ability of my site

 

ibrahim sowunmi lighthouse score first time
Higher than I expected but still pretty low

 

Google lighthouse, was one of the first I came across. Surprising, the website performed pretty well. I got a 92 for SEO? So, this tool clearly sucks. But, alas, I'm lazy and it's the best I've got 😔

 

My site it static. So, I can’t use any server-side rendering (no server). Client-side rendering and prerendering (sometimes uses a server, idk?) are my only options. I’ve never thought about SEO before in all honesty, so it was in interesting search. Learning about those 3 terms in the context of SEO.

 

So how will I attempt to do this?

 

1)    Prerender with react-snap. Initially I added a react helmet to all my components briefly outlining their function. React helmet allows you to set metadata (title, author, description) for my react components. Then I thought about the way SPA (Single page web apps) are loaded (sometimes multiple components at once) and figured something wasn’t right (multiple heads at once???). After sometime spent researching I realised if I’m not doing SSR (Server side rendering) then there isn’t much point to react-helmet. So prerendering with react-snap it is!

 

2)    Quality backlinks. The idea for PageRank — Google’s early ranking algorithm — stemmed from Einstein. Larry Page and Sergei Brin were students at Stanford, and they noticed how often scientific studies referred to famous papers, such as the theory of relativity. These references acted almost like a vote — the more your work was referenced the more important it must be. If they downloaded every scientific paper and looked at the references, they could theoretically decide which papers were the most important, and rank them.

 

They realized that because of links, the Internet could be analysed and ranked in a similar way, except instead of using references they could use links. So, they set about attempting to “download” (or crawl) the entire Internet, figuring out which sites were linked to the most. The sites with the most links were, theoretically, the best sites. And if you did a search for “university,” they could look at the pages that talked about “university” and rank them. Pretty cool story.

 

So, I pasted my URL perfectly into LinkedIn, Github & Medium. Fingers crossed.

 

3)I thought the name of your domain was relevant but I was very wrong unfortunately...     The name of your domain has zero effect on SEO ranking. To ensure quality rises to the top rather than matching domains. Dammit!

 

ibrahim sowunmi lighthouse sail test 2
 

Runnng the test again locally absolutely bombed performance (last test was on AWS) but accessibility and SEO are way up.

 

If googleing “Ibrahim Sowunmi” Doesn’t have a much higher result after the next google bot indexing, then my SPA SEO woes will have to be on hold until, next year.Click here to see how close I am to being SEO'd!