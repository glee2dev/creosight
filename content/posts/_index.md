---
title: Posts
layout: posts
---

## Blog Stories

Welcome to the blog stories section! Here are the latest posts:

{{ range first 5 .Pages.ByDate.Reverse }}
- [{{ .Title }}]({{ .Permalink }})  
  <small>{{ .Date.Format "January 2, 2006" }}</small>
{{ end }}