---
layout: page
title: "People"
---

Currently, our lab has three active PhD students and two former students who are working as research associates. We also have an undergraduate researcher. *** We are always interested in hearing from potential students! *** 

# Current Members

{% for person in site.people %}
  <div class="clearfix" style="margin-bottom: 40px;">
    {% if person.image %}
      <img src="{{ person.image }}" width="200" style="float: left; margin-right: 15px; margin-bottom: 0px;">
    {% endif %}
    
    <h3><a href="{{ person.url }}">{{ person.title }}</a></h3>
    <p>{{ person.description | markdownify}}</p>
  </div>
{% endfor %}
