---
layout: page
title: Senaste inlägg
permalink: /posts/
---

 <ul class="post-list">
    {% for post in site.posts limit:5 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>
          {{ post.content | truncatewords:50 }}
        </p>
      </li>
    {% endfor %}
  </ul>