---
title: "Bookmarks"
date: 2021-12-18T11:10:36+08:00
draft: false
language: en
description: A test with @tailwindcss/typography & Prose
# type: "bookmarks"
layout: bookmarks
---

{{ $.Scratch.Set "authors" (slice ) }}
{{ range where .Site.RegularPages "Type" "in" .Site.Params.mainSections }}
  {{ with .Params.author }}
    {{ if eq ( printf "%T" . ) "string"  }}
      {{ if ( not ( in ($.Scratch.Get "authors") . ) ) }}
        {{ $.Scratch.Add "authors" . }}
      {{ end }}
    {{ else if ( printf "%T" . ) "[]string" }}
      {{ range . }}
        {{ if ( not ( in ($.Scratch.Get "authors") . ) ) }}
          {{ $.Scratch.Add "authors" . }}
        {{ end }}
      {{ end }}
    {{ end }}
  {{ end }}
{{ end }}