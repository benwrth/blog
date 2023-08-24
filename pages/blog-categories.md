---
layout: page
title: Blog Categories
permalink: /blog/categories/
---

Looking for something more specific? Find an individual category to explore its contents.

{% for category in site.categories %}
  <div class="info-box">
  <p class="info-box-title">{{ category | first }}</p>
<table class="post-list">
    {% for post in category.last %}
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <tr class="post-table">
        <td class="post-table">
          <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title }}
          </a>
          <span class=" post-meta mobile-only">{{ post.date | date: date_format }}</span>
        </td>
        <td class="post-table desktop-only right" width="110px">
            <span class="post-meta">{{ post.date | date: date_format }}</span>
        </td>
        </tr>
    {%- endfor -%}
    </table>
  </div>
{%- endfor -%}

  <p class="right"><a href="/blog">Back to all posts</a></p>