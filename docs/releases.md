---
nav_order: 2
---

# Releases

{% for release in site.github.releases %}

## [{{ release.name }}]({{ release.html_url }})

{{ release.published_at | date: "%e %B %Y" }}

{{ release.body | replace: "##", "###" | markdownify }}

{% endfor %}