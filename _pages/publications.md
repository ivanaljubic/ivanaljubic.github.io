---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

## Technical Reports / Submitted Papers

{% for post in site.publications reversed %}
{% if post.type == 'reportorsubmittedpaper' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

## Journal Articles

{% for post in site.publications reversed %}
{% if post.type == 'journal' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

## Edited Books

{% for post in site.publications reversed %}
{% if post.type == 'editedbook' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

## Book Chapters

{% for post in site.publications reversed %}
{% if post.type == 'bookchapter' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

## Refereed Conference Proceedings

{% for post in site.publications reversed %}
{% if post.type == 'refereedconf' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

## PhD Thesis

{% for post in site.publications reversed %}
{% if post.type == 'phdthesis' %}
{% include archive-single.html %}
{% endif %}
{% endfor %}
