---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#  
layout: home
---  
Welcome to my website! Explore hybrid cloud computing, Kubernetes, and AI innovations.

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <div><span class="post-meta">{{ post.date }}</span></div>
    <div><span class="post-meta">{{ post.tags | join: ", " }}</span></div>
    <h3>
      <a
        class="post-link"
        href="{{ post.url }}"
      >
        {{ post.title }}
      </a>
    </h3>
  </li>
  {% endfor %}
</ul>