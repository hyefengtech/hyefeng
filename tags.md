---
layout: page
title: Tags
permalink: /tags/
---

{% raw %}
{% assign tags = site.tags | sort %}
{% for tag in tags %}
<h2>{{ tag[0]}} </h2>
<ul>
    {% for post in tag[1] %}
    <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
{% endfor %}
{% endraw %}

