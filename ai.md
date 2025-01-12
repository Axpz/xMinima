---
layout: home
title: AI today
permalink: /ais/
---

<ul class="post-list">
  {% for post in site.posts %}
    {% if post.tags and post.tags.size > 0 %}
      {% assign keywords = "ai, artificial, artifact, ml, machine learning, neural network, deep learning" | split: ", " %}
      {% assign found = false %}
      
      {% for tag in post.tags %}
        {% assign tag_words = tag | downcase | split: " " %}
        {% for keyword in keywords %}
          {% if tag_words contains keyword %}
            {% assign found = true %}
            {% break %}
          {% endif %}
        {% endfor %}
        {% if found %}
          {% break %}
        {% endif %}
      {% endfor %}

      {% if found %}
        <li>
          <div><span class="post-meta">{{ post.date }}</span></div>
          <div><span class="post-meta">{{ post.tags | join: ", " }}</span></div>
          <h3>
            <a class="post-link" href="{{ post.url }}">
              {{ post.title }}
            </a>
          </h3>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>





