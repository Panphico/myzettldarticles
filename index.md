---
layout: default
title: myzettldarticles
crawlertitle: "myzettldarticles"
summary: "I read a lot of articles, mainly on software, work and personal development. If they are interesting, a create a Zettl-note, that this blog aims to share."
---


<h1>Latest Posts</h1>

<ul>
{% for post in site.posts limit: 20 %}
  <article class="index-page">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <h4>{{ post.date | date: "%a, %b %d, %y" }}</h4>
        {{ post.excerpt }}
  </article>
{% endfor %}

</ul>
