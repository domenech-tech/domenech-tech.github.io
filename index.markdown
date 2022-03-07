---
layout: default
---
<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }} {{post.date}}</a></h3>
      <p>{{post.description}}</p>
    </li>
  {% endfor %}
</ul>