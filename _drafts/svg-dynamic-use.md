---
layout: post
category : [html, css, javascript]
title: Dynamic SVG with 'use' from an External Source
tags : [svg]
---

This one took some time to figure out.

{% highlight html %}
<svg viewbox="0 0 512 512"> <use xlink:href="icons/test.svg#broken-bottle"/> </svg>
{% endhighlight %}
