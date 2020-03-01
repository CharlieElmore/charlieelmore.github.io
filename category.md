---
layout: page
---

{%- capture site_tags -%} {%- for tag in site.tags -%} {{- tag | first -}}{%- unless
forloop.last -%},{%- endunless -%} {%- endfor -%} {%- endcapture -%} {%- assign tags_list = site_tags | split:',' | sort -%}

<div class="post-list">
  {%- for post in site.tags[page.category] -%}
  <article class="post-preview">
  <div class="post-entry-container">
  <div class="tag-entry">
    <a href="{{ post.url | relative_url }}">
      <h2 class="post-title">{{ post.title }}</h2>

      {% if post.subtitle %}
      <h3 class="post-subtitle">{{ post.subtitle }}</h3>
      {% endif %}
    </a>
    <div class="entry-date">
      <time datetime="{{- post.date | date_to_xmlschema -}}">{{- post.date | date: site.date_format -}}</time>
    </div>
    <div class="post-entry">
      {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }} {% assign excerpt_word_count =
      post.excerpt | number_of_words %} {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
      <a href="{{ post.url | relative_url }}" class="post-read-more">[Read&nbsp;More]</a> {% endif %}
    </div>
    </div>
    </div>

  </article>
  {%- endfor -%}
</div>
