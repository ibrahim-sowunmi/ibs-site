---
title: "Hugo BaseURL with custom domain redirects"
date: 2021-10-04T11:10:36+08:00
draft: True
language: en
description: The OG blog post and the beginning for ibrahimsowunmi.com
---

my experience 

FIx

Hugo’s documentation is not entirely clear on the format of the baseURL value in config.toml when using github pages with a custom domain. When using a custom domain, you need to add the file static/CNAME whose contents are only the CNAME of your site (www.ibrahimsowunmi.com in the case of this site). However, the baseURL value does seem to require the protocol as well (I guess this is implied by URL in the name…), so in the case of this site https://www.ibrahimsowunmi.com.

Note that setting a blank baseURL, i.e. baseURL="" will do something that is almost certainly not what you would intend. It ends up creating URLs with paths that are relative to the current page you are viewing which will potentially break image paths,etc. depending on what page you are on.

