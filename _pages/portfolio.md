---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---
This is a list of some of the software I've worked on in reverse chronological order. I hope you like them!

**Notice**: this list of projects is **not** complete and I still have many projects to add. Most of my projects are hosted on a private git repository.
{: .notice}

{% include base_path %}

{% assign portfolio = site.portfolio | sort: "order" | reverse %}
{% for post in portfolio %}
  {% include archive-single.html %}
{% endfor %}

