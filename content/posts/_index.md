---
title: Posts
layout: posts
---

## Blog Stories

Welcome to the blog stories section! Here are the latest posts:

{{ define "main" }}
  <h2>Latest Pages</h2>
  {{ $pages := .Pages.GroupByDate .Date.Add(-1*24*60*60*time.Hour) }}
  {{ range $pages.Reverse | slice(0, 5) }}
    <h3><a href="{{ .RelPermalink }}">{{ .LinkTitle }}</a></h3>
  {{ end }}
{{ end }}