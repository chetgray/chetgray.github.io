---
layout: post
title: Getting DOM Elements in JavaScript
date: 2018-03-17
---

* `Document.getElementById`
* `Document.getElementsByClassName`
* `Element.getElementsByClassName`
* `Document.getElementsByTagName`
* `Element.getElementsByTagName`
* `Document.querySelector`
* `Element.querySelector`
* `Document.querySelectorAll`
* `Element.querySelectorAll`

https://jsperf.com/getelementbyid-vs-queryselector

`getElementsByClassName` and `getElementsByTagName` return a live `HTMLCollection` (except, apparently, in Webkit, wherein it returns a `NodeList`. Not sure if it's live or static.).
`querySelectorAll` returns a static `NodeList`.

`querySelector` and `querySelectorAll` cannot use CSS pseudo-elements in the selector.

`getElementById` can only be called on `document`. The rest can be
called on `document`, or on any `Element`, whereupon they only return
decendant `Node`s. However, the selectors for `querySelector` and
`querySelectorAll` use the full DOM scope, while still only returning
decendants. Scope can be restricted by adding the `:scope` pseudo-class
to the beginning of the selector.
