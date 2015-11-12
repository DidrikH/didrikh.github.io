---
layout: page
title: Arkiv
permalink: /arkiv/
---

<ul class="post-list">
    {% for post in site.posts %}
    {% assign currentdate = post.date | date: "%b, %Y" %}
      {% if currentdate != date %}
          <li id="y{{currentdate}}">{{ currentdate }}</li>
          {% assign date = currentdate %} 
        {% endif %}
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
       
      </li>
    {% endfor %}
  </ul>