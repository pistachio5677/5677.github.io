---
layout: default
---

<div>
  {%- if site.posts.size > 0 -%}
    <h2>{{ page.list_title | default: "Posts" }}</h2>
    <ul>
      {%- for post in site.posts -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span>{{ post.date | date: "%Y-%m-%d" }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>
  {%- endif -%}
</div>
