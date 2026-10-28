---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

Pages and publications available on this site. An [XML sitemap]({{ base_path }}/sitemap.xml) is also available.

<h2>Pages</h2>
{% for post in site.pages %}
  {% if post.title and post.sitemap != false %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Publications</h2>
{% assign publications = site.publications | sort: "date" | reverse %}
{% for post in publications %}
  {% include archive-single.html %}
{% endfor %}
