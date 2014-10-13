---
layout: post
category : [html, css, javascript]
title: Dynamic SVG with 'use' from an External Source
tags : [svg]
---
{% include JB/setup %}

This one took some time to figure out.

    <svg viewbox="0 0 512 512"> <use xlink:href="icons/test.svg#broken-bottle"/> </svg>

