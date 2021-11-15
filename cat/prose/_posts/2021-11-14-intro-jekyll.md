---
layout: post
title: Intro to Jekyll
categories:
- prose
---

I have been long looking for a content management system for personal site and blog, and tried a few products including WordPress, but did not find
one that met my needs which are so simple (and somewhat naive): I just need a list of categories and publish posts under each category. 

Things start to change when I met [Jekyll](https://jekyllrb.com). Although I could not get Jekyll does what I want to do with one of
existing [Jekyll themes](https://jekyllthemes.io), I am able to make modifications to fit my purposes on top the default [minima theme](https://jekyll.github.io/minima/).

This post is not a generic introduction to Jekyll, for that you can follow the [Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/),
but rather my changes, and hope it could be of use for other people who have similar needs. 

- First I used `_data/cat.yml` file to setup a few categories:

```
- name: tax
  color: red
- name: math
  color: green
- name: poetry
  color: green
...
```

I use data because it provides an `ordered` list while `site.categories` does not provide. 

- The next step is build navigation page. I did this is `_layout/default.html`:

```
{% raw %}{%- for item in site.data.cat -%}
  {%- assign link = "/cat/" | append: item.name | downcase | append: ".html" %}
  ...
  {%- if is_current -%}<span style="color:blue;">&#9733 </span>{%- endif -%}
  <a href="{{ link }}"{%- if is_current -%}class="current"{%- endif -%}><span style="color: {{ item.color }};"> {{ item.name }}</span></a>
{%- endfor -%}{% endraw %}
```

That is, for each item, I set up a link. There are indications on categories you are reading, so you will not get lost.

- Set up the link

It would be tedious to setup and later modify each link, fortunately, we can setup a common `_layout/cat.html`:

```
{% raw %}<div class="wrapper">
  {%- assign topic = page.name | replace: ".html", "" %}
  {% for post in site.posts %}
  {% if post.categories contains topic %}
  <li><a href="{{post.url}}" target="_self">{{ post.title }}</a><span>{{ post.date | date: site.minima.date_format }}</span></li>
  {% endif %}
  {% endfor %}
</div>{% endraw %}
```

which display the posts of the referencing link, and each link is identified to each other which contains exactly these three lines:

```
---
layout: cat
---
```

These are the key points of my modification. The other advantage of using Jekyll is that it works with Github: you manage the
github files as you normally would and Jekyll converts them to static pages. As a matter of fact, the entire source code of
the [Tax and Life](http://taxandlife.com/) is on [this Githib repository](https://github.com/michaelxwang/michaelxwang.github.io). 
