---
layout: page
permalink: /repositories/
title: repositories
description: A sampling of the public GitHub repositories and accounts for members of the MAIEUTIC Lab. We have a lot more work on HuggingFace, personal websites, and GitLab (and a lot of other places as well).
nav: true
nav_order: 4
---


{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}



{% if site.data.repositories.github_users %}

## GitHub users

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}
