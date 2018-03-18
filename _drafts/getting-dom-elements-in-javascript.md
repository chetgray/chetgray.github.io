---
layout: post
title: Getting DOM Elements in JavaScript
date: 2018-03-17
---

* getElementById
* getElementsByClassName
* getElementsByTagName
* querySelector
* querySelectorAll

https://jsperf.com/getelementbyid-vs-queryselector

`getElementsByClassName` and `getElementsByTagName` return a live `HTMLCollection`.
`querySelectorAll` returns a static `NodeList`.

`querySelector` and `querySelectorAll` cannot use CSS pseudo-elements in the selector.
