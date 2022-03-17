---
layout: default
---
<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }} {{post.date | date_to_string }}</a></h3>
      <p>{{post.excerpt}}</p>
    </li>
  {% endfor %}
</ul>