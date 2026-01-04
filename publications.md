---
layout: default
title: Publications
---

<div class="section-header">
    <h1>Publications</h1>
    <p class="section-description">Selected peer-reviewed publications</p>
</div>

<!-- Publications are loaded from _data/publications.yml -->
<!-- To add a new publication, simply edit that file -->

{% if site.data.publications %}

{% assign pubs_by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}
<h2 class="year-header">{{ year_group.name }}</h2>

{% for pub in year_group.items %}
<div class="publication">
    <p class="publication-title">{{ pub.title }}</p>
    <p class="publication-authors">{{ pub.authors }}</p>
    <p class="publication-venue">{{ pub.venue }}</p>
    {% if pub.pdf or pub.doi or pub.code %}
    <div class="publication-links">
        {% if pub.pdf %}<a href="{{ pub.pdf }}" target="_blank">PDF</a>{% endif %}
        {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
        {% if pub.code %}<a href="{{ pub.code }}" target="_blank">Code</a>{% endif %}
        {% if pub.slides %}<a href="{{ pub.slides }}" target="_blank">Slides</a>{% endif %}
    </div>
    {% endif %}
</div>
{% endfor %}

{% endfor %}

{% else %}

## 2024

<div class="publication">
    <p class="publication-title">Example Publication Title</p>
    <p class="publication-authors">AAA BBB, Co-Author Name</p>
    <p class="publication-venue">Conference/Journal Name, 2024</p>
    <div class="publication-links">
        <a href="#">PDF</a>
        <a href="#">DOI</a>
    </div>
</div>

<p class="text-muted mt-2">Add your publications to <code>_data/publications.yml</code> for easy management.</p>

{% endif %}
