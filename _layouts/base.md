---
common-css:
  - "/css/bootstrap.min.css"
  - "/css/bootstrap-social.css"
  - "/css/main.css"
common-ext-css:
  - "//maxcdn.bootstrapcdn.com/font-awesome/4.6.0/css/font-awesome.min.css"
common-googlefonts:
  - "Syne:400,500,600,700"
  - "Engagement"
common-js:
  - "/js/jquery-1.11.2.min.js"
  - "/js/bootstrap.min.js"
  - "/js/main.js"
---

<!DOCTYPE html>
<html lang="en">
  <!-- Beautiful Jekyll | MIT license | Copyright Dean Attali 2016 -->
  {% include head.md %}

  <body>

    {% include gtm_body.md %}

    {% include nav.md %}

    {{ content }}

    {% include footer.md %}

    {% include footer-scripts.md %}

  </body>
</html>
