---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


{% assign pubs = site.publications | sort: 'date' | reverse %}

{% assign current_year = "" %}
{% for pub in pubs %}
  {% assign pub_year = pub.date | date: "%Y" %}
  {% if pub_year != current_year %}
   {{ pub_year }}
    {% assign current_year = pub_year %}
  {% endif %}

  {% include publication-item.html pub=pub %}
{% endfor %}
