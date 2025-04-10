---
layout: default
title: Blog
---
## Blog

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})
_{{ post.date | date: "%B %d, %Y" }}_

{{ post.content }}

---

{% endfor %}


<h3>All Posts</h3>
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> – {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>
