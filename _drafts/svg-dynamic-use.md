---
layout: post
category : [html, javascript, svg]
title: "Dynamic SVG with &lt;use&gt; from an External Source"
tags : [svg use, xlink, file]
excerpt: I have been teaching myself about svgs. One of the cool things I found was &lt;use&gt;. This post is about how to combine &lt;use&gt; with having the svg as an external source...
---
{% include JB/setup %}


I have been teaching myself about svgs. One of the cool things I found was \<use\>. This post is about how to combine <use> with having the svg as an external source. Demo of how to define an svg with \<use\>:

	<svg viewbox="0 0 32 32"><use xlink:href="#circle"/></svg>

It allows you to link one svg to another one that already exists. Say you want ten copies of the same object placed at different locations on the page, using ten different svgs is a bit wasteful since the only thing separating them is their position. \<use\> lets you link the other nine objects to the first one. You can even make changes to the copies, change their color, size, rotate them... But this post is about how to combine \<use\> with having the svg as an external source, so if you want more indepth information on \<use\> specificly this [link](http://taye.me/blog/svg/a-guide-to-svg-use-elements/) is to someone that explains how \<use\> works.

	(code example of 2 separate svgs)
	(how it looks)

	(code example of use)
	(how it looks)
    <svg viewbox="0 0 512 512"> <use xlink:href="icons/test.svg#broken-bottle"/> </svg>


I want to be able to have a separate svg-file. (link the website that explains how to use an external source)(http://css-tricks.com/svg-use-external-source/)

How to combine 'use' with having an external source?

Could not find a guide that explains how.
