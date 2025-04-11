---
layout: page
title: "Recent Publications"

---

Here are some of our recent publications. You can find all them on [Google Scholar](https://scholar.google.com/citations?user=564iLhYAAAAJ&hl=en)


{% assign max_projects = 5 %}
{% assign project_count = 0 %}
{% for project in site.pubs %}
  {% if project_count < max_projects %}
  <div class="clearfix" style="margin-bottom: 40px;">
    {% if project.image %}
      <img src="{{ project.image }}" width="200" style="float: left; margin-right: 15px; margin-bottom: 10px;">
    {% endif %}
    
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p>{{ project.description | markdownify }}</p>
    {% if project.link %}
      <a href="{{ project.link }}" target="_blank" rel="noopener noreferrer">Link.</a>
    {% endif %}
  </div>
    {% assign project_count = project_count | plus: 1 %}

  {% endif %}
{% endfor %}


{% if site.pubs.size > max_projects %}
  <div style="margin-top: 20px;">
    <a href="/archive" target="_self">See all publications</a>
  </div>
{% endif %}



