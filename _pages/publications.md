---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for category in site.publication_category %}
  {% assign cat = category[0] %}
  {% for post in site.publications reversed %}
    {% if post.category == cat %}
      {% if forloop.first %}
        <h1>{{ category[1].title }}</h1>
      {% endif %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endfor %}
