---
layout: page
permalink: /repositories/
title: Repositories
description: List of some of my repositories on Github
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

## GitHub Profile Pictures

<div class="repositories d-flex flex-wrap justify-content-center gap-2">
  {% for user in site.data.repositories.github_users %}
    <div class="repo p-1 text-center">
      <a href="https://github.com/{{ user }}" aria-label="{{ user }} GitHub profile">
        <img
          class="rounded-circle"
          alt="{{ user }}"
          src="https://avatars.githubusercontent.com/{{ user }}?size=160"
          width="96"
          height="96"
          loading="lazy"
        >
      </a>
      {% if site.data.repositories.github_users.size > 1 %}
        <div class="small mt-1">{{ user }}</div>
      {% endif %}
    </div>
  {% endfor %}
</div>
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
