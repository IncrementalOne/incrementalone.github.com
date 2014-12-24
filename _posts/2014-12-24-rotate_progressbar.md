---
layout: post
category : [bootstrap, css, html]
title: "Rotating a Bootstrap 3 Progress Bar with CSS3"
tags : [css3, progress bar, transform]
excerpt: Bootstrap has built in progressbars that are easily setup. But what if we want a horizontal bar? There doesn't seem to be an inbuilt way to make one, but CSS3 gives us a way to rotate it...
---
{% include JB/setup %}

Bootstrap has built in progressbars that are easily setup. But what if we want a horizontal bar? There doesn't seem to be an inbuilt way to make one, but CSS3 gives us a way to rotate it.
<br><br>

#### Setup the bar

	<div class="progress">
		<div class="progress-bar" role="progressbar" aria-valuenow="70" aria-valuemin="0" aria-valuemax="100" style="width: 70%;">
			<span class="sr-only">70% done</span>
		</div>
	</div>

*width* sets how far the progressbar has progressed and *class="sr-only"* hides the label on the bar. Above code will give a bar that looks like:  
{% raw %}
<div class="bs-example">
<div class="progress">
	<div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 70%;">
		<span class="sr-only">70% done</span>
	</div>
</div>
</div>
{% endraw %}
<br>

#### Lets rotate it!

	transform: rotate(90deg)
	
*rotate* will flip the bar around its center point. But say that we want its top left corner in the same place as before the transform.

	transform-origin: left bottom
	transform: translateY(-100%)

*transform-origin:left bottom* and *rotate(90deg)* will rotate the bar around its lower left corner, placing it just under where we want it.
*translateY(-100%)* moves it up to the top left cornern where the bar started.
<br>
<br>

All the CSS:

	.progress {
		-webkit-transform-origin: left bottom;
		-moz-transform-origin: left bottom;
		-ms-transform-origin: left bottom;
		-o-transform-origin: left bottom;
		transform-origin: left bottom;
		
		-webkit-transform: translateY(-100%) rotate(90deg);
		-moz-transform: translateY(-100%) rotate(90deg);
		-o-transform: translateY(-100%) rotate(90deg);
		-ms-transform: translateY(-100%) rotate(90deg);
		transform: translateY(-100%) rotate(90deg);
	}



	
<b>Take note!</b>&nbsp;&nbsp;[transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform#Browser_compatibility) and [transform-origin](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin#Browser_compatibility) is marked as "experimental technology" and is not not fully supported in all browsers.
