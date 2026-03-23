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

<div class="github-users-merged">
  {% for user in site.data.repositories.github_users %}
    <div class="github-user-row">
      <div class="github-user-avatar-block">
        <a href="https://github.com/{{ user }}" aria-label="{{ user }} GitHub profile">
          <img
            class="github-user-avatar"
            alt="{{ user }}"
            src="https://avatars.githubusercontent.com/{{ user }}?size=320"
            width="160"
            height="160"
            loading="lazy"
          >
        </a>
        <div class="github-user-name">{{ user }}</div>
      </div>

      <div class="github-user-stats">
        {% include repository/repo_user.liquid username=user %}
      </div>
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
