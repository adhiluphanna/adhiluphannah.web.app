---
layout: default
---

{% assign redirects = site.urls | where_exp: "item", "item.redirect != nil" %}
{% for page in redirects %}
  [{{ page.url }}]({{ page.url | relative_url }}) 🔀 `{{ page.redirect }}`

  > {{ page.title | escape }}

  ---
{% endfor %}
