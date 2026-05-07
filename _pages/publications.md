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
    <h2 style="margin-top:40px;">{{ pub_year }}</h2>
    {% assign current_year = pub_year %}
  {% endif %}

  <div style="display:flex; gap:24px; margin-bottom:36px; align-items:flex-start;">

    {% if pub.preview %}
    <div>
      <img src="{{ pub.preview | relative_url }}"
           style="width:140px; height:auto; border-radius:4px;">
    </div>
    {% endif %}

    <div style="flex:1;">

      <div style="font-size:30px; font-weight:500; line-height:1.3;">
        {{ pub.title }}
      </div>

      <div style="margin-top:8px; font-size:20px;">
        {{ pub.authors | markdownify | remove: '<p>' | remove: '</p>' }}
      </div>

      <div style="margin-top:6px; font-size:20px;">
        <em>{{ pub.venue }}</em>
      </div>

      <div style="margin-top:10px; font-size:18px;">

        {% if pub.official_url %}
        <a href="{{ pub.official_url }}" target="_blank">
          📄 Publisher's Version
        </a>
        {% endif %}

        {% if pub.bibtex %}
        <a href="javascript:void(0);"
           onclick="toggleBibtex('{{ pub.slug }}')"
           style="margin-left:18px;">
           🧰 BibTeX
        </a>

        <div id="bibtex-{{ pub.slug }}"
             style="display:none; margin-top:10px;">

<pre style="background:#f5f5f5;
padding:12px;
font-size:14px;
overflow-x:auto;">{{ pub.bibtex }}</pre>

        </div>
        {% endif %}

      </div>

    </div>

  </div>

{% endfor %}

<script>
function toggleBibtex(id) {
  var x = document.getElementById("bibtex-" + id);

  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
</script>
