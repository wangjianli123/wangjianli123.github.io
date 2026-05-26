---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  You can also find my articles on my <a href="{{ site.author.googlescholar }}">Google Scholar</a> profile.
{% endif %}

{% include base_path %}

{% assign current_year = "" %}

{% assign pubs = site.publications | sort: "date" | reverse %}

{% for post in pubs %}
{% assign post_year = post.date | date: "%Y" %}
{% if post_year != current_year %}
<h3 class="pub-year">{{ post_year }}</h3>
{% assign current_year = post_year %}
{% endif %}

{% include archive-single-publication.html %}
{% endfor %}
