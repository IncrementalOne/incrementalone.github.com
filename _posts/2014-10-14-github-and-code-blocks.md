---
layout: post
category : blog
title: "Github and Code Blocks"
tags : markdown
---
{% include JB/setup %}

Getting the blog up and running it taking longer than anticipated. I keep getting side-tracked by small things as "What size should my headings be?". I just finished making jekyll work it's magic locally. Do not, i repeat, do NOT try to install ruby in a folder where the path contains one or more spaces! The development kit has a hatred for spaces and does not want to work under those circumstances, not even when I tried to go around the problem by creating a symbolic link without the space. Reinstalling was the only solution.

My latest diversion is finding how to present code examples in a nice way. The blog will be mainly used for taking notes on code related things, so making the code readable seems somewhat important. I did some research on syntax highlighting and found that [pygments](http://pygments.org/) seems to be the best choice. Unfortunately pygments requires an installation of python and after the ruby installation gave me a minor headache I wasn't to keen on it. I might have done it if I could have used python 3; it's been a while since I did some python scripting and it might be time to have a go at it again, but as far as I can tell only the development version of pygments supports python 3. I'm postponing it for another day.

Creating a code block turned out to be easier. I originally wanted to just use `<pre lang="html"><code>` tags but I can't find a way to inline custom html in markdown. Let's look at what githubs version of markdown does support. There seems too be two ways to make a simple code block.
<br><br>

#### Four spaces 

Indenting a line with four spaces makes a fenced block around it.  

[empty line]  
[4 spaces] <div><p>Hello<p/></div>  
[4 spaces] <div><p>Hello again<p/></div>  
[empty line]  

will show as:

    <div><p>Hello<p/></div>
	<div><p>Hello again<p/></div>

The good:

* This works great with short examples; quick to write.
* The Markdown text is easy to read.

The bad:

* Not as useful for long examples.
* If you want a block inside a list you need to indent it eight spaces. Which at least to me doesn't feel very practical. It's a little to easy to accidentally put seven or nine spaces instead of eight.)
<br><br>

#### Using three ~ 

Place ~~~ on an empty row; followed by an optional language such as "html", "javascript" etc. End the block with another three ~. You are also supposed to be able to use ``` instead of ~~~ to create a block, but I couldn't get it to work.

 ~~~html  
\<div><p>Hello<p/>\</div>  
\<div><p>Hello again<p/>\</div>  
~~~  

will show as:

~~~html
<div><p>Hello<p/></div>
<div><p>Hello again<p/></div>
~~~

The good:

* Easy to wrap large blocks of text.
* You can tell it which language to use.

The bad:

* Using ``` strangly doesn't work for me

