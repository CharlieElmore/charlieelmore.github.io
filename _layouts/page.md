---
layout: base
---

{% include header.md type="page" %}

<div class="container" role="main">
  <div class="row">
    <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
      {{ content }} {% if page.comments %}
      <div class="disqus-comments">{% include disqus.md %}</div>
      {% include fb-comment.md %}
      <div class="staticman-comments">{% include staticman-comments.md %}</div>
      <div class="justcomments-comments">{% include just_comments.md %}</div>
      {% endif %}
    </div>
  </div>
</div>
