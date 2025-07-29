---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱 🌿 🌳 🖥️

<p style="padding: 3em 1em; background: var(--color-box-background, #2d2d2d); border-radius: 4px; color: var(--color-text,rgb(181, 149, 108));">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

>I figured this would be good place to put this:

Working Colorschemes:
><span style="background-color: rgb(0,0,0); color: rgb(235, 226, 215); padding: 2px 8px;">BLACK BACKGROUND | RGB (0,0,0)</span>

><span style="color: rgb(235, 226, 215);">MAIN TEXT FONT | RGB (235, 226, 215)</span>

><span style="color: rgb(16, 35, 57);">LINK TEXT FONT | RGB (16, 35, 57)</span>

<span style="font-size: 8px;">Other studies in the assets folder</span>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
