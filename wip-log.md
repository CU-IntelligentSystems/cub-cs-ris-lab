---
title: WIP Log
layout: default
nav_order: 3
---

# Work-in-Progress Log
{: .no_toc }

This page shows the latest WIP entries across all projects, newest first.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

The WIP Log aggregates all work-in-progress updates from researchers across projects. Each entry follows a standardized format documenting goals, progress, results, and reproducibility details. Entries are automatically pulled from the `wip/` directory and sorted by date.

{% assign wip_posts = site.pages | where_exp: "page", "page.path contains 'wip/'" | where_exp: "page", "page.title contains 'WIP:'" | sort: "date" | reverse %}

{% if wip_posts.size > 0 %}
{% for post in wip_posts %}
## [{{ post.title }}]({{ post.url }})
**Date:** {{ post.date | date: "%Y-%m-%d" }}
**Project:** [{{ post.project }}](/projects/{{ post.project }}/)
**Presenter:** {{ post.presenter }}
**Status:** {{ post.status }}

---
{% endfor %}
{% else %}
*No WIP entries yet. Check back soon!*
{% endif %}
