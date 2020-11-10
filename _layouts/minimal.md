---
common-css:
- "/css/bootstrap.min.css"
- "/css/main-minimal.css"
common-js:
- "/js/jquery-1.11.2.min.js"
- "/js/bootstrap.min.js"
---

<!DOCTYPE html>
<html lang="en">

{% include head.md %}

  <body>

    <div role="main" class="container main-content">
      {{ content }}
    </div>

    {% include footer-minimal.md %}

    {% include footer-scripts.md %}

  </body>
</html>
