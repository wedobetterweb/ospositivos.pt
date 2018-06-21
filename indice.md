---
layout: page
---
{%- if site.posts.size > 0 -%}
<ul>
    {%- for post in site.posts -%}
    <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        <br>
        <small>{{ post.date | date: date_format }}</small>
    </li>
    {%- endfor -%}
</ul>
{%- endif -%}