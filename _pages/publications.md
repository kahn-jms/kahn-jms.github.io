---
layout: page
permalink: /publications/
title: publications
description: A list of my recent works, for the full list including many-author publications see my <a href='https://scholar.google.com/citations?user=X550jHAAAAAJ&hl=en'>Google Scholar profile</a>
years: [2023, 2022, 2021]
nav: true
nav_order: 1
bibtex_show: true
---
<!-- _pages/publications.md -->

<!--[Google Scholar profile](https://scholar.google.com/citations?user={{ site.data.scholar.id }}):-->

```python
google_scholar_metrics = {
  "citations": {{ site.data.scholar.citations }},
  "h-index": {{ site.data.scholar.h_index }},
  "i10-index": {{ site.data.scholar.i10_index }},
}
```

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
