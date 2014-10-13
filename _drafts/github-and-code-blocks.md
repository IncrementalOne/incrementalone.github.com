---
layout: post
category : blog
title: "Github and Code Blocks"
tags : markdown
---
{% include JB/setup %}

(use blog to note down coding solutions, need a way to do code blocks)
(want to use \<pre lang="html">\<code> but I can't find a way to inline html in markdown)
Let's look at what githubs version of markdown does support. There seems too be two ways to make a simple code block.
<br><br>

#### Four spaces 

markdown
4 indent gives a fenced block around anything

    <svg viewbox="0 0 512 512"> <use xlink:href="icons/test.svg#broken-bottle"/> </svg>
	
(problem: if you want a block inside a list you need to indent it with eight spaces. Which at least to me doesn't feel very practical. It's a little to easy to accidentally put seven or nine spaces instead of eight.)
<br><br>

#### Using three ~ 

(describe how to use it)
You are also supposed to be able to use ``` instead of three ~ to create a block, but I couldn't get it to work.

(preferable because you can tell it which language to use)

~~~html
<svg viewbox="0 0 512 512"> <use xlink:href="icons/test.svg#broken-bottle"/> </svg>
~~~

