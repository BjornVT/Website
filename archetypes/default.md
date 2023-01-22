---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
url: /{{ .Name }}/
tags:
    - STM
    - ESP32
draft: false

thumbnail: "content/images/2023/temp.png"
lead: "Example lead - highlighted near the title" # Lead text
comments: false # Enable Disqus comments for specific page
# authorbox: false # Enable authorbox for specific page
pager: false # Enable pager navigation (prev/next) for specific page
toc: false # Enable Table of Contents for specific page
mathjax: false # Enable MathJax for specific page
sidebar: "right" # Enable sidebar (on the right side) per page
widgets: # Enable sidebar widgets in given order per page
  - "search"
  - "recent"
  - "taglist"
---

