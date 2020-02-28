---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can also find my articles on <u><a href="https://scholar.google.com/citations?user=6ZSwOZgAAAAJ">my Google Scholar profile</a>.</u>

{% include base_path %}

## Preprints

{% for post in site.preprints reversed %}
  {% include archive-single.html %}
{% endfor %}

## Peer-reviewed Journal Articles

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
