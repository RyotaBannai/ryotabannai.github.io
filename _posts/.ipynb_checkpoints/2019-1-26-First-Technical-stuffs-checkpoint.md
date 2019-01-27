---
layout: post
title: First Technical Stuffs
---

<h1>{{ page.h1_title }}</h1>

I have encountered samll stumbling block to fully start out jekyii.<br/>

<h2>Issue 1: jekyii: command not found</h2>
<p><b>Solution</b>:</p>
```shell
export PATH=$(brew --prefix ruby)/bin:$PATH
```
<p><b>Note</b>: This is only for Mac. Details is <a href="https://github.com/jekyll/jekyll/issues/1504">here</a></p>

<h2>Issue 2: Showcase blog posts descend order: From latest to oldest.</h2>
<p><b>Solution</b>: <b>add reversed</b> ater site.posts array. <u>Please get rid of backslashes\ I just needed these since Liquid detects them as operational tags without \.</u></p>

```liquid
---
layout: default
---
<div class="posts">
  {\% for post in site.posts reversed \%}
```

<p><b>Note</b>: The usage in details can be find <a href='https://shopify.github.io/liquid/tags/iteration/'>here</a></p>


<h2>Issue 3: roughfy: command not found</h2>
<p><b>Solution</b>:</p>
```shell
export PATH="/usr/local/Cellar/ruby/2.0.0-p247/bin:$PATH"
```

<p><b>Note</b>:</p>
<ul>
    <li>Chagen the ruby version depending on yours. This is only for Mac.</li>
    <li>User guide for Roughfy can be found <a href='https://bnhr.xyz/2017/03/25/add-syntax-highlighting-to-your-jekyll-site-with-rouge.html'>here</a></li>
</ul>

<h2>Issue 4: Run on an another port other than 4000</h2>
<p><b>Solution</b>:</p>
```shell
jekyll serve --port 4001
```