---
layout: default
permalink: /categories/
---


<div>
{% for category in site.categories %}
  <div>
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3>{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    {% endfor %}
  </div>
{% endfor %}
</div>