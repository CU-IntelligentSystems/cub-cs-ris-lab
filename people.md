---
title: People
layout: default
nav_order: 4
---

# People
{: .no_toc }

This page lists all lab members and links to their WIP entries.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Lab members are listed by role, with links to their research contributions. The WIP entries section automatically aggregates all updates by each researcher.

## Faculty

*Coming soon...*

## Graduate Students

### Arturo
**Projects:** [Sonar Computer Vision](/projects/sonar-cv/)
**Research Focus:** Computer vision for underwater robotics, sonar imaging, simulation

## Undergraduate Students

*Coming soon...*

---

## WIP Entries by Person

{% assign wip_posts = site.pages | where_exp: "page", "page.path contains 'wip/'" | where_exp: "page", "page.title contains 'WIP:'" %}
{% assign presenters = wip_posts | map: "presenter" | uniq | sort %}

{% if presenters.size > 0 %}
{% for presenter in presenters %}
### {{ presenter }}
{% assign presenter_posts = wip_posts | where: "presenter", presenter | sort: "date" | reverse %}
{% for post in presenter_posts %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%Y-%m-%d" }} - {{ post.project }}
{% endfor %}
{% endfor %}
{% else %}
*No WIP entries yet.*
{% endif %}
