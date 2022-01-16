---
layout: default
title: myzettldarticles
---


A zettld version of articles I read FR/EN

<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    </li>
  {% endfor %}
</ul>

{% for post in site.posts limit: 10 %}
  <article class="index-page">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
	<h4>{{ post.date | date: "%a, %b %d, %y" }}</h4>
    {{ post.excerpt }}
  </article>
{% endfor %}
