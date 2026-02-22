---
layout: page
permalink: /repositories/
title: Repositories
description: A collection of the repositories that belong to me or that I find interesting.
nav: true
nav_order: 2
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-column align-items-stretch">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-column align-items-stretch">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const descriptionElements = document.querySelectorAll('[data-repo-description]');
    const cache = new Map();

    const setDescriptionText = (repository, text) => {
      const targets = document.querySelectorAll(`[data-repo-description="${repository}"]`);
      targets.forEach((target) => {
        if (!target.dataset.customDescription) {
          target.textContent = text;
        }
      });
    };

    descriptionElements.forEach((element) => {
      const repository = element.dataset.repoDescription;
      if (!repository || element.dataset.customDescription) {
        return;
      }

      if (cache.has(repository)) {
        setDescriptionText(repository, cache.get(repository));
        return;
      }

      const [owner, name] = repository.split('/');
      if (!owner || !name) {
        return;
      }

      fetch(`https://api.github.com/repos/${owner}/${name}`)
        .then((response) => {
          if (!response.ok) {
            throw new Error('Failed to fetch repository metadata');
          }
          return response.json();
        })
        .then((data) => {
          const description = data.description || '---';  // fallback to '---' if description is null
          cache.set(repository, description);
          setDescriptionText(repository, description);
        })
        .catch(() => {
          const fallback = '---';
          cache.set(repository, fallback);
          setDescriptionText(repository, fallback);
        });
    });
  });
</script>

{% endif %}
