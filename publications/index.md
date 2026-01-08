---
layout: page
title: Publications
subtitle: Peer-reviewed papers, preprints, and other outputs
permalink: /publications/
---

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}
<section class="section">
  <div class="section-header">
    <h2>{{ year_group.name }}</h2>
  </div>
  
  <ul class="publication-list">
    {% for pub in year_group.items %}
    <li class="publication-item">
      <span class="publication-year">{{ pub.year }}</span>
      <h3 class="publication-title">{{ pub.title }}</h3>
      <p class="publication-authors">{{ pub.authors }}</p>
      <p class="publication-journal"><em>{{ pub.journal }}</em>{% if pub.volume %}, {{ pub.volume }}{% endif %}</p>
      <div class="publication-links">
        {% if pub.pdf and pub.pdf != "" %}<a href="{{ pub.pdf }}">PDF</a>{% endif %}
        {% if pub.doi and pub.doi != "" %}<a href="{{ pub.doi }}">DOI</a>{% endif %}
        {% if pub.code and pub.code != "" %}<a href="{{ pub.code }}">Code</a>{% endif %}
        {% if pub.data and pub.data != "" %}<a href="{{ pub.data }}">Data</a>{% endif %}
      </div>
    </li>
    {% endfor %}
  </ul>
</section>
{% endfor %}

<section class="section">
  <div class="section-header">
    <h2>Google Scholar</h2>
  </div>
  
  <p>For a complete and up-to-date list of publications, see the PI's <a href="https://scholar.google.com/citations?user=YOURID">Google Scholar profile</a>.</p>
</section>
